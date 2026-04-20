<p align="center">
  <a href="./README.md">English</a>
  ·
  <a href="./README.ko.md">한국어</a>
  ·
  <a href="./README.ja.md">日本語</a>
</p>

<h1 align="center">Hyeonjo Kim</h1>

<p align="center">
  Software builder creating polished products across web, AI, developer tools, browser extensions, desktop apps, and systems programming.
</p>

<p align="center">
  <a href="mailto:lion0110@naver.com">Email</a>
  ·
  <a href="https://github.com/hyeonjo00">GitHub</a>
  ·
  <a href="https://chat-paper-platform-iota.vercel.app/">Latest Project</a>
</p>

---

## About

I build practical software products that turn ideas into usable, deployable systems.

My work spans frontend applications, AI-powered products, developer tools, browser extensions, desktop software, and low-level systems. I care about clean UX, reliable architecture, fast iteration, and shipping projects that feel complete enough to be used in the real world.

Recently, I have been working with Next.js, TypeScript, OpenAI API, Claude, JavaFX, Chrome Extension, Prisma, PostgreSQL, C, and Java.

---

## Tech Stack

### Frontend
<p>
  <img src="https://skillicons.dev/icons?i=react,nextjs,js,ts,tailwind,html,css" />
</p>

### Backend & Database
<p>
  <img src="https://skillicons.dev/icons?i=nodejs,postgres,prisma" />
</p>

### AI & Automation
<p>
  <img src="https://img.shields.io/badge/OpenAI_API-111827?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI API" />
  <img src="https://img.shields.io/badge/Claude-CC785C?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude" />
</p>

### Desktop & Systems
<p>
  <img src="https://skillicons.dev/icons?i=java,c" />
  <img src="https://img.shields.io/badge/JavaFX-1F2937?style=for-the-badge&logo=openjdk&logoColor=white" alt="JavaFX" />
  <img src="https://img.shields.io/badge/raylib-111827?style=for-the-badge&logo=c&logoColor=white" alt="raylib" />
</p>

### Browser & Extensions
<p>
  <img src="https://img.shields.io/badge/Chrome_Extension-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Chrome Extension" />
  <img src="https://img.shields.io/badge/Manifest_V3-111827?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Manifest V3" />
</p>

### Deployment & Tools
<p>
  <img src="https://skillicons.dev/icons?i=vercel,git,github,vscode,npm" />
</p>

---

## Projects

### Chat Paper AI
Korean-first AI SaaS platform that turns KakaoTalk and AI conversation logs into academic-style research papers.

<p align="center">
  <a href="https://chat-paper-platform-iota.vercel.app/">
    <img src="https://raw.githubusercontent.com/hyeonjo00/chat-paper-platform/main/docs/screenshots/home-dark.png" alt="Chat Paper AI desktop preview" width="100%" />
  </a>
</p>

**Highlights**
- KakaoTalk `.zip` / `.txt` upload and conversation parsing
- AI-powered conversation analysis and academic paper generation
- Research dashboard for generated paper insights
- Journal-style academic paper reader
- Guest-first workflow without login friction
- Korean / Japanese / English UI support
- Dark mode ready responsive SaaS interface
- Privacy-conscious flow with raw uploads not permanently stored

**Tech**  
Next.js, TypeScript, Tailwind CSS, Prisma, PostgreSQL, OpenAI API, Vercel

**Documentation**
- [Technical Whitepaper (EN)](https://github.com/hyeonjo00/chat-paper-platform/blob/main/docs/chat-paper-ai-technical-whitepaper-en.md)
- [Technical Whitepaper (KO)](https://github.com/hyeonjo00/chat-paper-platform/blob/main/docs/chat-paper-ai-technical-whitepaper-ko.md)

**Links**
- Demo: https://chat-paper-platform-iota.vercel.app/
- GitHub: https://github.com/hyeonjo00/chat-paper-platform

---

### Chart Insight Assistant
AI-powered stock and crypto chart screenshot analysis SaaS.

Chart Insight Assistant is a Next.js application that lets users upload market chart screenshots, run cautious OpenAI-powered scenario analysis, and review structured trading insights in a clean dark UI.

<p align="center">
  <a href="https://chart-insight-assistant.vercel.app">
    <img src="https://raw.githubusercontent.com/hyeonjo00/chart-insight-assistant/main/public/readme/home.png" alt="Chart Insight Assistant home preview" width="100%" />
  </a>
</p>

**Highlights**
- Drag-and-drop chart screenshot upload
- Image preview with PNG, JPG, JPEG, and WEBP validation
- Server-side OpenAI chart analysis API route
- Structured analysis output: bias, confidence, entry zone, invalidation zone, take-profit targets, and summary
- Cautious scenario-based market interpretation without guaranteed predictions
- Local analysis history saved with `localStorage`
- Clean dark-themed responsive UI
- Google AdSense-ready monetization structure
- `ads.txt` verification support
- English / Korean / Japanese README documentation

#### Product Screens

<p align="center">
  <img src="https://raw.githubusercontent.com/hyeonjo00/chart-insight-assistant/main/public/readme/analyze.png" alt="Chart Insight Assistant upload screen" width="49%" />
  <img src="https://raw.githubusercontent.com/hyeonjo00/chart-insight-assistant/main/public/readme/analysis-result.png" alt="Chart Insight Assistant analysis result" width="49%" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/hyeonjo00/chart-insight-assistant/main/public/readme/history.png" alt="Chart Insight Assistant history screen" width="100%" />
</p>

**Tech**  
Next.js, TypeScript, Tailwind CSS, OpenAI API, Vercel, Google AdSense

**Architecture**
- `app/api/analyze/route.ts` handles server-side OpenAI requests
- `components/chart-upload-panel.tsx` manages upload, preview, API call, result rendering, and local history saving
- `lib/analysis-history.ts` stores completed analysis results in browser `localStorage`
- `components/ad-banner.tsx` prepares reusable AdSense-ready ad slots

**Links**
- Demo: https://chart-insight-assistant.vercel.app
- GitHub: https://github.com/hyeonjo00/chart-insight-assistant
- English README: https://github.com/hyeonjo00/chart-insight-assistant/blob/main/README.en.md
- Korean README: https://github.com/hyeonjo00/chart-insight-assistant/blob/main/README.ko.md
- Japanese README: https://github.com/hyeonjo00/chart-insight-assistant/blob/main/README.ja.md

---

# ToS Change Tracker

![ToS Change Tracker Screenshot](https://raw.githubusercontent.com/hyeonjo00/tos-change-tracker/main/public/readme/home.png)

ToS Change Tracker is an AI-assisted Next.js prototype for reviewing changes in terms of service, privacy policies, and other user-facing policy documents. A user enters a public policy URL, the server fetches the page, normalizes the HTML into readable text, and generates a line-level diff. When an OpenAI API key is configured, the app also summarizes the changes and provides a Low, Medium, or High risk assessment.

## Key Features

- Policy URL input with server-side HTML fetching
- Text normalization by removing scripts, styles, and HTML tags
- Line-level document diffing with the `diff` package
- OpenAI Responses API integration for change summaries and risk analysis
- Dark and light theme support
- English, Korean, and Japanese README and whitepaper documentation
- Real application screenshot for portfolio presentation

## Tech Stack

- Next.js App Router
- React
- TypeScript
- Tailwind CSS
- OpenAI Responses API
- diff

## Technical Whitepaper

- [English Whitepaper](https://github.com/hyeonjo00/tos-change-tracker/blob/main/docs/tos-change-tracker-technical-whitepaper-en.md)
- [Korean Whitepaper](https://github.com/hyeonjo00/tos-change-tracker/blob/main/docs/tos-change-tracker-technical-whitepaper-ko.md)
- [Japanese Whitepaper](https://github.com/hyeonjo00/tos-change-tracker/blob/main/docs/tos-change-tracker-technical-whitepaper-ja.md)

## Links

- Demo: [https://tos-change-tracker.vercel.app/](https://tos-change-tracker.vercel.app/)
- GitHub: [https://github.com/hyeonjo00/tos-change-tracker](https://github.com/hyeonjo00/tos-change-tracker)

## Project Highlight

This project demonstrates the core pipeline of a policy-change monitoring product in a small, transparent prototype. The current version focuses on URL fetching, text normalization, diff generation, and AI-assisted summarization, while leaving a clear path toward database-backed snapshots and scheduled monitoring.


---

## AI Code Review

![AI Code Review screenshot](https://ai-code-review-lac-seven.vercel.app/screenshots/ai-code-review.png)

AI Code Review is a Next.js web application that uses the OpenAI API to analyze JavaScript or TypeScript code and return structured feedback. Users can paste code, request a review, and receive issues, improvement ideas, and a revised code example in a clean two-panel interface.

### Key Features

- Submit pasted code for AI review
- Receive issues, improvements, and revised code
- Copy review output to the clipboard
- Load sample code for quick demos
- Protect the OpenAI API key with a server-side route handler
- Includes README screenshot and technical whitepaper documentation

### Tech Stack

Next.js 16, React 19, TypeScript, Tailwind CSS, OpenAI Responses API, react-syntax-highlighter

### Technical Whitepapers

- [English Technical Whitepaper](https://github.com/hyeonjo00/ai-code-review/blob/main/docs/TECHNICAL_WHITEPAPER.en.md)
- [Korean Technical Whitepaper](https://github.com/hyeonjo00/ai-code-review/blob/main/docs/TECHNICAL_WHITEPAPER.ko.md)

### Links

- Repository: [GitHub](https://github.com/hyeonjo00/ai-code-review)
- Demo: [https://ai-code-review-lac-seven.vercel.app/](https://ai-code-review-lac-seven.vercel.app/)



---

### Premium JavaFX Blackjack Simulator
A premium desktop blackjack simulator built with JavaFX, featuring real-time strategy analysis, advanced gameplay actions, and a casino-style animated UI.

**Highlights**
- Real-time AI strategy analysis
- Hit / Stand / Double / Split support
- Expected EV, bust risk, and dealer bust chance display
- Session save / load and stats export
- Premium casino-style table UI with animated dealing flow
- Multi-hand split support and recommendation accuracy tracking

**Tech**  
Java, JavaFX, FXML, CSS

#### Gameplay Showcase

**Premium Table Theme**

![Theme Demo](https://raw.githubusercontent.com/hyeonjo00/blackjack-engine-java/main/screenshots/balckjack_starttheme.gif)

**Hit / Stand Decision Flow**

![Hit Stand Demo](https://raw.githubusercontent.com/hyeonjo00/blackjack-engine-java/main/screenshots/balckjack_hitstand.gif)

**Double Down Action**

![Double Down Demo](https://raw.githubusercontent.com/hyeonjo00/blackjack-engine-java/main/screenshots/balckjack_doubledown.gif)

**Split Hand Management**

![Split Demo](https://raw.githubusercontent.com/hyeonjo00/blackjack-engine-java/main/screenshots/balckjack_split.gif)

#### Documentation

Premium software engineering whitepapers covering the Blackjack Engine architecture, EV strategy logic, split recursion, UI-state synchronization, and optimization roadmap.

- [English Whitepaper PDF](https://raw.githubusercontent.com/hyeonjo00/blackjack-engine-java/main/docs/premium-javafx-blackjack-engine-whitepaper.pdf)
- [Korean Whitepaper PDF](https://raw.githubusercontent.com/hyeonjo00/blackjack-engine-java/main/docs/premium-javafx-blackjack-engine-whitepaper-ko.pdf)

**Links**
- GitHub: https://github.com/hyeonjo00/blackjack-engine-java

---

### MiniDB Studio
A lightweight database management studio built in pure C.

This project combines a reusable storage engine, B+ Tree indexing, WAL-style recovery, and a native raylib desktop UI.

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

**Highlights**
- Two-layer architecture with a pure C11 storage engine and a separate native desktop UI
- Hash indexes on `id` and `department`, plus B+ Tree indexes on `id` and `age`
- Lightweight query optimizer for exact lookups, range scans, and ordered traversal
- CSV snapshot + WAL replay recovery model
- Studio-style desktop workflow with a SQL workspace, result grid, index explorer, storage browser, and performance dashboard

<p align="center">
  <a href="https://github.com/hyeonjo00/c-mini-db-engine">
    <img src="https://raw.githubusercontent.com/hyeonjo00/c-mini-db-engine/main/docs/studio-benchmark.svg" alt="MiniDB Studio benchmark dashboard" width="100%" />
  </a>
</p>

**Links**
- Repository: https://github.com/hyeonjo00/c-mini-db-engine
- README: https://github.com/hyeonjo00/c-mini-db-engine/blob/main/README.md
- Whitepaper (EN): https://github.com/hyeonjo00/c-mini-db-engine/blob/main/docs/minidb-studio-algorithm-whitepaper-en.pdf

---

## GitHub Stats

<p align="center">
  <img src="https://github-readme-stats-sigma-five.vercel.app/api?username=hyeonjo00&show_icons=true&theme=tokyonight" />
</p>

## Top Languages

<p align="center">
  <img src="https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=hyeonjo00&layout=compact&theme=tokyonight&langs_count=8" />
</p>
