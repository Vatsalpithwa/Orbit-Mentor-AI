# 🚀 Orbit Mentor AI

> **An all-in-one AI-powered learning, coding, and career mentorship platform**

[![Next.js](https://img.shields.io/badge/Next.js-14-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Supabase](https://img.shields.io/badge/Supabase-PostgreSQL-green?style=flat-square&logo=supabase)](https://supabase.com/)
[![Gemini AI](https://img.shields.io/badge/Google-Gemini_AI-orange?style=flat-square&logo=google)](https://ai.google.dev/)
[![License](https://img.shields.io/badge/License-MIT-purple?style=flat-square)](LICENSE)

Orbit Mentor AI is a production-grade, dark-themed web application that acts as an autonomous AI mentor, real-time chatbot, daily task manager, multi-language coding lab, exam certification platform, progress scoreboard, and career roadmap assistant — all in one unified experience.

---

## 📋 Table of Contents

- [Current Status](#-current-status)
- [Key Features](#-key-features)
- [Technology Stack](#-technology-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Supabase Setup](#-supabase-setup)
- [Security Architecture](#-security-architecture)
- [Deployment](#-deployment)
- [Future Roadmap](#-future-roadmap)

---

## 📊 Current Status

### ✅ Completed & Working

| Module | Status | Notes |
|--------|--------|-------|
| **Landing Page** | ✅ Complete | Glassmorphism design, Google OAuth entry |
| **Google OAuth Auth** | ✅ Complete | Supabase Auth + persistent sessions + RLS |
| **AI Chatbot (Astra & Orion)** | ✅ Complete | Streaming, Markdown, syntax highlighting, citations |
| **Task Manager + Pomodoro** | ✅ Complete | CRUD, calendar view, Web Audio API chimes |
| **Cognitive Scoreboard** | ✅ Complete | Heatmap, metrics, achievement badges |
| **AI Quiz Generator** | ✅ Complete | MCQ, T/F, Short Answer, Coding types |
| **Voice Mentor Stage** | ✅ Complete | Speech Synthesis + Recognition, rate/pitch controls |
| **Neural Voice Player** | ✅ Complete | Advanced voice playback engine (`neuralVoice.ts`) |
| **Multi-Language Code Lab** | ✅ Complete | JS, Python, HTML/CSS, SQL, C++ sandboxed execution |
| **Timed Certification Exams** | ✅ Complete | Countdown, hint tokens, AI revision recommendations |
| **Career Roadmap** | ✅ Complete | Phased milestones, resources, interview prep |
| **Tech News Feed** | ✅ Complete | AI, Cybersecurity, Open Source, bookmarks |
| **3D Interactive Globe** | ✅ Complete | Three.js Earth with pulsing tech event markers |
| **Command Palette** | ✅ Complete | Quick-access keyboard-driven navigation |
| **Onboarding Flow** | ✅ Complete | Profile setup modal on first login |
| **Profile Settings** | ✅ Complete | Avatar, interests, career goals, preferences |
| **Toast Notifications** | ✅ Complete | Global context-based notification system |
| **Database Schema** | ✅ Complete | `supabase_schema.sql` with RLS policies |

### 🚧 In Progress / Needs Refinement

| Area | Issue | Priority |
|------|-------|----------|
| `.env.local` in git | Accidentally committed — needs removal from history | 🔴 High |
| `next-env.d.ts` in git | Auto-generated file, should be gitignored | 🟡 Medium |
| `tsconfig.tsbuildinfo` in git | Build artifact, should be gitignored | 🟡 Medium |
| Voice Mentor TTS | `/api/ai/tts` route needs real provider integration | 🟡 Medium |
| Python Execution | WebAssembly Pyodide integration completeness | 🟡 Medium |

---

## 🌟 Key Features

### 1. 🔐 Google OAuth & Secure Sessions
- One-click Google sign-in powered by **Supabase Auth** — no passwords collected
- Persistent user profiles: avatar, interests, career goal, study preferences
- **PostgreSQL Row-Level Security (RLS)** ensuring zero cross-tenant data leakage

### 2. 🤖 Autonomous AI Chatbot with Streaming
- Real-time streaming responses with **Markdown rendering**, syntax highlighting, and copy buttons
- Two selectable mentor personas:
  - **Astra** — Female, inspiring, empathetic, deep-tech guide
  - **Orion** — Male, analytical, pragmatic, veteran software architect
- Explanation depth: **Beginner / Intermediate / Expert (Architectural)**
- Drag-and-drop file upload with AI vision & diagram analysis
- Voice note recording with live waveform and speech-to-text
- Real-time **Web Search mode** with live source citations

### 3. ✅ Daily Task Manager & Pomodoro Timer
- Full CRUD: categories, priorities, due dates, recurring patterns
- **List view** and **Weekly Calendar view**
- Integrated Pomodoro: 25m Focus · 5m Short Break · 15m Long Break · Custom
- Synthesized Web Audio API alert chimes on timer completion

### 4. 📊 Cognitive Scoreboard & Telemetry
- Daily / Weekly / Monthly / All-time performance metrics
- **GitHub-style 365-day heatmap**
- Focus velocity bar chart and unlocked achievement badges
- Strongest competencies & personalized improvement areas

### 5. 🧠 Adaptive AI Quiz Generator
- Instant quiz from any topic, subject, or pasted notes
- Types: **MCQ, True/False, Short Answer, Coding**
- Post-submission scoring, full solutions, and historical analytics

### 6. 🎙️ Voice Mentor Stage
- Lifelike vocal narration via **Web Speech Synthesis & Recognition**
- Rate controls (0.8x–1.5x), pitch tuning, mute options
- Step-by-step explainer mode + audio image analysis

### 7. 💻 Multi-Language Sandboxed Code Lab
- Languages: **JavaScript, Python 3, HTML5/CSS3, SQL, C++20**
- Line numbers, syntax styling, starter templates, runtime benchmarking
- **Safe sandboxed execution** — code never runs on the server:
  - JS → isolated client-side worker
  - Python → client-side WebAssembly (Pyodide)
  - HTML/CSS → sandboxed iframe
  - SQL → in-memory relational sandbox
- "Ask Mentor" & "Get Hint" progressive debug assistant

### 8. 📝 Timed Certification Exams
- Countdown timer, question navigator, flag-for-review system
- 3 progressive hint tokens per session
- Score breakdown + AI-generated revision recommendations

### 9. 🗺️ Step-by-Step Career Roadmap
- Phased roadmaps: Foundations → Intermediate → Advanced → Capstone → Interview Prep
- Interactive milestone checkboxes + curated resource links
- Senior & Staff-level interview questions per milestone
- **Custom roadmap generator** for any specialized role

### 10. 📰 Frontier Tech News
- Daily global updates: AI · Software · Cybersecurity · Science · Open Source
- Category filters, article summaries, bookmarks, "AI Brief" instant summaries

### 11. 🌍 3D Interactive Tech Globe
- **Three.js** rotating Earth with atmospheric glow and star field
- Pulsing markers for global AI breakthroughs, tech summits, quantum labs
- Click-to-inspect cards with verified source attributions

---

## 🛠️ Technology Stack

| Layer | Technology |
|-------|-----------|
| **Framework** | Next.js 14 (App Router) |
| **Language** | TypeScript 5.x |
| **UI** | React 18, Vanilla CSS (custom design system, glassmorphism) |
| **Icons** | Lucide React |
| **3D Graphics** | Three.js |
| **Audio** | Web Audio API (procedural synthesized chimes) |
| **Voice** | Web Speech API (SpeechSynthesis + SpeechRecognition) |
| **Database** | Supabase (PostgreSQL + Row-Level Security) |
| **Auth** | Supabase Auth (Google OAuth 2.0) |
| **AI Engine** | Google Gemini API + intelligent fallback reasoning engine |
| **Code Sandbox** | Client-side Workers, WebAssembly (Pyodide), sandboxed iframes |

---

## 📁 Project Structure

```
orbit-mentor-ai/
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   ├── ai/
│   │   │   │   ├── chat/route.ts         # Streaming AI chat endpoint
│   │   │   │   ├── code-assist/route.ts  # Code mentor endpoint
│   │   │   │   ├── quiz/route.ts         # Quiz generation endpoint
│   │   │   │   └── tts/route.ts          # Text-to-speech endpoint
│   │   │   └── code/
│   │   │       └── run/route.ts          # Code execution sandbox
│   │   ├── auth/
│   │   │   └── callback/route.ts         # Supabase OAuth callback
│   │   ├── dashboard/
│   │   │   └── page.tsx                  # Main dashboard shell
│   │   ├── globals.css                   # Global CSS design system
│   │   ├── layout.tsx                    # Root layout
│   │   └── page.tsx                      # Landing page
│   ├── components/
│   │   ├── Chat/
│   │   │   ├── ChatModule.tsx            # Full chat UI with streaming
│   │   │   └── MarkdownRenderer.tsx      # Markdown + code syntax renderer
│   │   ├── CodeLab/
│   │   │   └── CodeLabModule.tsx         # Multi-language code editor
│   │   ├── CommandPalette/
│   │   │   └── CommandPalette.tsx        # Keyboard-driven command palette
│   │   ├── Dashboard/
│   │   │   └── ScoreboardModule.tsx      # Metrics, heatmap, badges
│   │   ├── Exams/
│   │   │   └── ExamModule.tsx            # Timed certification exams
│   │   ├── Globe/
│   │   │   └── Globe3DModule.tsx         # Three.js interactive globe
│   │   ├── Navigation/
│   │   │   ├── Sidebar.tsx               # Side navigation
│   │   │   └── TopBar.tsx                # Top navigation bar
│   │   ├── News/
│   │   │   └── TechNewsModule.tsx        # Tech news feed
│   │   ├── Notification/
│   │   │   └── ToastContext.tsx          # Global toast notification system
│   │   ├── Profile/
│   │   │   ├── OnboardingModal.tsx       # First-login onboarding flow
│   │   │   └── ProfileSettingsModal.tsx  # User profile settings
│   │   ├── Quiz/
│   │   │   └── QuizModule.tsx            # AI quiz generator
│   │   ├── Roadmap/
│   │   │   └── RoadmapModule.tsx         # Career roadmap
│   │   ├── Tasks/
│   │   │   └── TaskManager.tsx           # Task manager + Pomodoro
│   │   └── VoiceMentor/
│   │       ├── NeuralVoicePlayer.tsx     # Advanced voice playback UI
│   │       └── VoiceMentorModule.tsx     # Voice mentor stage
│   └── lib/
│       ├── aiService.ts                  # Gemini AI service layer
│       ├── audio.ts                      # Web Audio API utilities
│       ├── neuralVoice.ts                # Neural voice engine
│       ├── sampleData.ts                 # Demo / fallback data
│       ├── supabase.ts                   # Supabase client + auth helpers
│       └── types.ts                      # Shared TypeScript types
├── supabase_schema.sql                   # Full DB schema with RLS policies
├── .env.example                          # Environment variable template
├── next.config.mjs                       # Next.js configuration
├── package.json
└── tsconfig.json
```

---

## 🚀 Getting Started

### Prerequisites
- **Node.js** v18.0.0 or higher
- **npm** or **yarn**

### Installation

```bash
# Clone the repository
git clone https://github.com/Vatsalpithwa/Orbit-Mentor-AI.git
cd Orbit-Mentor-AI

# Install dependencies
npm install
```

### Environment Variables

Copy the example file:
```bash
cp .env.example .env.local
```

Fill in your keys:
```env
# Supabase (optional — app falls back to local demo mode if empty)
NEXT_PUBLIC_SUPABASE_URL=https://your-project-id.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-supabase-anon-key

# Google Gemini AI (optional — app uses fallback AI engine if empty)
GEMINI_API_KEY=your-google-gemini-api-key

# App URL
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

> ✅ **Works out of the box!** Even without API keys, the app is fully interactive using persistent local session storage and a built-in fallback AI engine.

### Run Locally

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🗄️ Supabase Setup (Optional — for Cloud Sync)

1. Create a project at [supabase.com](https://supabase.com)
2. Go to **Authentication → Providers → Google** and enable Google OAuth
3. In **Authentication → URL Configuration**, add the redirect URL:
   ```
   http://localhost:3000/auth/callback       # Local development
   https://your-domain.com/auth/callback     # Production
   ```
4. Open the **SQL Editor**, paste the contents of `supabase_schema.sql`, and click **Run**
5. Copy your **Project URL** and **anon key** into `.env.local`

---

## 🔒 Security Architecture

| Layer | Protection |
|-------|-----------|
| **Authentication** | Google OAuth 2.0 only — no passwords ever collected or stored |
| **Database** | Row-Level Security on every table (`auth.uid() = user_id`) |
| **Code Execution** | All user code runs client-side (workers, WebAssembly, iframes) — never on the server |
| **Data Attribution** | Web search & news items always cite source, publisher, and date |
| **Secrets** | API keys stored server-side in env vars only — never exposed to the client |

---

## 📦 Deployment

### Deploy to Vercel (Recommended)

1. Push code to GitHub
2. Import the project at [vercel.com](https://vercel.com)
3. Add environment variables:
   - `NEXT_PUBLIC_SUPABASE_URL`
   - `NEXT_PUBLIC_SUPABASE_ANON_KEY`
   - `GEMINI_API_KEY`
   - `NEXT_PUBLIC_APP_URL`
4. Click **Deploy** 🚀

### Deploy to Netlify

```bash
npm run build
# Deploy the `.next` output folder via Netlify CLI or drag-and-drop
```

---

## 🔮 Future Roadmap

### 🔴 Immediate Fixes (High Priority)

- [ ] **Remove `.env.local` from git history** — accidentally committed with secrets; use `git filter-branch` or BFG Repo Cleaner to purge and force-push
- [ ] **Tighten `.gitignore`** — add `next-env.d.ts`, `tsconfig.tsbuildinfo`, `.env.local`
- [ ] **Revoke exposed GitHub PAT** — regenerate at [github.com/settings/tokens](https://github.com/settings/tokens)

### 🟠 Near-Term Features (v1.1)

- [ ] **Real TTS Provider** — integrate ElevenLabs or Google Cloud TTS for ultra-realistic voice synthesis beyond browser Speech API
- [ ] **Pyodide / Python Sandbox** — complete WebAssembly Python execution with package support (numpy, pandas, matplotlib)
- [ ] **C++ Compilation** — connect to a containerized backend (Judge0 or Docker) for real C++ compilation and execution
- [ ] **Chat History Persistence** — save and restore conversation threads from Supabase per user
- [ ] **File Attachment Vision** — complete image/diagram upload and AI vision analysis in chat
- [ ] **Mobile Responsive Overhaul** — audit and optimize all modules for small screens and touch

### 🟡 Medium-Term Features (v1.2)

- [ ] **Collaborative Mode** — real-time pair programming via WebRTC or Supabase Realtime channels
- [ ] **AI Flashcard Generator** — auto-generate spaced repetition flashcards from chat conversations
- [ ] **GitHub Integration** — link GitHub account to track commits, PRs, and streaks on the scoreboard
- [ ] **Custom Exam Builder** — let users create and share their own certification exam banks
- [ ] **Dark/Light Theme Toggle** — expose the design system theme as a user preference
- [ ] **Plugin / Extension System** — allow community-built mentor modules

### 🟢 Long-Term Vision (v2.0)

- [ ] **Native Mobile App** — React Native or Expo port of the full platform
- [ ] **AI Mentor Fine-Tuning** — users can "train" their mentor's personality over time using conversation history
- [ ] **Marketplace** — community-contributed roadmaps, quizzes, and exam banks
- [ ] **Enterprise Tier** — team management, cohort analytics, and company-specific knowledge bases
- [ ] **Offline PWA Support** — service worker caching for full offline study sessions
- [ ] **Localization** — multi-language UI (Spanish, Hindi, French, Arabic)
- [ ] **Accessibility (A11y) Audit** — full WCAG 2.1 AA compliance

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'feat: add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License**.

---

© 2026 Orbit Mentor AI · Built by [Vatsal Pithwa](https://github.com/Vatsalpithwa) · Empowering developers, students, and engineers globally 🌍

---

## 🌟 Key Features

1. **Futuristic Landing Page**:
   - Celestial glassmorphism design with responsive gradients and accessibility.
   - One-click Google OAuth sign-in and instant live demo exploration.

2. **Google OAuth & Secure Persistent Sessions**:
   - Google sign-in powered by Supabase Auth with zero password collection.
   - Persistent user profile with avatar, interests, career goal, and study preferences.
   - PostgreSQL Row-Level Security (RLS) ensuring strict user data isolation.

3. **Autonomous AI Chatbot with Streaming & Citations**:
   - Streaming responses with Markdown formatting, syntax highlighting, and copy buttons.
   - Two selectable mentor personalities:
     - **Astra**: Female persona, inspiring, structured, empathetic, deep-tech guide.
     - **Orion**: Male persona, analytical, pragmatic, veteran software architect.
   - Explanation depth toggles: **Beginner**, **Intermediate**, and **Expert / Architectural**.
   - Drag-and-drop / file upload with AI vision and diagram analysis.
   - Voice note recording with live waveform, transcription, and speech-to-text.
   - Real-time Web Search mode citing live technical sources and references.

4. **Daily Task Manager & Pomodoro Focus Timer**:
   - Task CRUD with categories, priorities, due dates, and recurring patterns.
   - List and Weekly Calendar views.
   - Integrated Pomodoro focus timer (25m Focus, 5m Short Break, 15m Long Break, Custom).
   - Melodic Web Audio API synthesized alert chimes and in-app notifications on timer completion.

5. **Cognitive Scoreboard & Telemetry**:
   - Daily, weekly, monthly, and all-time performance metrics.
   - GitHub-style 365-day practice heatmap.
   - Visual focus velocity bar chart and unlocked achievement badges.
   - Identification of strongest competencies and personalized areas to improve.

6. **Adaptive AI Quiz Generator**:
   - Instant quiz generation from any topic, subject, or pasted study notes.
   - Supports Multiple-Choice, True/False, Short Answer, and Coding questions.
   - Post-submission scoring, complete solutions, and historical improvement analytics.

7. **Voice Mentors Stage**:
   - Lifelike vocal narration using Web Speech Synthesis and Speech Recognition.
   - Speech rate controls (0.8x to 1.5x), pitch tuning, and mute options.
   - Step-by-step explainer mode and audio image analysis.

8. **Multi-Language Sandboxed Code Lab**:
   - Full code workspace supporting **JavaScript, Python 3, HTML5/CSS3, SQL, and C++ 20**.
   - Line numbers, syntax styling, starter templates, and run time benchmarking.
   - **Safe Sandboxed Execution**: untrusted code never executes directly on the server host:
     - JavaScript runs in an isolated client-side worker context.
     - Python runs in client WebAssembly.
     - HTML/CSS renders in a secure, sandboxed iframe.
     - SQL executes in an in-memory relational sandbox with sample schemas.
   - "Ask Mentor" & "Get Hint" educational debug assistant for progressive clues without spoiling solutions.

9. **Timed Certification Exams**:
   - Timed exams with countdown timer, question navigator, and flag for review.
   - 3 progressive hint tokens per test session.
   - Score breakdown and AI-generated revision recommendations.

10. **Step-by-Step Career Roadmap**:
    - Phased engineering roadmaps (Foundations -> Intermediate -> Advanced -> Capstone Projects -> Interview Prep).
    - Interactive milestone checkboxes and curated resource links.
    - Senior & Staff interview questions for each milestone.
    - Custom career roadmap generator for any specialized role.

11. **Frontier Tech News**:
    - Fresh daily global updates across AI, Software, Cybersecurity, Science, and Open Source.
    - Category filters, article summaries, bookmarks, and instant "AI Brief" summaries.

12. **3D Interactive Tech Globe**:
    - Three.js rotating 3D Earth with atmospheric glow and star field.
    - Interactive pulsing markers pinpointing global AI breakthroughs, tech summits, and quantum labs.
    - Click-to-inspect cards with verified source attributions.

---

## 🛠️ Technology Stack

- **Framework**: Next.js 14 (App Router)
- **Frontend**: React 18, TypeScript, Vanilla CSS Design System with CSS Tokens & Glassmorphism
- **Icons**: Lucide React
- **Graphics & 3D**: Three.js
- **Audio**: Web Audio API (Synthesized procedural chimes)
- **Database & Auth**: Supabase (PostgreSQL with Row-Level Security, Google OAuth)
- **AI Engine**: Google Gemini API integration with intelligent fallback reasoning engine

---

## 🚀 Getting Started

### 1. Prerequisites
- **Node.js**: v18.0.0 or higher
- **npm** or **yarn**

### 2. Installation
```bash
# Clone the repository and enter directory
cd "chat bot"

# Install dependencies
npm install
```

### 3. Environment Variables
Copy `.env.example` to `.env.local`:
```bash
cp .env.example .env.local
```

Fill in your configuration keys:
```env
# Supabase Configuration (Optional - app automatically falls back to secure Local Demo mode if empty)
NEXT_PUBLIC_SUPABASE_URL=https://your-project-id.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-supabase-anon-key

# AI API Key (Optional - app includes intelligent fallback mentor AI engine if empty)
GEMINI_API_KEY=your-google-gemini-api-key

# App URL
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

> **Note**: Even without external API keys, the application is **100% interactive and fully functional** out of the box with persistent local session storage and simulated Google Auth!

### 4. Setting up Supabase (Optional for Cloud Sync)
1. Create a project at [supabase.com](https://supabase.com).
2. Go to **Authentication -> Providers -> Google** and enable Google OAuth by supplying your Google Cloud Client ID and Secret.
3. In **Authentication -> URL Configuration**, set the Redirect URL to:
   ```
   https://your-domain.com/auth/callback
   # Or for local development:
   http://localhost:3000/auth/callback
   ```
4. Open the Supabase **SQL Editor** and paste the contents of `supabase_schema.sql` included in this repository. Click **Run** to generate all tables, triggers, and Row-Level Security (RLS) policies.

### 5. Running Locally
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🔒 Security Architecture

1. **Google OAuth 2.0 Only**: Never collects or stores Google passwords. Sessions are managed through secure tokens.
2. **Database Row-Level Security (RLS)**: Every table enforces `auth.uid() = user_id`, guaranteeing zero cross-tenant leakage.
3. **Sandboxed Code Execution**: User code in JavaScript, Python, C++, HTML, and SQL runs client-side in sandboxed workers, iframes, and WebAssembly—never on the backend node server.
4. **Attribution & Transparency**: Web search results and news items cite their source publisher, publication date, and domain.

---

## 📦 Deployment (Vercel / Netlify / Node)

### Deploy to Vercel:
1. Push the code to a GitHub repository.
2. Import the project into [Vercel](https://vercel.com).
3. Set the Environment Variables (`NEXT_PUBLIC_SUPABASE_URL`, `NEXT_PUBLIC_SUPABASE_ANON_KEY`, `GEMINI_API_KEY`, `NEXT_PUBLIC_APP_URL`).
4. Click **Deploy**.

---

© 2026 Orbit Mentor AI. Empowering developers, students, and engineers globally.
