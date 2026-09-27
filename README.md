# Hi, I'm Rovs (Rovince Eduvane)

I'm a Machine Learning Engineer Intern on GCash's Trust & Security team, based in Metro Manila, Philippines. Outside work I build and ship apps, solo and with hackathon teams, much of it applied AI for classrooms and Filipino micro-businesses. Three are live: [KayaMo](https://www.kayamo.fit), [KitaMo](https://kitamo.online) and [HTTYD-PE](https://httyd-pe.vercel.app).

## Currently

- **Machine Learning Engineer Intern, Trust & Security, GCash** (Jun 2026 to present). I convert trained ML artifacts into production-scale pipelines for fraud detection and validate them for production readiness. Python, SQL, Apache Airflow, Kafka, MLflow, GitLab, AWS.
- **De La Salle University Manila**: BS Applied Economics, major in Financial Economics, minor in Data Science (expected 2027).
- **Volunteer Technology Lead, Acts 242 Church of Christ**: launched [acts242churchofchrist.com](https://acts242churchofchrist.com) in April 2026.

Before this: AI Data Trainer (contract) at Invisible Technologies, supporting an OpenAI project (2021 to 2022).

## Featured projects

| Project | What it does | Built with |
| --- | --- | --- |
| **KayaMo**<br>[kayamo.fit](https://www.kayamo.fit) · [repo](https://github.com/RawBeans02/KayaMo-web) | Meal, workout and daily-plan tracker with Filipino foods and Taglish built in. The AI assistant, Lis, drafts food entries from text or a photo. Nutrition numbers come from USDA, Open Food Facts and a curated Philippine dataset, never from the model, and nothing Lis drafts is saved until you confirm. Entries are written to the device first and synced later. | Next.js, TypeScript, Supabase, OpenAI (Vercel AI SDK), Zod, Dexie |
| **KitaMo**<br>[kitamo.online](https://kitamo.online) · [Android repo](https://github.com/kitamo-ph/owner-seller-mobile) · [site repo](https://github.com/kitamo-ph/website) | Business app for sari-sari (neighborhood convenience) stores and karinderias (small eateries). The public repo is the Android app, being prepared for Google Play internal testing: sales, stock, recipe costing, cost of goods and net profit, stored only on the device. Checkout runs in an exclusive SQLite transaction with a unique checkout token, so a retry can't deduct stock or issue a receipt twice. | Android app: React Native, Expo, SQLite |
| **HTTYD-PE** (How To Train Your Dragon: Prompt Engineering)<br>[live](https://httyd-pe.vercel.app) · [repo](https://github.com/RawBeans02/HTTYD-PE) | Classroom game: students write prompts to recreate an AI-generated dragon, vote in real time, and a vision model scores each image. A parallel generation queue claims jobs atomically, each game has image and player caps, and starting a real game needs a host access code (practice games never call OpenAI). | Next.js, Supabase Realtime, OpenAI image generation and vision |
| **Basa Buddy**<br>[live demo](https://open-ai-build-week2026.vercel.app) · [repo](https://github.com/RawBeans02/basa-buddy) | Bilingual (English/Filipino) adaptive reading check for Grades 1 to 3, built by a four-person team at OpenAI Build Week 2026. My part: the client-side 2PL IRT engine with EAP estimation (the test keeps going when the connection drops), the 36-item bilingual item bank, and the authoring and validation scripts. Whisper scores one read-aloud sentence on the server, and the step is skipped if the mic or network fails. Voice prompts need the network and are currently off on the hosted demo. | Next.js PWA, TypeScript, OpenAI Whisper |
| **CarinderAI**<br>[hack-sprint demo](https://carinder-ai.vercel.app) · [repo](https://github.com/RawBeans02/CarinderAI) | Operations app for carinderia owners, built by Team CarinderAI at the Cursor Manila Hack Sprint 2026, where it placed 3rd. The demo is the hack-sprint build: photograph a handwritten palengke (wet-market) list and a vision model turns it into an editable supplier order. The app on `main` (runs locally) adds a camera point of sale and automatic journaling of sales and expenses. | Next.js, TypeScript, OpenAI vision; Prisma on `main` |
| **Finance Project: Quant, Risk and Macro Analytics**<br>[repo](https://github.com/RawBeans02/finance-analytics-portfolio) | Python finance analytics: IFRS 9-style credit-risk ECL engine, portfolio optimization and CAPM, fixed-income risk (duration, DV01), Philippine inflation nowcasting dashboard, DuckDB market-data pipeline, and a retrieval-based research memo tool with citation checks. | Python, pandas, scikit-learn, Streamlit, DuckDB |

## How I build

- LLM output is schema-validated with Zod (KayaMo, CarinderAI). The numbers that matter come from sourced data or deterministic code: nutrition in KayaMo, and ability estimates in Basa Buddy, where the server re-runs the estimate instead of trusting the client.
- Local-first where connectivity is unreliable: the KitaMo Android app keeps everything on the device; KayaMo writes to IndexedDB first and syncs later; Basa Buddy's adaptive test keeps running offline (voice prompts and read-aloud need a connection).
- HTTYD-PE gates real (paid) games behind a host access code, caps images and players per game, puts a timeout on every OpenAI call, and lets the host retry or skip stuck image jobs.
- In KayaMo, nothing the AI drafts is saved until the user confirms. Acts242 Studio routes AI output through approvals and evaluator gates.

## Other work

- **Acts242 Studio** (private): AI media workflows with human approval steps, covering faster-whisper transcription, sermon clips, RAG over sermon materials, and evaluator gates.
- **CourseKin** (in development): AI study companion that turns course materials into summaries, quizzes, flashcards and spaced-review cards. FastAPI + Next.js.
- **[Rune Rush](https://github.com/RawBeans02/Rune-Rush)**: browser roguelite prototype with four classes, stage waves and bosses. Vite, React, TypeScript, Canvas.
- **Academic work**: China-U.S. volatility spillovers (VAR, Diebold-Yilmaz), VAR macro-shock analysis, and portfolio optimization with CAPM.

## Recognition

- **2nd Prize**, Philippine Datathon 2023 (Team Liver Ready)
- **3rd Place**, Cursor Manila Hack Sprint 2026 (Team CarinderAI, built CarinderAI)
- **3rd Place**, Henkel Philippines "Loctite Reimagined" Hackathon 2026 (Team Hackatinkers, brand strategy)

Also competed in OpenAI Build Week 2026 (Basa Buddy), BPI D.A.T.A. Wave (2023 to 2025), PJDSC (2023 to 2024), and the GenAI PH Builders Agentic Hackathon 2025.

## Tech

- **Languages:** Python, SQL, TypeScript, R
- **ML and data:** pandas, scikit-learn, PyTorch, XGBoost
- **ML pipelines:** MLflow, Apache Airflow, Kafka
- **Applied AI:** OpenAI API, Claude API and MCP, Whisper, RAG, agent orchestration, evaluator design
- **Apps:** FastAPI, Next.js, React, React Native / Expo
- **Infra and media:** Supabase, Vercel, AWS, Cloudflare, FFmpeg

## Certifications

- **NVIDIA:** Fundamentals of Deep Learning (2025)
- **DataCamp:** Associate Data Scientist in Python (2023), plus 23 courses
- **Anthropic:** 8 courses, including Building with the Claude API and Intro to Model Context Protocol (2026)

## Connect

The quickest way to reach me is [LinkedIn](https://www.linkedin.com/in/rovince-eduvane).
