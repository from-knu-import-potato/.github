<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/baro-banner-black.png">
  <img alt="Baro Banner" src="./assets/baro-banner-white.png">
</picture>

<br/>

<table width="100%" border="0">
  <tr>
    <td><a href=""><img src="https://capsule-render.vercel.app/api?type=transparent&height=220&color=449CD4&text=BARO%20서비스%20링크&section=header&fontColor=000000&textBg=false&animation=twinkling&desc=%EC%8B%A4%EC%A0%9C%20%EC%9A%B4%EC%98%81%20%EC%A4%91%EC%9D%B8%20BARO%20%EC%84%9C%EB%B9%84%EC%8A%A4%EC%9E%85%EB%8B%88%EB%8B%A4&descAlignY=70&descSize=18&stroke=cacaca&reversal=false" width="100%" /></a></td>
    <td><a href=""><img src="https://capsule-render.vercel.app/api?type=transparent&height=220&color=72B4DE&text=BARO%20QA%20링크&section=header&fontColor=000000&textBg=false&animation=twinkling&desc=%EB%B0%B0%ED%8F%AC%20%EC%A0%84%20%ED%85%8C%EC%8A%A4%ED%8A%B8%20%EB%B0%8F%20%EA%B2%80%EC%A6%9D%20%ED%99%98%EA%B2%BD%EC%9E%85%EB%8B%88%EB%8B%A4&descAlignY=70&descSize=18&stroke=cacaca&reversal=false" width="100%" /></a></td>
  </tr>
</table>

<p align="center">↑ 이미지를 클릭하면 해당 서비스로 이동합니다</p>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=BARO%20팀원%20소개&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

<table width="100%">
  <tbody>
    <tr>
      <td width="25%" align="center"><a href="https://github.com/daaoooy"><img src="https://github.com/daaoooy.png" width="150px;" alt="유다연"/><br /><b>[팀장] 유다연</b></a><br />FE, BE</td>
      <td width="25%" align="center"><a href="https://github.com/ghlwz17"><img src="https://github.com/ghlwz17.png" width="150px;" alt="고효림"/><br /><b>[팀원] 고효림</b></a><br />기획</td>
      <td width="25%" align="center"><a href="https://github.com/kchaewon0317-ctrl"><img src="https://github.com/kchaewon0317-ctrl.png" width="150px;" alt="김채원"/><br /><b>[팀원] 김채원</b></a><br />기획</td>
      <td width="25%" align="center"><a href="https://github.com/soyunseop"><img src="https://github.com/soyunseop.png" width="150px;" alt="소윤섭"/><br /><b>[팀원] 소윤섭</b></a><br />기획</td>
    </tr>
  </tbody>
</table>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=시스템%20아키텍쳐&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

<picture>
  <img alt="Baro Service Architecture" src="./assets/baro-service-architecture.png">
</picture>

<br/>

### 핵심 기능 데이터 플로우

<details>
<summary><b>실시간 주문 (SSE)</b></summary>
<br/>

```mermaid
sequenceDiagram
    participant G as 손님 Browser
    participant F as Vercel (Frontend)
    participant B as Railway (Backend)
    participant O as 사장님 Browser

    O->>B: GET /orders/stream (SSE 연결 수립, Authorization: Bearer token)
    G->>F: 메뉴 선택 후 주문하기
    F->>B: POST /orders
    B->>B: DB에 주문 저장 + pending 재고 경고 계산
    B-->>O: SSE event: new-order (payload: 주문 정보 + stockWarnings)
    O->>O: stockWarnings → useOrderWarningsStore 저장
    O->>O: queryClient.invalidateQueries(['orders']) → 주문 목록 갱신

    Note over O,B: 주문 상태 변경(수락·취소·완료) 시
    O->>B: PATCH /orders/:id/status
    B->>B: adjustStockForOrder() — preparing 시 레시피 기반 즉시 재고 차감
    B-->>O: SSE event: order-status-changed
    O->>O: queryClient.invalidateQueries(['orders']) → UI 업데이트
```

</details>

<details>
<summary><b>OCR 입고 처리 파이프라인</b></summary>
<br/>

```mermaid
sequenceDiagram
    participant U as 사장님
    participant F as Frontend
    participant B as Backend
    participant C as Naver CLOVA OCR
    participant G as Gemini 2.5 Flash
    participant S as Supabase Storage

    U->>F: 거래명세서 이미지 업로드
    F->>B: POST /ocr/upload (multipart)
    B->>C: base64 이미지 전송
    C-->>B: 원시 OCR 텍스트 (fields 배열)
    B->>G: OCR 텍스트 + 식자재 목록 + 파싱 프롬프트 (temperature=0)
    G-->>B: 구조화 JSON (isInvoice, metadata, items)
    alt isInvoice = false
        B-->>F: 422 NOT_INVOICE 에러
    else isInvoice = true
        B->>B: 서버사이드 검증 (수량 0 이하, 음수 금액, 단가×수량 3% 초과 오차)
        B->>B: 메타데이터 검증 (공급가액 + 부가세 = 총액)
        B->>S: 명세서 이미지 저장 (invoice-images 버킷)
        B->>B: 식자재 이름 매핑 (storeIngredients 대조)
        B-->>F: 파싱 결과 반환 (items, metadata, imageUrl)
        F->>F: 비표준 단위(BOX·BTL 등) spec 파싱 → 변환 계수 계산
        F->>U: 검수 화면 표시 (경고 항목 하이라이트, 수동 확인 필수)
        U->>F: 항목별 수량·단위·매핑 검수 후 확정
        F->>B: POST /ingredients/inbound
        B->>B: currentStock 업데이트
    end
```

</details>

<details>
<summary><b>AI 발주 가이드 생성</b></summary>
<br/>

```mermaid
sequenceDiagram
    participant U as 사장님
    participant F as Frontend
    participant B as Backend
    participant G as Google Gemini

    U->>F: 발주 가이드 생성 요청
    F->>B: POST /order-guide/generate
    B->>B: 6가지 트리거로 발주 필요 식자재 필터링
    B->>B: 14일·3일 소비 평균 + 요일별 매출 패턴(8주) 수집
    B->>G: 식자재 컨텍스트 블록 + 매장 패턴 데이터 (temperature=0.3)
    G-->>B: ingredientId + recommendedOrderAmount + 추천 이유(reason)
    B->>B: calcStatus()로 긴급도 서버사이드 계산 (critical / warning / expiry)
    B->>B: purchaseConversions 역산 → BOX·BTL 단위 수량 변환
    B->>B: orderGuides DB 저장
    B-->>F: 발주 가이드 반환 (추천량 + 이유 + 긴급도 + 발주 단위 수량)
    F->>U: AI 추천 화면 표시
```

</details>

<details>
<summary><b>마감하기 플로우</b></summary>
<br/>

```mermaid
sequenceDiagram
    participant U as 사장님
    participant F as Frontend
    participant B as Backend
    participant DB as Supabase DB

    Note over U,DB: 영업 중 — 주문 수락 시 즉시 차감
    U->>B: PATCH /orders/:id/status → preparing
    B->>DB: adjustStockForOrder() — 레시피 기반 currentStock 즉시 차감
    Note over B,DB: 취소 시 sign=-1로 즉시 복원

    Note over U,DB: 마감 시작
    U->>F: 마감하기 클릭
    F->>B: GET /closing/preview
    B->>DB: preparing + completed 주문 × 레시피 → orderDeductedAmount 합산
    B->>B: openingStock = currentStock + orderDeductedAmount (영업 시작 재고 역산)
    B-->>F: 식자재별 {openingStock, orderDeductedAmount, isNegative}
    F->>U: 미리보기 화면 — 이론 차감량 확인

    U->>F: 식자재별 실제 잔여 재고(remainingStock) 직접 입력
    F->>B: POST /closing/confirm {remainingStock}
    B->>B: actualUsage = openingStock - remainingStock
    B->>B: adjustmentAmount = actualUsage - orderDeductedAmount (보정값 = 이론·실제 차이)
    B->>DB: currentStock = remainingStock 저장 + closingDeductions 기록
    B-->>F: 마감 완료

    Note over U,F: 마감 취소 시
    U->>F: 마감 취소 클릭
    F->>B: POST /closing/cancel
    B->>DB: currentStock += adjustmentAmount (보정값만 복원, 주문 차감분은 유지)
    B-->>F: 취소 완료
```

</details>

<details>
<summary><b>JWT 인증 & 자동 갱신</b></summary>
<br/>

```mermaid
sequenceDiagram
    participant F as Frontend
    participant B as Backend

    F->>B: API 요청 (Authorization: Bearer accessToken)
    alt 토큰 유효
        B-->>F: 정상 응답
    else 401 Unauthorized
        F->>B: POST /auth/refresh (refreshToken)
        alt 갱신 성공
            B-->>F: 새 accessToken 발급
            F->>B: 원래 요청 재시도
        else 갱신 실패
            F->>F: 로그아웃 처리 → /login 리다이렉트
        end
    end
```

</details>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=BARO%20온보딩%20가이드&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

<img src="./assets/team-collaboration-strategy.png" width="100%" />

<br/>

### 개발 관련 가이드

<details>
<summary><b>작업 시작 전 필수 규칙</b></summary>
<br/>

1. **이슈 먼저** — 작업 전 반드시 GitHub 이슈를 생성하고, 이슈 번호를 브랜치명에 포함
2. **브랜치 필수** — 모든 작업은 작업 브랜치에서 진행, `main`·`develop` 직접 커밋 금지
3. **커밋 전 검사 필수** — 각 레포지토리의 README에서 확인

<br/>

> 레포별 개발 환경 설정 및 커밋 전 검사 방법은 각 README를 참고하세요.
>
> - 📄 [프론트엔드 기여 가이드](./baro-frontend/README.md#기여-가이드)
> - 📄 [백엔드 기여 가이드](./baro-backend/README.md#기여-가이드)

</details>

<details>
<summary><b>브랜치 전략</b></summary>
<br/>

```
작업 브랜치 → develop → release/vX.Y.Z → main
```

| 브랜치                | 역할                                      |
| --------------------- | ----------------------------------------- |
| `main`                | 프로덕션 배포 브랜치. 직접 커밋 금지      |
| `develop`             | 모든 기능·버그·리팩토링 PR의 대상 브랜치  |
| `feature/`, `fix/` 등 | 실제 작업 브랜치. `develop`에서 분기      |
| `release/vX.Y.Z`      | 배포 시 `develop`에서 분기, `main`으로 PR |

</details>

<details>
<summary><b>브랜치 네이밍</b></summary>
<br/>

- 형식: `작업유형/이슈번호-작업이름`

```bash
feature/15-qr-order-page      # 새 기능
fix/42-sse-reconnect           # 버그 수정
refactor/67-auth-store         # 리팩토링
style/71-dashboard-layout      # UI·스타일
config/80-vite-alias           # 설정·빌드·인프라
release/v0.2.0                 # 릴리즈 브랜치
```

</details>

<details>
<summary><b>이슈 생성</b></summary>
<br/>

- 이슈 생성 시 `.github/ISSUE_TEMPLATE/` 내 템플릿을 **반드시** 사용한다.

| 템플릿 파일   | gitmoji | 용도                              |
| ------------- | ------- | --------------------------------- |
| `feature.md`  | ✨      | 새로운 기능 제안                  |
| `bug.md`      | 🐛      | 버그 신고                         |
| `refactor.md` | ♻️      | 코드 개선·리팩토링                |
| `style.md`    | 🎨      | UI·디자인·CSS 변경                |
| `config.md`   | 🔧      | 설정·빌드·의존성·문서·인프라 작업 |
| `deploy.md`   | 🚀      | 배포 관련 작업                    |
| `thinking.md` | 💭      | 기술 결정 고민·구현 방향 논의     |

</details>

<details>
<summary><b>커밋 컨벤션</b></summary>
<br/>

- 형식: `[gitmoji] (#이슈번호) [태그]: [제목]`

```bash
✨ (#55) feat: 카카오 로그인 구현
🐛 (#61) fix: SSE 재연결 시 인증 토큰 누락 수정
💄 (#73) ui: 대시보드 카드 레이아웃 개선
♻️ (#80) refactor: axiosInstance 인터셉터 분리
📝 (#82) docs: OCR 처리 흐름 문서 추가
🔧 (#85) config: Vite path alias 설정 추가
```

| gitmoji | 태그       | 용도             |
| ------- | ---------- | ---------------- |
| ✨      | `feat`     | 새 기능          |
| 🐛      | `fix`      | 버그 수정        |
| 💄      | `ui`       | UI·스타일 수정   |
| ♻️      | `refactor` | 리팩토링         |
| 📝      | `docs`     | 문서 수정        |
| 🔧      | `config`   | 설정·빌드·인프라 |
| 🚀      | `deploy`   | 배포             |

</details>

<details>
<summary><b>PR 생성</b></summary>
<br/>

- PR 생성 시 `.github/PULL_REQUEST_TEMPLATE.md` 템플릿을 **반드시** 사용
- PR 제목에 연관 이슈 번호 포함
- PR 본문에 `Closes #이슈번호` 명시하여 이슈 자동 연결

```
PR 제목 예시:
✨ (#55) feat: 카카오 로그인 구현
🐛 (#61) fix: SSE 재연결 시 인증 토큰 누락 수정
```

</details>

<details>
<summary><b>배포 흐름</b></summary>
<br/>

```
develop ──→ release/vX.Y.Z ──→ main
```

1. 배포 이슈 생성 (`deploy.md` 템플릿 사용)
2. `develop`에서 `release/vX.Y.Z` 브랜치 분기
3. `release/vX.Y.Z` → `main` PR 생성 (배포 이슈 연결)
   ```
   🚀 (#56) deploy: v0.2.0 OCR 입고 처리 기능 배포
   ```
4. `main` 머지 후 GitHub Release 및 태그(`vX.Y.Z`) 생성

</details>

<details>
<summary><b>버전 관리 (Semantic Versioning)</b></summary>
<br/>

- 형식: `Major.Minor.Patch`

| 구분      | 올리는 시점                                                | 예시              |
| --------- | ---------------------------------------------------------- | ----------------- |
| **Major** | 하위 호환 안 되는 큰 변경 (UI 전면 개편, 서비스 구조 변경) | `1.0.0` → `2.0.0` |
| **Minor** | 하위 호환되는 기능 추가 (새 페이지, 새 기능)               | `0.1.0` → `0.2.0` |
| **Patch** | 버그 수정·소규모 개선                                      | `0.1.0` → `0.1.1` |

</details>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=디자인%20시스템&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

### 로고 (Logo)

| <img width="30%" alt="general logo" src="./assets/baro-logo.png" /> | <img width="70%" alt="app icon" src="./assets/baro-icon.png" /> |
| :-----------------------------------------------------------------: | :-------------------------------------------------------------: |
|                          **General Logo**                           |                          **App Icon**                           |

| <img width="55%" alt="simple logo" src="./assets/baro-simple-logo.png" /> | <img width="45%" alt="full logo" src="./assets/baro-full-logo.png" /> |
| :-----------------------------------------------------------------------: | :-------------------------------------------------------------------: |
|                              **Simple Logo**                              |                             **Full Logo**                             |

| <img width="50%" alt="kr text" src="./assets/baro-kr-text.png" /> | <img width="50%" alt="en text" src="./assets/baro-en-text.png" /> |
| :---------------------------------------------------------------: | :---------------------------------------------------------------: |
|                            **KR Text**                            |                            **EN Text**                            |

| <img width="100%" alt="logo concept" src="./assets/baro-logo-concept.png" /> |
| :--------------------------------------------------------------------------: |
|                               **Logo Concept**                               |

<br/>

### 디자인 토큰

<img width="100%" alt="" src="./assets/baro-design-token.png" />

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=지원%20창구&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

- [💬 BARO 버그 제보](https://github.com/orgs/from-knu-import-potato/discussions/190)
- [💭 BARO 기능 제안](https://github.com/orgs/from-knu-import-potato/discussions/248)
- [🙋🏻 BARO 1:1 문의 폼](https://form.naver.com/response/lKA7-JRIWJWq_xDIwmtdHg)
- [📧 BARO 문의 메일](dd22dd22.yy66yy66@gmail.com)
