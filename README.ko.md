<p align="center">
  <a href="./README.md">English</a>
  ·
  <a href="./README.ko.md">한국어</a>
  ·
  <a href="./README.ja.md">日本語</a>
</p>

<h1 align="center">김현조</h1>

<p align="center">
  웹, AI, 개발자 도구, 브라우저 확장, 데스크톱 앱, 시스템 프로그래밍까지 제품으로 완성하는 소프트웨어 빌더입니다.
</p>

<p align="center">
  <a href="mailto:lion0110@naver.com">Email</a>
  ·
  <a href="https://github.com/hyeonjo00">GitHub</a>
  ·
  <a href="https://chat-paper-platform-iota.vercel.app/">Latest Project</a>
</p>

---

## 소개

아이디어를 실제로 사용할 수 있는 제품과 시스템으로 만드는 개발자입니다.

프론트엔드 애플리케이션, AI 기반 제품, 개발자 도구, 브라우저 확장 프로그램, 데스크톱 소프트웨어, 로우레벨 시스템까지 다양한 영역을 다룹니다. 깔끔한 UX, 신뢰할 수 있는 구조, 빠른 반복 개발, 그리고 실제 사용자에게 보여줄 수 있는 완성도를 중요하게 생각합니다.

최근에는 Next.js, TypeScript, OpenAI API, Claude, JavaFX, Chrome Extension, Prisma, PostgreSQL, C, Java를 활용해 여러 제품을 만들고 있습니다.

## 소개

아이디어를 실제로 사용할 수 있는 제품과 시스템으로 만드는 개발자입니다.

프론트엔드 애플리케이션, AI 기반 제품, 개발자 도구, 브라우저 확장 프로그램, 데스크톱 소프트웨어, 로우레벨 시스템까지 다양한 영역을 다룹니다. 깔끔한 UX, 신뢰할 수 있는 구조, 빠른 반복 개발, 그리고 실제 사용자에게 보여줄 수 있는 완성도를 중요하게 생각합니다.

최근에는 Next.js, TypeScript, OpenAI API, Claude, JavaFX, Chrome Extension, Prisma, PostgreSQL, C, Java를 활용해 여러 제품을 만들고 있습니다.

---

## 기술 스택

### 프론트엔드
<p>
  <img src="https://skillicons.dev/icons?i=react,nextjs,js,ts,tailwind,html,css" />
</p>

### 백엔드 & 데이터베이스
<p>
  <img src="https://skillicons.dev/icons?i=nodejs,postgres,prisma" />
</p>

### AI & 자동화
<p>
  <img src="https://img.shields.io/badge/OpenAI_API-111827?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI API" />
  <img src="https://img.shields.io/badge/Claude-CC785C?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude" />
</p>

### 데스크톱 & 시스템
<p>
  <img src="https://skillicons.dev/icons?i=java,c" />
  <img src="https://img.shields.io/badge/JavaFX-1F2937?style=for-the-badge&logo=openjdk&logoColor=white" alt="JavaFX" />
  <img src="https://img.shields.io/badge/raylib-111827?style=for-the-badge&logo=c&logoColor=white" alt="raylib" />
</p>

### 브라우저 & 확장 프로그램
<p>
  <img src="https://img.shields.io/badge/Chrome_Extension-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Chrome Extension" />
  <img src="https://img.shields.io/badge/Manifest_V3-111827?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Manifest V3" />
</p>

### 배포 & 도구
<p>
  <img src="https://skillicons.dev/icons?i=vercel,git,github,vscode,npm" />
</p>

---

## 프로젝트

### Chat Paper AI
카카오톡, 인스타그램 DM, LINE, AI 대화 로그를 학술 논문 형식의 리서치 문서로 변환하는 한국어 중심 AI SaaS 플랫폼입니다.

<p align="center">
  <a href="https://chat-paper-platform-iota.vercel.app/">
    <img src="https://raw.githubusercontent.com/hyeonjo00/chat-paper-platform/main/docs/screenshots/home-dark.png" alt="Chat Paper AI 데스크톱 미리보기" width="100%" />
  </a>
</p>

**주요 기능**
- KakaoTalk `.zip` / `.txt`, Instagram DM, LINE, AI 대화 로그 업로드 지원
- 대화 데이터를 파싱, 익명화한 뒤 AI 논문 생성 파이프라인으로 처리
- 제목, 초록, 서론, 연구 방법, 결과, 논의, 결론으로 구성된 학술형 문서 생성
- 한국어 / 영어 / 일본어 UI 및 논문 생성 흐름 지원
- 로그인 없이 사용할 수 있는 게스트 기반 워크플로우
- 생성 결과를 확인할 수 있는 리서치 대시보드와 진행 상태 UI
- 저널 스타일의 논문 리더와 export 중심 UX
- 원본 업로드 파일을 영구 저장하지 않는 개인정보 보호 중심 설계

**백엔드 설계**
- Next.js API Routes, Redis, BullMQ, Prisma, PostgreSQL, 독립 Node.js Worker 기반 비동기 생성 파이프라인 구축
- 업로드/분석 API에서 DB 접근 전 Redis preflight rate limit을 먼저 실행해 게스트 기반 DB DoS 위험 완화
- 긴 AI 논문 생성 작업은 API에서 직접 실행하지 않고 BullMQ 큐와 Worker를 통해 처리
- PostgreSQL `idempotencyKey`와 BullMQ `jobId`에 동일한 SHA-256 키를 사용해 중복 생성 방지
- Prisma Serializable transaction으로 작업 quota, Paper 생성, Job 생성을 원자적으로 처리
- Worker에 hard timeout, OpenAI 요청 timeout, exponential backoff + jitter retry, graceful shutdown 적용
- Redis 상태를 확인한 뒤 stuck job을 복구하여 중복 실행 위험을 줄임
- ZIP 업로드는 Content-Length 검증, entry 수 제한, 파일별 크기 제한, 총 압축 해제 크기 제한으로 방어

**기술 스택**  
Next.js, TypeScript, Tailwind CSS, Prisma, PostgreSQL, Redis, BullMQ, OpenAI API, Node.js Worker, Vercel, Fly.io

**문서**
- [기술 백서 (EN)](https://github.com/hyeonjo00/chat-paper-platform/blob/main/docs/chat-paper-ai-technical-whitepaper-en.md)
- [기술 백서 (KO)](https://github.com/hyeonjo00/chat-paper-platform/blob/main/docs/chat-paper-ai-technical-whitepaper-ko.md)

**링크**
- Demo: https://chat-paper-platform-iota.vercel.app/
- GitHub: https://github.com/hyeonjo00/chat-paper-platform

---

### Chart Insight Assistant
AI 기반 주식 및 암호화폐 차트 스크린샷 분석 SaaS.

Chart Insight Assistant는 사용자가 시장 차트 스크린샷을 업로드하고, OpenAI 기반의 보수적인 시나리오형 분석을 실행한 뒤, 구조화된 트레이딩 인사이트를 다크 테마 UI에서 확인할 수 있는 Next.js 애플리케이션입니다.

<p align="center">
  <a href="https://chart-insight-assistant.vercel.app">
    <img src="https://raw.githubusercontent.com/hyeonjo00/chart-insight-assistant/main/public/readme/home.png" alt="Chart Insight Assistant 홈 화면" width="100%" />
  </a>
</p>

**주요 기능**
- 드래그 앤 드롭 차트 스크린샷 업로드
- PNG, JPG, JPEG, WEBP 이미지 미리보기 및 파일 검증
- 서버 사이드 OpenAI 차트 분석 API 라우트
- 구조화된 분석 결과: Bias, Confidence, Entry Zone, Invalidation Zone, Take Profit Targets, Summary
- 미래 가격을 보장하지 않는 보수적인 시나리오형 시장 해석
- `localStorage` 기반 로컬 분석 히스토리 저장
- 깔끔한 다크 테마 반응형 UI
- Google AdSense 준비형 수익화 구조
- `ads.txt` 사이트 인증 지원
- 영어 / 한국어 / 일본어 README 및 기술 백서 문서화

#### 제품 화면

<p align="center">
  <img src="https://raw.githubusercontent.com/hyeonjo00/chart-insight-assistant/main/public/readme/analyze.png" alt="Chart Insight Assistant 업로드 화면" width="49%" />
  <img src="https://raw.githubusercontent.com/hyeonjo00/chart-insight-assistant/main/public/readme/analysis-result.png" alt="Chart Insight Assistant 분석 완료 화면" width="49%" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/hyeonjo00/chart-insight-assistant/main/public/readme/history.png" alt="Chart Insight Assistant 히스토리 화면" width="100%" />
</p>

**기술 스택**  
Next.js, TypeScript, Tailwind CSS, OpenAI API, Vercel, Google AdSense

**아키텍처**
- `app/api/analyze/route.ts`: 서버 사이드 OpenAI 이미지 분석 요청 처리
- `components/chart-upload-panel.tsx`: 업로드, 미리보기, API 전송, 결과 렌더링, 로컬 히스토리 저장 흐름 관리
- `lib/analysis-history.ts`: 완료된 분석 결과를 브라우저 `localStorage`에 저장
- `components/ad-banner.tsx`: 재사용 가능한 AdSense 준비형 광고 슬롯 제공
- `docs/`: 다국어 기술 백서 문서 포함

**기술 백서**
- English: https://github.com/hyeonjo00/chart-insight-assistant/blob/main/docs/technical-whitepaper-en.md
- Korean: https://github.com/hyeonjo00/chart-insight-assistant/blob/main/docs/technical-whitepaper-ko.md
- Japanese: https://github.com/hyeonjo00/chart-insight-assistant/blob/main/docs/technical-whitepaper-ja.md

**링크**
- Demo: https://chart-insight-assistant.vercel.app
- GitHub: https://github.com/hyeonjo00/chart-insight-assistant
- README: https://github.com/hyeonjo00/chart-insight-assistant



---

# ToS Change Tracker

![ToS Change Tracker Screenshot](https://raw.githubusercontent.com/hyeonjo00/tos-change-tracker/main/public/readme/home.png)

ToS Change Tracker는 서비스 약관, 개인정보 처리방침, 정책 문서의 변경 사항을 빠르게 확인하기 위한 Next.js 기반 AI 프로토타입입니다. 사용자가 공개 정책 URL을 입력하면 서버에서 페이지를 가져오고, HTML을 읽기 쉬운 텍스트로 정리한 뒤, 줄 단위 diff를 생성합니다. OpenAI API 키가 설정되어 있으면 변경 내용을 요약하고 Low, Medium, High 기준의 위험도 분석도 제공합니다.

## 주요 기능

- 정책 URL 입력 및 서버 측 HTML fetch
- script, style, 태그 제거를 통한 텍스트 정규화
- `diff` 패키지 기반 줄 단위 변경 비교
- OpenAI Responses API 기반 변경 요약 및 위험도 분석
- 다크/라이트 테마 전환
- 영어, 한국어, 일본어 README 및 기술백서 제공
- 실제 화면 스크린샷 포함

## 기술 스택

- Next.js App Router
- React
- TypeScript
- Tailwind CSS
- OpenAI Responses API
- diff

## 기술백서

- [한국어 기술백서](https://github.com/hyeonjo00/tos-change-tracker/blob/main/docs/tos-change-tracker-technical-whitepaper-ko.md)
- [English Whitepaper](https://github.com/hyeonjo00/tos-change-tracker/blob/main/docs/tos-change-tracker-technical-whitepaper-en.md)
- [日本語ホワイトペーパー](https://github.com/hyeonjo00/tos-change-tracker/blob/main/docs/tos-change-tracker-technical-whitepaper-ja.md)

## Links

- Demo: [https://tos-change-tracker.vercel.app/](https://tos-change-tracker.vercel.app/)
- GitHub: [https://github.com/hyeonjo00/tos-change-tracker](https://github.com/hyeonjo00/tos-change-tracker)

## 프로젝트 포인트

이 프로젝트는 약관 변경 모니터링 제품의 핵심 파이프라인을 작고 투명하게 구현한 프로토타입입니다. 현재는 URL fetch, 텍스트 정규화, diff 생성, AI 요약 흐름에 집중하며, 향후 데이터베이스 기반 스냅샷 저장과 예약 모니터링으로 확장할 수 있도록 설계했습니다.


---

## AI 코드 리뷰

![AI 코드 리뷰 화면](https://ai-code-review-lac-seven.vercel.app/screenshots/ai-code-review.png)

AI 코드 리뷰는 OpenAI API를 활용해 JavaScript 또는 TypeScript 코드를 분석하고, 문제점과 개선 아이디어, 수정 예시 코드를 제공하는 Next.js 기반 웹 애플리케이션입니다. 사용자는 코드를 붙여 넣고 버튼을 누르는 것만으로 구조화된 AI 리뷰 결과를 받을 수 있습니다.

### 주요 기능

- 코드 입력 후 AI 리뷰 요청
- 문제점, 개선점, 수정 예시 코드 제공
- 리뷰 결과 클립보드 복사
- 샘플 코드 불러오기
- 서버 라우트 핸들러를 통한 OpenAI API 키 보호
- README 스크린샷과 기술백서 문서화

### 기술 스택

Next.js 16, React 19, TypeScript, Tailwind CSS, OpenAI Responses API, react-syntax-highlighter

### 기술백서

- [한국어 기술백서](https://github.com/hyeonjo00/ai-code-review/blob/main/docs/TECHNICAL_WHITEPAPER.ko.md)
- [English Technical Whitepaper](https://github.com/hyeonjo00/ai-code-review/blob/main/docs/TECHNICAL_WHITEPAPER.en.md)

### 링크

- Repository: [GitHub](https://github.com/hyeonjo00/ai-code-review)
- Demo: [https://ai-code-review-lac-seven.vercel.app/](https://ai-code-review-lac-seven.vercel.app/)


---

### Premium JavaFX Blackjack Simulator
JavaFX로 만든 프리미엄 데스크톱 블랙잭 시뮬레이터입니다. 실시간 전략 분석, 고급 게임 액션, 카지노 스타일 애니메이션 UI를 제공합니다.

**주요 기능**
- 실시간 AI 전략 분석
- Hit / Stand / Double / Split 지원
- 기대 EV, 버스트 위험도, 딜러 버스트 확률 표시
- 세션 저장 / 불러오기 및 통계 내보내기
- 애니메이션 딜링 플로우가 있는 프리미엄 카지노 테이블 UI
- 멀티 핸드 Split 지원 및 추천 정확도 추적

**기술**  
Java, JavaFX, FXML, CSS

#### 플레이 쇼케이스

**프리미엄 테이블 테마**

![Theme Demo](https://raw.githubusercontent.com/hyeonjo00/blackjack-engine-java/main/screenshots/balckjack_starttheme.gif)

**Hit / Stand 의사결정 흐름**

![Hit Stand Demo](https://raw.githubusercontent.com/hyeonjo00/blackjack-engine-java/main/screenshots/balckjack_hitstand.gif)

**Double Down 액션**

![Double Down Demo](https://raw.githubusercontent.com/hyeonjo00/blackjack-engine-java/main/screenshots/balckjack_doubledown.gif)

**Split 핸드 관리**

![Split Demo](https://raw.githubusercontent.com/hyeonjo00/blackjack-engine-java/main/screenshots/balckjack_split.gif)

#### 문서

Blackjack Engine 아키텍처, EV 전략 로직, Split 재귀 처리, UI 상태 동기화, 최적화 로드맵을 다룬 소프트웨어 엔지니어링 기술백서입니다.

- [영문 기술백서 PDF](https://raw.githubusercontent.com/hyeonjo00/blackjack-engine-java/main/docs/premium-javafx-blackjack-engine-whitepaper.pdf)
- [국문 기술백서 PDF](https://raw.githubusercontent.com/hyeonjo00/blackjack-engine-java/main/docs/premium-javafx-blackjack-engine-whitepaper-ko.pdf)

**링크**
- GitHub: https://github.com/hyeonjo00/blackjack-engine-java

---

### MiniDB Studio
순수 C로 만든 경량 데이터베이스 관리 스튜디오입니다.

재사용 가능한 스토리지 엔진, B+ Tree 인덱싱, WAL 스타일 복구, raylib 기반 네이티브 데스크톱 UI를 결합한 프로젝트입니다.

<p align="center">
  <a href="https://github.com/hyeonjo00/c-mini-db-engine">
    <img src="https://raw.githubusercontent.com/hyeonjo00/c-mini-db-engine/main/docs/studio-overview.svg" alt="MiniDB Studio overview" width="100%" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/C-C11-00599C?style=for-the-badge&logo=c&logoColor=white" alt="C11" />
  <img src="https://img.shields.io/badge/UI-raylib-1F2937?style=for-the-badge" alt="raylib" />
  <img src="https://img.shields.io/badge/Engine-B%2B%20Tree%20%2B%20WAL-60A5FA?style=for-the-badge" alt="B+ Tree and WAL" />
</p>

**주요 기능**
- 순수 C11 스토리지 엔진과 별도 네이티브 데스크톱 UI로 구성된 2계층 구조
- `id`, `department` 해시 인덱스와 `id`, `age` B+ Tree 인덱스
- exact lookup, range scan, ordered traversal을 위한 경량 쿼리 옵티마이저
- CSV snapshot + WAL replay 기반 복구 모델
- SQL 작업 공간, 결과 그리드, 인덱스 탐색기, 스토리지 브라우저, 성능 대시보드를 갖춘 Studio 스타일 워크플로우

<p align="center">
  <a href="https://github.com/hyeonjo00/c-mini-db-engine">
    <img src="https://raw.githubusercontent.com/hyeonjo00/c-mini-db-engine/main/docs/studio-benchmark.svg" alt="MiniDB Studio benchmark dashboard" width="100%" />
  </a>
</p>

**링크**
- Repository: https://github.com/hyeonjo00/c-mini-db-engine
- README: https://github.com/hyeonjo00/c-mini-db-engine/blob/main/README.md
- Whitepaper EN: https://github.com/hyeonjo00/c-mini-db-engine/blob/main/docs/minidb-studio-algorithm-whitepaper-en.pdf

---

## GitHub 통계

<p align="center">
  <img src="https://github-readme-stats-sigma-five.vercel.app/api?username=hyeonjo00&show_icons=true&theme=tokyonight" />
</p>

## 사용 언어

<p align="center">
  <img src="https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=hyeonjo00&layout=compact&theme=tokyonight&langs_count=8" />
</p>

