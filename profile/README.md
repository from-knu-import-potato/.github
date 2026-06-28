## 주문부터 재고, 발주, 마감까지 — 소규모 카페·식당 사장님을 위한 올인원 플랫폼

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

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=왜%20BARO%20인가요%3F&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

<table border="0" width="100%">
  <tr>
    <td width="40"><kbd>B</kbd></td>
    <td width="100%"><b>Best Inventory</b> — 최적의 재고 상태 유지</td>
  </tr>
  <tr>
    <td width="40"><kbd>A</kbd></td>
    <td width="100%"><b>AI-Assistant</b> — AI를 통한</td>
  </tr>
  <tr>
    <td width="40"><kbd>R</kbd></td>
    <td width="100%"><b>Recommendation</b> — 맞춤형 발주 추천</td>
  </tr>
  <tr>
    <td width="40"><kbd>O</kbd></td>
    <td width="100%"><b>One-click Operation</b> — 주문부터 마감까지 모든 가게 운영을 한 번에</td>
  </tr>
</table>

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

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=배포%20환경&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

| 구분               | URL                                                     |
| ------------------ | ------------------------------------------------------- |
| 프론트엔드         | https://baro-web.vercel.app                             |
| 백엔드 API         | https://baro-backend-production-c908.up.railway.app/v1/ |
| API 문서 (Swagger) | https://baro-backend-production-c908.up.railway.app/doc |

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=설치%20및%20실행&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

<details>
<summary><b>사전 요구사항</b></summary>
<br/>

- Node.js >= 22
- pnpm >= 10
- PostgreSQL (또는 Supabase 프로젝트)

<br/>
</details>

<details>
<summary><b>프론트엔드</b></summary>
<br/>

```bash
git clone https://github.com/from-knu-import-potato/baro-frontend.git
cd baro-frontend
pnpm install
cp .env.example .env.local
# .env.local 환경 변수 설정 후 실행
pnpm dev
# http://localhost:5173
```

| 명령어          | 설명                             |
| --------------- | -------------------------------- |
| `pnpm dev`      | 개발 서버 실행 (Vite HMR)        |
| `pnpm build`    | TypeScript 검사 + 프로덕션 빌드  |
| `pnpm lint`     | ESLint 검사                      |
| `pnpm lint:fix` | ESLint 자동 수정 + Prettier 포맷 |
| `pnpm preview`  | 빌드 결과 미리보기               |

<br/>
</details>

<details>
<summary><b>백엔드</b></summary>
<br/>

```bash
git clone https://github.com/from-knu-import-potato/baro-backend.git
cd baro-backend
pnpm install
cp .env.example .env
# .env 환경 변수 설정 후 실행
pnpm db:migrate     # DB 마이그레이션 실행
pnpm dev
# http://localhost:3000
# Swagger UI: http://localhost:3000/doc
```

| 명령어             | 설명                                   |
| ------------------ | -------------------------------------- |
| `pnpm dev`         | 개발 서버 실행                         |
| `pnpm build`       | 프로덕션 빌드 (`dist/`)                |
| `pnpm db:generate` | 스키마 변경으로 마이그레이션 파일 생성 |
| `pnpm db:migrate`  | 마이그레이션 실행                      |
| `pnpm db:push`     | 스키마를 DB에 직접 반영                |
| `pnpm db:studio`   | Drizzle Studio (DB 웹 UI) 실행         |

<br/>
</details>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=환경%20변수&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

<details>
<summary><b>프론트엔드 (.env.local)</b></summary>
<br/>

```env
VITE_API_BASE_URL=http://localhost:3000/v1
```

<br/>
</details>

<details>
<summary><b>백엔드 (.env)</b></summary>
<br/>

```env
# 데이터베이스
DATABASE_URL=postgresql://user:password@db.supabase.co:5432/postgres

# JWT 시크릿
JWT_SECRET=your-access-token-secret
JWT_REFRESH_SECRET=your-refresh-token-secret

# Kakao OAuth
KAKAO_CLIENT_ID=your-kakao-app-key
KAKAO_CLIENT_SECRET=your-kakao-client-secret
KAKAO_REDIRECT_URI=http://localhost:3000/v1/auth/kakao/callback

# AI / OCR
GEMINI_API_KEY=your-google-gemini-api-key
CLOVA_OCR_API_URL=https://your-clova-ocr-endpoint
CLOVA_OCR_SECRET_KEY=your-clova-secret-key

# Supabase
SUPABASE_URL=https://your-project.supabase.co
SUPABASE_SERVICE_KEY=your-supabase-service-role-key

# 기타
FRONTEND_URL=http://localhost:5173
REGISTER_CODE=your-invite-code-for-local-testing
PORT=3000
```

> 각 키 발급처: [Kakao Developers](https://developers.kakao.com) · [Google AI Studio](https://aistudio.google.com) · [Naver CLOVA](https://clova.ai/ocr) · [Supabase](https://supabase.com)

<br/>
</details>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=API%20문서&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

Swagger UI를 통해 전체 API를 인터랙티브하게 확인할 수 있습니다.

| 환경     | URL                                                     |
| -------- | ------------------------------------------------------- |
| 로컬     | http://localhost:3000/doc                               |
| 프로덕션 | https://baro-backend-production-c908.up.railway.app/doc |

<details>
<summary><b>엔드포인트 목록</b></summary>
<br/>

| 도메인          | 메서드 | 경로                                 | 설명                          | 인증 |
| --------------- | ------ | ------------------------------------ | ----------------------------- | ---- |
| **Auth**        | GET    | `/auth/kakao`                        | 카카오 OAuth 로그인           | ❌   |
|                 | POST   | `/auth/refresh`                      | 토큰 갱신                     | ❌   |
|                 | POST   | `/auth/logout`                       | 로그아웃                      | ✅   |
| **Users**       | GET    | `/users/me`                          | 내 정보 조회                  | ✅   |
|                 | GET    | `/users/me/stores`                   | 내 가게 목록                  | ✅   |
| **Stores**      | POST   | `/stores/setup`                      | 가게 초기 세팅                | ✅   |
|                 | GET    | `/stores/:id`                        | 가게 정보 조회                | ✅   |
|                 | PATCH  | `/stores/:id`                        | 가게 정보 수정                | ✅   |
|                 | POST   | `/stores/:id/invite-code`            | 초대 코드 재발급              | ✅   |
|                 | DELETE | `/stores/:id`                        | 가게 삭제                     | ✅   |
| **Orders**      | POST   | `/stores/:id/orders`                 | 주문 생성 (손님, 인증 불필요) | ❌   |
|                 | GET    | `/stores/:id/orders`                 | 주문 목록 조회                | ✅   |
|                 | PATCH  | `/stores/:id/orders/:orderId/status` | 주문 상태 변경                | ✅   |
|                 | GET    | `/stores/:id/orders/stream`          | SSE 실시간 스트림             | ✅   |
| **Menus**       | GET    | `/stores/:id/menus`                  | 메뉴 목록                     | ✅   |
|                 | POST   | `/stores/:id/menus`                  | 메뉴 생성                     | ✅   |
|                 | POST   | `/stores/:id/menus/ocr-scan`         | AI 메뉴 스캔                  | ✅   |
| **Ingredients** | GET    | `/stores/:id/ingredients`            | 재고 목록                     | ✅   |
|                 | POST   | `/stores/:id/ingredients/inbound`    | 입고 등록                     | ✅   |
| **Closing**     | GET    | `/stores/:id/closing/preview`        | 마감 미리보기                 | ✅   |
|                 | POST   | `/stores/:id/closing`                | 마감 확정                     | ✅   |
|                 | DELETE | `/stores/:id/closing/:closingId`     | 마감 취소                     | ✅   |
| **OCR**         | POST   | `/stores/:id/ocr/upload`             | 거래명세서 OCR 처리           | ✅   |
| **Order Guide** | GET    | `/stores/:id/order-guide`            | 발주 가이드 조회              | ✅   |
|                 | POST   | `/stores/:id/order-guide/generate`   | 발주 가이드 생성              | ✅   |
| **Dashboard**   | GET    | `/stores/:id/dashboard/stats`        | 대시보드 통계                 | ✅   |
|                 | GET    | `/stores/:id/dashboard/sales`        | 12개월 매출                   | ✅   |

<br/>
</details>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=테스트%20가이드&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

- 테스트 가이드에 대한 문서는 추가 예정입니다.

```
ID: [테스트 계정 ID]
PW: [테스트 계정 PW]
```

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=프로젝트%20소개&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

**BARO(바로)** 는 강원도 소규모 카페·식당 사장님을 위한 **OCR·AI 기반 올인원 가게 운영 SaaS**입니다.

거래명세서를 카메라로 찍으면 AI가 자동으로 재고를 입고하고, 누적된 소비 데이터를 분석해 적정 발주량을 추천합니다. 손님은 QR 코드로 직접 주문하고, 사장님은 하루 영업이 끝나면 한 번의 마감으로 재고를 자동 정산합니다.

**주문 · 재고 · 발주 · 마감** — 혼자서 모든 걸 처리해야 하는 소상공인의 하루를 BARO 하나로 끝냅니다.

<br/>

<details>
<summary><b>배경 — 강원도 소상공인 문제</b></summary>
<br/>

강원도는 전국 평균 대비 소규모 음식점과 개인 사업장의 비중이 높고, 그만큼 폐업률도 높은 지역입니다. 외식업 운영비에서 식자재 비용이 차지하는 비율은 평균 30~40%에 달하며, 이를 얼마나 효율적으로 관리하느냐가 사업 존속에 직결됩니다.

그러나 소규모 매장의 사장님들은 주문·재고·발주·마감을 **대부분 혼자, 수작업으로** 처리하고 있습니다. BARO는 이 구조적 비효율을 해결하여 강원도 소상공인의 운영 부담을 낮추고 폐업률을 줄이는 것을 목표로 합니다.

</details>

<details>
<summary><b>해결하려는 문제</b></summary>
<br/>

**수작업 중심의 재고 관리**

기존 재고 관리는 품목을 하나씩 직접 등록하고 수기로 관리해야 합니다. 매입 거래명세서도 직접 전사(轉寫)해야 하므로 점주의 업무 부담이 크고, 반복적인 입력 업무로 시간과 인력이 낭비됩니다.

<br/>

**경험과 감에만 의존하는 발주**

재고 현황과 소비 데이터를 체계적으로 분석하지 못해 점주의 경험과 직감에만 의존해 발주를 결정합니다. 그 결과 과잉 재고·품절·폐기가 반복되고, 원가 상승과 매출 손실로 이어집니다.

<br/>

**소규모 매장에 맞지 않는 기존 시스템**

시중의 재고 관리 프로그램은 기능이 복잡하고 사용성이 낮아 소규모 매장에서 실제로 활용하기 어렵습니다. 특히 강원도처럼 점주가 홀로 재고·발주·주문을 모두 담당하는 환경에서는 도입 자체가 부담입니다.

</details>

<details>
<summary><b>BARO의 접근</b></summary>
<br/>

| 문제                      | BARO의 해결                                                       |
| ------------------------- | ----------------------------------------------------------------- |
| 거래명세서 수기 전사      | OCR 촬영 → Naver CLOVA + Gemini AI 자동 파싱 → 검수 후 1클릭 입고 |
| 감에 의존한 발주          | 재고·소비 데이터 분석 → AI 발주량 추천 + 서술형 이유 제공         |
| 구두·메모 주문, 누락 발생 | 테이블 QR → 손님 직접 주문 → 사장님 화면 실시간 수신              |
| 수기 마감 정산            | 레시피 기반 자동 차감 계산 → 사장님 검토 후 확정                  |
| 복잡한 기존 시스템        | 소규모 매장에 최적화된 직관적 UI, 과도한 기능 없음                |

> **주문 · 재고 · 발주 · 마감** — 소상공인을 위한 4가지 핵심 업무를 하나의 플랫폼으로

</details>

<details>
<summary><b>사용자 정의</b></summary>
<br/>

| 사용자             | 설명                                                    | 접근 방식                              |
| ------------------ | ------------------------------------------------------- | -------------------------------------- |
| **사장님 (Owner)** | 서비스 주 사용자. 주문 수락, 재고 관리, 발주, 마감 수행 | 카카오 소셜 로그인 후 대시보드 접근    |
| **손님 (Guest)**   | 비회원. 별도 로그인 없이 주문만 가능                    | 테이블 QR 스캔 → 주문 페이지 바로 접근 |

</details>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=주요%20화면&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

| 화면                                                    | 설명                                                |
| ------------------------------------------------------- | --------------------------------------------------- |
| ![랜딩](./docs/images/screenshot-landing.png)           | **랜딩 페이지** — 서비스 소개 및 로그인 진입        |
| ![대시보드](./docs/images/screenshot-dashboard.png)     | **대시보드** — 실시간 주문 수신, 재고·매출 현황     |
| ![QR주문](./docs/images/screenshot-order.png)           | **손님 주문 페이지** — QR 스캔 후 메뉴 선택·주문    |
| ![OCR](./docs/images/screenshot-ocr.png)                | **OCR 입고 처리** — 거래명세서 촬영 → 자동 디지털화 |
| ![발주가이드](./docs/images/screenshot-order-guide.png) | **AI 발주 가이드** — AI 기반 발주량 추천            |
| ![마감](./docs/images/screenshot-closing.png)           | **마감하기** — 레시피 기반 재고 자동 차감           |
| ![재고](./docs/images/screenshot-inventory.png)         | **재고 현황** — 전체 재고 상태 및 안전재고 경고     |
| ![설정](./docs/images/screenshot-settings.png)          | **가게 설정** — 메뉴·레시피·테이블·테마 관리        |

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=주요%20기능&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

| #   | 기능                     | 설명                                                                                                                                                 | 관련 기술                     |
| --- | ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- |
| 1   | **QR 기반 비대면 주문**  | 테이블 QR 스캔 → 손님 주문 → SSE 실시간 수신                                                                                                         | SSE, React Query              |
| 2   | **OCR 자동 입고 처리**   | 거래명세서 촬영 → CLOVA OCR 텍스트 추출 → Gemini 2.5 Flash 구조화 파싱 → 경고 검증 → 수동 검수 확정                                                  | Naver CLOVA, Gemini 2.5 Flash |
| 3   | **AI 발주 가이드**       | 6가지 트리거 필터링 → Gemini 2.5 Flash 발주량·추천 이유 생성 → 서버사이드 긴급도 계산(critical/warning/expiry) → BOX·BTL 단위 역산 표시              | Google Gemini                 |
| 4   | **마감하기**             | 주문 수락 시 즉시 재고 차감 → 마감 시 이론값(orderDeductedAmount)과 실측값(remainingStock) 비교 → 보정값(adjustmentAmount) 기록·확정. 소급 마감 지원 | Recipe 기반 하이브리드 차감   |
| 5   | **통합 대시보드**        | 실시간 주문·재고·매출 현황 한 화면에서 관리                                                                                                          | SSE, React Query              |
| 6   | **카카오 소셜 로그인**   | 카카오 OAuth 2.0 → JWT 발급 (Access 15분 / Refresh 7일)                                                                                              | Kakao OAuth, JWT              |
| 7   | **메뉴·레시피 관리**     | 메뉴 이미지 업로드, Gemini AI 메뉴 스캔, 레시피 재료 매핑                                                                                            | Supabase Storage, Gemini      |
| 8   | **안전재고 경고 시스템** | 안전재고 비율 설정 → 상태별 경고 (normal/warning/critical/depleted)                                                                                  | 재고 계산 로직                |
| 9   | **멀티 스토어**          | 초대 코드로 매장 참여, Owner/Staff 역할별 권한 관리                                                                                                  | JWT, Role-based Auth          |
| 10  | **가게 테마 커스텀**     | 손님 주문 페이지 색상·레이아웃·배너 이미지 설정                                                                                                      | Supabase Storage              |

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=사용%20가이드&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

<details>
<summary><b>역할별 권한</b></summary>
<br/>

| 기능               | Owner | Staff | Guest |
| ------------------ | :---: | :---: | :---: |
| 대시보드 조회      |  ✅   |  ✅   |  ❌   |
| 실시간 주문 수신   |  ✅   |  ✅   |  ❌   |
| 주문 상태 변경     |  ✅   |  ✅   |  ❌   |
| 재고 조회·관리     |  ✅   |  ✅   |  ❌   |
| OCR 입고 처리      |  ✅   |  ✅   |  ❌   |
| 마감하기           |  ✅   |  ✅   |  ❌   |
| 메뉴·레시피 설정   |  ✅   |  ❌   |  ❌   |
| 멤버 관리          |  ✅   |  ❌   |  ❌   |
| 가게 설정·삭제     |  ✅   |  ❌   |  ❌   |
| QR 주문 (비로그인) |  ❌   |  ❌   |  ✅   |

<br/>
</details>

<details>
<summary><b>최초 가입 & 가게 세팅</b></summary>
<br/>

```
카카오 로그인
→ 초기 세팅 위저드 진입
→ 가게 기본 정보 입력 (이름, 업종, 카테고리)
→ 영업 시간 설정
→ 메뉴 등록 (이미지 업로드 또는 AI 스캔)
→ 식자재 등록 (이름, 단위, 초기 재고)
→ 레시피 설정 (메뉴 ↔ 식자재 매핑)
→ 안전재고 비율 설정 → 완료
```

<br/>
</details>

<details>
<summary><b>하루 영업 사이클</b></summary>
<br/>

```
개점하기 (영업일 시작)
→ 대시보드에서 실시간 주문 수신
→ 주문 확인 후 상태 변경 (대기 → 준비 중 → 완료)
→ 마감하기 (판매 메뉴 확인 → 재고 차감 미리보기 → 잔여재고 입력 → 확정)
→ AI 발주 가이드 확인 (재고 부족 품목 추천)
```

<br/>
</details>

<details>
<summary><b>OCR 입고 처리</b></summary>
<br/>

```
OCR 입고 페이지 → 거래명세서 촬영·업로드
→ CLOVA OCR + Gemini AI 자동 파싱
→ 검수 화면에서 품목·수량·단가 확인 및 수정
→ 기존 식자재와 매핑 → 입고 확정
→ 재고 자동 업데이트
```

<br/>
</details>

<details>
<summary><b>손님 QR 주문</b></summary>
<br/>

```
테이블 QR 코드 스캔 → 메뉴판 페이지 접속 (로그인 불필요)
→ 메뉴 선택 → 수량 조절 → 주문하기
→ 사장님 화면에 실시간으로 주문 수신
```

<br/>
</details>

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
    B->>B: adjustStockForOrder() — preparing 전환 시 레시피 기반 즉시 재고 차감
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

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=개발%20기술%20스택&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

<details>
<summary><b>프론트엔드</b></summary>
<br/>

| 기술                      | 버전 | 선택 이유                                                         |
| ------------------------- | ---- | ----------------------------------------------------------------- |
| **React**                 | 19   | 최신 Concurrent 기능, 안정적인 생태계                             |
| **TypeScript**            | ~6.0 | 컴파일 타임 타입 안전성, 런타임 오류 사전 차단                    |
| **Vite**                  | 8.0  | 빠른 HMR, ESM 기반 빌드로 개발 생산성 극대화                      |
| **Tailwind CSS**          | 4.2  | 유틸리티 클래스 기반으로 디자인 일관성 유지, 별도 CSS 파일 불필요 |
| **Shadcn/UI**             | -    | 접근성(a11y) 준수 컴포넌트 + 커스터마이징 완전 자유               |
| **Zustand**               | 5.0  | 서버 상태와 분리된 경량 전역 UI 상태 관리, 보일러플레이트 최소화  |
| **React Query**           | 5.x  | 서버 상태 캐싱·동기화·백그라운드 refetch 자동화                   |
| **React Hook Form + Zod** | -    | 타입 안전 폼 검증, 서버 에러를 필드 단위로 바인딩                 |
| **Axios**                 | 1.16 | 인터셉터 기반 전역 인증·에러 처리 용이                            |

</details>

<details>
<summary><b>백엔드</b></summary>
<br/>

| 기술            | 버전 | 선택 이유                                                              |
| --------------- | ---- | ---------------------------------------------------------------------- |
| **Hono**        | 4.12 | 초경량 Node.js 프레임워크, OpenAPI/Swagger 내장, Railway 배포 최적     |
| **Node.js**     | 22   | JavaScript 풀스택 일관성, 비동기 I/O 최적화                            |
| **TypeScript**  | 5.8  | 엔드투엔드 타입 안전성 (프론트·백 타입 공유 가능)                      |
| **Drizzle ORM** | 0.45 | 타입 안전 쿼리 빌더, Prisma 대비 경량·빠른 마이그레이션, Supabase 호환 |
| **jose (JWT)**  | 6.2  | Web Crypto API 기반 표준 JWT, 엣지 환경 완전 호환                      |
| **Zod**         | 4.4  | 런타임 스키마 검증 + OpenAPI 문서 자동 생성 (hono/zod-openapi)         |

</details>

<details>
<summary><b>외부 서비스</b></summary>
<br/>

| 서비스                | 용도               | 선택 이유                                                         |
| --------------------- | ------------------ | ----------------------------------------------------------------- |
| **Kakao OAuth 2.0**   | 소셜 로그인        | 국내 소상공인 타겟 서비스 특성상 가장 높은 접근성                 |
| **Naver CLOVA OCR**   | 거래명세서 인식    | 한국어 특화, 표 구조 인식 정확도가 Google Vision 대비 우수        |
| **Google Gemini API** | AI 파싱·분석·추천  | 멀티모달 지원, 긴 컨텍스트 처리, 비용 대비 성능 우수              |
| **Supabase**          | DB + 파일 스토리지 | PostgreSQL + S3 호환 스토리지 + 관리 UI를 단일 플랫폼에서 제공    |
| **Vercel**            | 프론트엔드 배포    | React SPA 최적 CDN 배포, GitHub 연동 자동 배포                    |
| **Railway**           | 백엔드 배포        | Node.js 서버 간단 배포, Nixpacks 빌드 자동화, 환경 변수 관리 편의 |

</details>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=폴더%20구조&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

<details>
<summary><b>프론트엔드 (baro-frontend/)</b></summary>
<br/>

```
src/
├─ app/                   # 레이아웃, 라우팅, AppInitializer
├─ features/              # 도메인별 기능 모듈
│  ├─ auth/               # 로그인, 카카오 OAuth, JWT
│  │  ├─ api/
│  │  ├─ components/
│  │  ├─ hooks/
│  │  ├─ store/           # Zustand 인증 스토어
│  │  └─ types/
│  ├─ dashboard/          # 대시보드, SSE 실시간 주문
│  ├─ customer-order/     # 손님 주문 (QR)
│  ├─ inventory/          # 재고 현황
│  ├─ ocr-inbound/        # OCR 입고 처리
│  ├─ order-guide/        # AI 발주 가이드
│  ├─ closing/            # 마감하기
│  ├─ store-settings/     # 가게 설정 (메뉴·레시피·테이블·테마)
│  ├─ initial-setup/      # 초기 세팅 위저드
│  ├─ notification/       # 알림
│  └─ landing/            # 랜딩 페이지
├─ pages/                 # 라우팅 페이지 (features 조합만)
├─ widgets/               # 2개 이상 페이지 공용 UI
├─ shadcn/                # Shadcn 컴포넌트 (수정 금지)
└─ shared/
   ├─ api/                # Axios 인스턴스, 인터셉터
   ├─ components/         # 공용 UI 컴포넌트
   ├─ hooks/              # 공용 훅
   ├─ store/              # 전역 Zustand 스토어
   ├─ utils/              # businessDate, apiError 등
   ├─ constants/
   ├─ types/
   └─ design-token/       # colors.css, spacing.css, typography.css
```

<br/>
</details>

<details>
<summary><b>백엔드 (baro-backend/)</b></summary>
<br/>

```
src/
├─ index.ts               # 진입점, 라우터 등록, OpenAPI 설정, CORS
├─ routes/                # 도메인별 라우터
│  ├─ auth.ts             # OAuth, JWT 로그인·갱신·로그아웃
│  ├─ stores.ts           # 가게 CRUD, 멤버, 초대 코드
│  ├─ menus.ts            # 메뉴 CRUD, 이미지 업로드, AI 스캔
│  ├─ menu-categories.ts  # 메뉴 카테고리 관리
│  ├─ ingredients.ts      # 재고·입고 기록
│  ├─ recipes.ts          # 레시피 (메뉴-재료 매핑)
│  ├─ orders.ts           # 주문 CRUD, SSE 스트림
│  ├─ ocr.ts              # 거래명세서 OCR 처리
│  ├─ order-guide.ts      # AI 발주 가이드 생성
│  ├─ closing.ts          # 마감 (미리보기·확정·취소)
│  ├─ dashboard.ts        # 통계·매출 데이터
│  ├─ theme.ts            # 가게 테마 설정
│  └─ open.ts             # 영업 개점·상태 확인
├─ middleware/
│  └─ auth.ts             # JWT 검증 미들웨어
├─ db/
│  ├─ schema.ts           # Drizzle 테이블 정의 (18개 테이블)
│  └─ index.ts            # DB 클라이언트 초기화
└─ lib/
   ├─ jwt.ts              # 토큰 생성·검증
   ├─ sse.ts              # SSE 클라이언트 관리·브로드캐스트
   ├─ supabase.ts         # Supabase 클라이언트
   └─ kst.ts              # KST 타임존 유틸리티
```

<br/>
</details>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=설계%20고민%20과정&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

<details>
<summary><b>1. 실시간 통신: WebSocket vs SSE</b></summary>
<br/>

**상황**: 손님이 주문하면 사장님 화면에 실시간으로 주문이 표시되어야 함

|               | WebSocket             | SSE                      |
| ------------- | --------------------- | ------------------------ |
| 통신 방향     | 양방향                | 서버 → 클라이언트 단방향 |
| 구현 복잡도   | 높음 (연결 관리 복잡) | 낮음 (HTTP 기반)         |
| Railway 호환  | 별도 설정 필요        | HTTP 그대로 사용         |
| 우리 요구사항 | 과도한 스펙           | 주문 수신만 필요         |

**결정**: 주문 수신은 서버→클라이언트 단방향으로 충분하고, Railway 환경에서 HTTP 기반 SSE가 더 안정적이므로 **SSE 선택**

</details>

<details>
<summary><b>2. SSE 구현: EventSource API vs 커스텀 fetch</b></summary>
<br/>

**상황**: SSE 연결 시 JWT 인증 헤더를 함께 보내야 함

브라우저 내장 `EventSource`는 커스텀 HTTP 헤더를 설정할 수 없는 구조적 한계가 있음.

**결정**: `fetch()` API로 SSE 스트림을 직접 파싱하는 **커스텀 SSE 클라이언트 구현**

```ts
// event: 와 data: 라인을 직접 파싱
const response = await fetch(url, {
  headers: { Authorization: `Bearer ${token}` },
});
// ReadableStream으로 청크 단위 처리
```

</details>

<details>
<summary><b>3. 상태 관리: React Query + Zustand 역할 분리</b></summary>
<br/>

**고민**: 전역 상태를 하나의 라이브러리로 통합할지, 역할에 따라 분리할지

| 상태 종류                 | 담당 라이브러리 | 예시                              |
| ------------------------- | --------------- | --------------------------------- |
| 서버 데이터 (캐싱·동기화) | React Query     | 주문 목록, 재고 현황, 마감 데이터 |
| 클라이언트 UI 상태        | Zustand         | 인증 토큰, 영업일 상태, 재고 경고 |
| 폼 상태                   | React Hook Form | 로그인 폼, 메뉴 등록 폼           |

**결정**: 서버 상태와 UI 상태의 관심사를 명확히 분리하여 **React Query + Zustand 병행 사용**

</details>

<details>
<summary><b>4. ORM: Prisma vs Drizzle</b></summary>
<br/>

|               | Prisma             | Drizzle          |
| ------------- | ------------------ | ---------------- |
| 번들 사이즈   | 큼 (바이너리 포함) | 경량             |
| 타입 안전성   | 우수               | 우수             |
| 엣지 환경     | 제약 있음          | 완전 지원        |
| 마이그레이션  | 자동화 우수        | 코드로 직접 관리 |
| Supabase 연동 | 별도 설정 필요     | 직접 연결        |

**결정**: Railway·Supabase 환경에서 경량으로 동작하고 타입 안전성도 보장되는 **Drizzle 선택**

</details>

<details>
<summary><b>5. OCR 결과 자동 확정 vs 수동 검수 유지</b></summary>
<br/>

**상황**: OCR + AI 파싱 결과를 자동으로 재고에 반영할지, 사람이 검토 후 확정할지

OCR 인식 오류, AI 파싱 실패, 비표준 단위 등 다양한 예외 상황이 발생할 수 있음. 잘못된 데이터가 자동 반영되면 발주·마감 전체에 영향을 미침.

**결정**: OCR 결과는 반드시 **사용자가 검수 화면에서 직접 확인 후 확정**. 자동 확정 로직은 구현하지 않음.

</details>

<details>
<summary><b>6. JWT 저장 위치: localStorage vs httpOnly 쿠키</b></summary>
<br/>

|             | localStorage | httpOnly 쿠키              |
| ----------- | ------------ | -------------------------- |
| XSS 취약성  | 취약         | 안전                       |
| 구현 복잡도 | 낮음         | 높음 (CORS, SameSite 설정) |
| 현재 단계   | 적용 중      | 마이그레이션 예정          |

**결정**: 개발 속도를 위해 현재는 **localStorage 사용**, 코드에 `// TODO: httpOnly 쿠키로 마이그레이션` 주석 명시. 프로덕션 보안 강화 시 마이그레이션 예정.

</details>

<details>
<summary><b>7. businessDate 개념 설계</b></summary>
<br/>

**상황**: 심야 영업 카페의 경우 자정이 넘어도 마감 전까지는 같은 영업일로 처리해야 함

단순 `new Date()`로 날짜를 판단하면 자정 이후 주문이 다음 날로 분류되어 마감 데이터 불일치 발생.

**결정**: 가게 개점(`POST /open`) 시 `businessDate`를 별도로 기록하고, 마감 전까지의 모든 주문을 해당 `businessDate`에 귀속. KST 타임존 유틸리티(`kst.ts`) 별도 구현.

</details>

<details>
<summary><b>8. 재고 차감 시점: 주문 수락 시 vs 마감 확정 시</b></summary>
<br/>

**고민**: 재고를 언제 차감할 것인가. 주문이 들어오는 순간 즉시 차감하면 재고 현황이 실시간으로 반영되지만, 취소된 주문까지 차감되는 문제가 생김. 반대로 마감 때만 차감하면 영업 중 재고 현황이 부정확함.

| 방식              | 장점                 | 단점                     |
| ----------------- | -------------------- | ------------------------ |
| 주문 즉시 차감    | 실시간 재고 반영     | 취소 주문 복원 로직 복잡 |
| 마감 시 일괄 차감 | 확정된 데이터만 반영 | 영업 중 재고 현황 부정확 |

**결정**: 두 방식을 결합한 **하이브리드 방식** 채택

- **주문 수락(`preparing`) 시점**: `adjustStockForOrder()`로 레시피 기반 재고 **즉시 차감** → 영업 중 실시간 재고 현황 반영
- **취소 시**: 차감분 즉시 복원 (`sign = -1`) → `cancelled` 주문은 자동으로 재고에서 제외
- **마감 시**: `orderDeductedAmount`(preparing+completed 레시피 합산)와 사장님이 직접 확인한 `remainingStock`의 차이를 `adjustmentAmount`(보정값)로 적용 → 이론과 실제 사용량의 괴리를 명시적으로 기록

</details>

<details>
<summary><b>9. 이론 사용량 vs 실제 사용량 괴리 처리</b></summary>
<br/>

**고민**: 레시피에 등록된 이론 사용량(예: 라떼 1잔 = 우유 200ml)과 실제 사용량은 항상 다름. 시식, 음식 낭비, 레시피 오차, 직원 실수 등이 발생하면 레시피 계산만으로 정확한 재고 파악이 불가능함.

**결정**: 마감 시 두 단계로 처리

```
orderDeductedAmount  = 주문 수락분 기반 레시피 이론 차감량 (시스템 계산)
remainingStock       = 사장님이 직접 확인해 입력한 실제 잔여 재고
─────────────────────────────────────────────────────────────
actualUsage          = openingStock - remainingStock (실제 총 사용량)
adjustmentAmount     = actualUsage - orderDeductedAmount (보정값 = 이론과 실제의 차이)
```

시스템이 계산한 이론값과 사장님이 직접 확인한 실측값의 차이를 `adjustmentAmount`로 명시적으로 기록. 마감 취소 시에는 이 **보정값(adjustmentAmount)만 복원**하고, 주문 기반 차감분은 유지하여 데이터 정합성 보장.

</details>

<details>
<summary><b>10. 재고 단위 3종 고정 (g / ml / 개)</b></summary>
<br/>

**고민**: 식자재 단위를 자유 입력으로 할지, 고정 단위로 제한할지

자유 입력을 허용하면 `500g`, `0.5kg`, `반 봉지` 등 단위가 혼재되어 재고 비교·계산이 불가능해짐. 특히 OCR 파싱 결과와 레시피 단위를 맞춰야 하는 구조에서는 표준화가 필수.

**결정**: 모든 재고는 `g`, `ml`, `개` 3종으로만 저장. 외부에서 들어오는 `kg → g(×1000)`, `L → ml(×1000)` 변환은 프론트엔드에서 처리 후 서버에 표준 단위로 전송. 단위 고정으로 레시피 계산, 마감 차감, 안전재고 비교가 모두 단일 기준에서 동작.

</details>

<details>
<summary><b>11. 포장단위·입고단위·사용단위 불일치 해결</b></summary>
<br/>

**고민**: 공급사는 `BOX`·`BTL`·`봉` 단위로 납품하고, 레시피는 `g`·`ml` 단위를 쓰며, 사장님이 발주할 때는 다시 `BOX` 단위로 주문함. 세 단위가 모두 달라 단순 숫자 비교가 불가능.

**결정**: 3단계 변환 체계 설계

```
입고 단위 (BOX, BTL...)
    ↓ conversionFactor (사용자 입력 또는 spec 자동 파싱)
재고 단위 (g, ml, 개)  ← DB 저장 기준, 레시피·마감 계산에 사용
    ↓ purchaseConversions (저장된 변환 계수 역산)
발주 단위 (BOX, BTL...)  ← 발주 가이드에서 사장님이 실제 주문할 수량
```

한 번 입력한 변환 계수는 `ingredientUnitConversions` 테이블에 저장되어, **같은 식자재가 같은 단위로 재입고될 때 자동 적용**. 발주 가이드에서는 `recommendedOrderAmount`(g/ml 기준)를 저장된 변환 계수로 역산해 실제 주문 수량(BOX 단위)을 함께 표시.

</details>

<details>
<summary><b>12. 다양한 명세서 포맷 수용 전략</b></summary>
<br/>

**고민**: 공급사마다 거래명세서 양식이 다름. 품목명·수량·단가·단위 열의 위치가 다르고, 같은 정보가 `"3통"`, `"3 BOX"`, 또는 품목명 뒤 괄호 `"(1L×12)"` 등 다양한 방식으로 표기됨.

**결정**: 규칙 기반 파서 대신 **LLM 파싱 채택**

- Naver CLOVA OCR로 텍스트 추출 → Google Gemini 2.5 Flash로 구조화 파싱
- 단, AI 출력의 일관성을 위해 상세 규칙을 프롬프트에 명문화 (`temperature=0`):
  - 단위 추출 우선순위 (별도 열 > 품목명 내 괄호 > 없으면 EA)
  - 포장 단위(BOX, BTL…) vs 자동 변환 단위(KG, L…) 판별 규칙
  - `spec` 필드로 내용물 정보 분리 (`"박스/20개"` → `spec: "20개"`)
  - 식자재 목록은 ID 매핑 참고용으로만 제공, 이름 교정에 사용 금지
- 거래명세서가 아닌 이미지는 `isInvoice: false`로 즉시 거부 (422 반환)

</details>

<details>
<summary><b>13. 발주 가이드 생성 시점 및 트리거 기준</b></summary>
<br/>

**고민**: 발주 가이드를 언제 생성할 것인가. 마감 직후 자동 생성하면 편리하지만, 사장님이 원하는 시점에 최신 데이터로 다시 생성하고 싶을 수도 있음. 발주 필요 기준도 단순 안전재고 미달만으로는 부족함.

**결정**: 온디맨드(on-demand) 생성으로 설계. 사장님이 원하는 시점에 생성 요청하면 그 시점의 최신 재고·소비 데이터로 분석.

발주 필요 식자재 필터링 기준을 **6가지 트리거**로 세분화:

| 트리거               | 기준                                                            |
| -------------------- | --------------------------------------------------------------- |
| 안전재고 미달        | `currentStock < safetyStock`                                    |
| 유통기한 임박        | 최근 입고분 유통기한 5일 이내                                   |
| 소진 3일 이내        | 14일 평균 소비 기준 3일 안에 소진 예상                          |
| **선제 발주**        | 현재는 안전 수준이나 7일 내 안전재고 미달 예상                  |
| **소비 가속**        | 최근 3일 평균이 14일 평균 대비 50% 이상 급증 + 7일 내 소진 예상 |
| **재발주 주기 초과** | 마지막 입고 후 경과일이 평균 입고 주기의 1.2배 초과             |

</details>

<details>
<summary><b>14. 발주 AI 프롬프트 설계 — 컨텍스트와 폴백</b></summary>
<br/>

**고민**: AI에게 어떤 데이터를 넘길 것인가. 숫자만 주면 현황 설명은 가능하지만 요일·계절 패턴 반영이 안 됨. 너무 많은 데이터를 주면 프롬프트가 비대해지고 응답 품질이 떨어짐.

**결정**: 식자재별 컨텍스트 블록 + 매장 전체 패턴 데이터를 구조화해 전달

```
식자재 컨텍스트:
  - 발주 트리거 (왜 이 식자재가 선택됐는지 명시)
  - 14일 일평균 소비량 + 최근 3일 일평균 (소비 추세 비교)
  - 예상 소진일 (두 기준 각각)
  - 유통기한, 마지막 입고일 + 평균 입고 주기
  - 연관 메뉴명 (레시피 기반)

매장 전체 컨텍스트:
  - 최근 7일 일평균 매출
  - 요일별 평균 매출 패턴 (최근 8주)
  - 내일 요일의 평균 대비 매출 예측 비율
```

추천량 계산식: `max(14일 평균, 최근 3일 평균) × 7일치`, 내일이 성수기 요일이면 +20% 버퍼 추가.

AI 응답 파싱 실패 또는 503 에러 시 **룰 기반 폴백 자동 실행** — 서비스 가용성 보장.

</details>

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=직면했던%20문제점%20/%20해결%20과정&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

<details>
<summary><b>1. SSE 연결 시 인증 헤더 전달 불가</b></summary>
<br/>

**문제**: 브라우저 내장 `EventSource`는 `Authorization` 헤더를 설정할 수 없어 인증된 SSE 연결이 불가능했음

**해결**: `fetch()` API와 `ReadableStream`을 활용해 커스텀 SSE 파서를 직접 구현. `event:` 와 `data:` 라인을 수동으로 파싱하여 이벤트를 처리하고, 연결 끊김 시 3초 후 자동 재연결 로직을 추가.

```ts
const response = await fetch(url, {
  headers: { Authorization: `Bearer ${token}` },
});
// ReadableStream으로 청크 단위 처리, event:/data: 라인 직접 파싱
```

</details>

<details>
<summary><b>2. OCR 비표준 단위 처리</b></summary>
<br/>

**문제**: 공급사마다 `BOX`, `BTL`, `봉`, `팩` 등 포장 단위를 사용해 내용물 기준 단위(`g`/`ml`/`개`)로 자동 변환이 불가능한 경우가 많았음

**해결**: 3단계 처리 전략 도입

1. **Gemini가 `spec` 필드로 내용물 정보 추출** — 예) `"박스/20개"` → `spec: "20개"`
2. **프론트엔드 `parseSpec()`으로 자동 변환 시도** — `spec` 문자열에서 숫자+단위 파싱, `L→ml(×1000)`, `kg→g(×1000)` 자동 변환
3. **변환 불가 시 `amount=null`로 처리** → 검수 화면에서 사용자가 변환 계수 직접 입력. 입력한 계수는 `ingredientUnitConversions` 테이블에 저장되어 동일 식자재·단위 재입고 시 자동 적용

</details>

<details>
<summary><b>3. businessDate 자정 경계 문제</b></summary>
<br/>

**문제**: 심야 영업 시 자정 이후 주문이 다음 날짜로 분류되어 마감 데이터 불일치 발생

**해결**: 가게 개점(`POST /open`) 시 `businessDate`를 별도 컬럼으로 기록하고, 마감 전까지의 모든 트랜잭션을 해당 날짜에 귀속. KST 기준 날짜 계산 유틸리티(`kst.ts`)를 분리하여 일관된 시간대 처리.

</details>

<details>
<summary><b>4. SSE 이벤트 수신 후 React Query 캐시 무효화 타이밍</b></summary>
<br/>

**문제**: SSE로 새 주문 이벤트를 수신해도 화면의 주문 목록이 즉시 업데이트되지 않는 경우 발생

**해결**: SSE 이벤트 핸들러 내에서 `queryClient.invalidateQueries(['orders', storeId])`를 즉시 호출하도록 수정. 이벤트 수신과 캐시 무효화 사이의 비동기 타이밍 이슈를 해결하고, 새 주문 페이로드에 포함된 `stockWarnings`를 Zustand 스토어에 즉시 반영하도록 분리.

</details>

<details>
<summary><b>5. 마감 재고 차감 정합성 & 취소 복원 범위</b></summary>
<br/>

**문제**: 마감 확정 시 재고 차감 로직이 복잡했음

- 주문이 `preparing` 상태가 될 때 이미 실시간으로 재고가 차감됨
- 사용자가 실제로 확인한 잔여 재고와 시스템 계산값이 다를 수 있음
- 마감 취소 시 어디까지 복원해야 하는지 기준이 불명확했음

**해결**: 3단계 수치 설계로 해결

```
orderDeductedAmount  = preparing + completed 주문 기반 레시피 이론 차감량 (시스템 계산)
remainingStock       = 사장님이 직접 확인해 입력한 실제 잔여 재고
─────────────────────────────────────────────────────────────────────
actualUsage          = openingStock - remainingStock (실제 총 사용량)
adjustmentAmount     = actualUsage - orderDeductedAmount (보정값 = 이론과 실제의 차이)
```

마감 취소 시에는 `adjustmentAmount`(보정값)만 복원하고, 주문 기반 차감분은 유지. `GET /closing/preview` 전용 엔드포인트로 미리보기와 확정을 명확히 분리.

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

이슈 생성 시 `.github/ISSUE_TEMPLATE/` 내 템플릿을 **반드시** 사용한다.

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

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=자주%20묻는%20질문&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

| 문제 상황                  | 원인                              | 해결 방법                                     |
| -------------------------- | --------------------------------- | --------------------------------------------- |
| 로그인 후 화면이 안 넘어감 | 카카오 OAuth 콜백 처리 지연       | 브라우저 새로고침 후 `/dashboard`로 직접 이동 |
| OCR 인식 결과가 엉뚱함     | 이미지 품질 불량 또는 비표준 서식 | 밝은 환경에서 재촬영, 검수 화면에서 수동 수정 |
| 실시간 주문이 안 들어옴    | SSE 연결 끊김                     | 페이지 새로고침 (3초 후 자동 재연결)          |
| 재고 기능이 비활성화됨     | 등록된 식자재 없음                | 가게 설정 → 식자재 먼저 등록                  |
| 마감 후 재고 차감이 이상함 | 레시피 미설정 메뉴 존재           | 가게 설정 → 레시피 등록 후 재시도             |
| 발주 가이드가 생성 안 됨   | 마감 데이터 없음                  | 하루 영업 후 마감 완료 필요                   |

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=알려진%20제한사항&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

- 이미지 업로드 최대 **10MB**
- 식자재 단위는 `g`, `ml`, `개` **3종만 지원**
- **OCR 결과 자동 확정 불가** — 반드시 수동 검수 단계를 거쳐야 함
- **마감 재고 자동 차감 불가** — 사용자 검토·수정 후 최종 확정 필수
- JWT 토큰 localStorage 저장 (XSS 취약점 존재, httpOnly 쿠키 마이그레이션 예정)
- **카카오 소셜 로그인만 지원** (이메일·일반 회원가입 미지원)
- 회원 탈퇴 시 가게 데이터(재고·메뉴·레시피 등) **초기화 선행 필수**

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=향후%20구현%20기능&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

- [ ] httpOnly 쿠키 기반 JWT 저장으로 보안 강화
- [ ] 푸시 알림 (PWA / FCM) — 주문 수신 시 알림
- [ ] 다크 모드 (토글 UI 존재, 기능 완성 예정)
- [ ] 매출 분석 심화 — 카테고리별·시간대별·메뉴별 통계
- [ ] 바코드 스캔 기반 입고 처리
- [ ] 멀티 테이블 동시 주문 현황 뷰
- [ ] 다국어 지원 (i18n)
- [ ] 테스트 코드 작성 (Vitest)
- [ ] 모바일 앱 (React Native)

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

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=449CD4&height=45&text=라이선스&fontSize=18&fontColor=ffffff&fontAlign=50&fontAlignY=50" width="100%" />

This project is licensed under the MIT License.
