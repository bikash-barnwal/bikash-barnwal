<h1 align="center">Hi, I'm Bikash Prasad Barnwal 👋</h1>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=22&pause=1200&color=36BCF7&center=true&vCenter=true&width=720&lines=Full+Stack+Software+Engineer;I+build%2C+ship+and+run+production+software;AI-assisted+speed.+Human-owned+design.;Merged+PRs+in+Apache+Superset+and+OpenWind" alt="Typing SVG" />
</p>

<p align="center">
  <a href="https://heybikash.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/in/bikash-prasad-barnwal/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://x.com/bikash_barnwal_"><img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white" alt="X (Twitter)" /></a>
  <a href="https://bento.me/bikash-prasad-barnwal"><img src="https://img.shields.io/badge/Bento-000000?style=for-the-badge&logo=about.me&logoColor=white" alt="Bento" /></a>
  <a href="mailto:bikashprasadbarnwal@gmail.com?subject=Exploring%20Potential%20Collaboration%20Opportunities"><img src="https://img.shields.io/badge/Email-F9CA24?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

---

## 🧭 About

I'm a **Full Stack Software Engineer** at **JMV LPS Ltd.** I design, build, test, deploy and maintain web apps on my own, from the first schema to the production server.

- 🏗️ **Frontend:** React, Next.js, TypeScript, Tailwind CSS
- ⚙️ **Backend:** FastAPI, Node.js, PostgreSQL, Redis, Kafka
- 🚢 **Ship and run it:** Docker, Nginx, CI/CD on Ubuntu, with tracing, logs and metrics built in
- 🤖 **AI:** I use AI to code faster, but I design the systems myself and never hand decisions to it
- 🔐 **Security:** SSO (OIDC), role-based access control (RBAC), secret management

| | |
|---|---|
| ⏱️ **Experience** | 1+ year professional (since Oct 2025), 2160+ hours of hands-on coding |
| 🏭 **In production** | 10+ services deployed and maintained on Ubuntu servers |
| 📦 **Largest build** | Asset system tracking 1,500+ physical assets |
| 🤝 **Open source** | Merged PRs in Apache Superset and OpenWind |
| 🌍 **Based in** | India |

---

## 🚀 What I've Built (at JMV LPS)

| Project | What it does | Stack |
|---|---|---|
| **Asset Management System** | Maintenance for 1,500+ physical assets: QR-based tracking, custody records, analytics, PDF reports. OpenTelemetry traces errors and slow requests back to their source. | React · FastAPI · PostgreSQL |
| **Multi-tenant Notification Platform** | Sends messages for multiple tenants with delivery-status webhooks. Prometheus and Grafana dashboards surface failed or stuck messages early. | FastAPI · Kafka · Redis · PostgreSQL |
| **Self-hosted AI Service** | Open-source LLMs (Gemma 4, Qwen3) running on company servers. In-house apps call them over REST at zero per-call cost. Health and response times are tracked in real time. | Ollama · REST APIs |
| **WhatsApp Cloud API** | Taken from approval to production: Meta Business verification, App Review (legal, consent, privacy), then integration into company apps. | WhatsApp Cloud API · Meta Business |
| **SSO + RBAC** | Single sign-on and role-based access across internal applications. | Zitadel · OIDC |
| **Company Websites** | SEO-optimized, responsive sites deployed with Docker and Nginx. | Docker · Nginx |

---

## 🤝 Open Source: Merged Pull Requests

### [Apache Superset](https://github.com/apache/superset)

| PR | What I fixed |
|---|---|
| [#43192](https://github.com/apache/superset/pull/43192) | **fix(echarts): emit no cross-filter for clicks that are not categories.** Clicking a pie chart's Total text, its aggregated "Other" slice, or an unnamed sector sent a cross-filter with no dimension values, so downstream charts filtered on nothing. The fix emits no cross-filter for those clicks. |

### [OpenWind](https://github.com/TinyPhi/OpenWind) (open-source, self-hostable business platform, TypeScript)

**🔐 Secrets management with OpenBao (ADR-023)**

| PR | What it does |
|---|---|
| [#912](https://github.com/TinyPhi/OpenWind/pull/912) | Proposed ADR-023: OpenBao as the secrets manager |
| [#935](https://github.com/TinyPhi/OpenWind/pull/935) | Hardened the OpenBao client: request timeout, retry with backoff, token renewal, re-login on 403, shared login across concurrent callers; added production guards |
| [#936](https://github.com/TinyPhi/OpenWind/pull/936) | Kept bootstrap secrets out of `.env.local` in production |
| [#938](https://github.com/TinyPhi/OpenWind/pull/938) | Added OpenBao startup loaders and prepared the compose setup |
| [#939](https://github.com/TinyPhi/OpenWind/pull/939) | Production compose override: per-service credential files with mode 0600 |
| [#940](https://github.com/TinyPhi/OpenWind/pull/940) | OpenBao secrets runbook and production notes |

**🛡️ Superset security and audit (reporting integration)**

| PR | What it does |
|---|---|
| [#790](https://github.com/TinyPhi/OpenWind/pull/790) | Superset now refuses to start if database connections could be pooled across tenants (NullPool guard, with tests) |
| [#1069](https://github.com/TinyPhi/OpenWind/pull/1069) | Docs: recorded Superset secrets in OpenBao |
| [#1070](https://github.com/TinyPhi/OpenWind/pull/1070) | Bounded the export SQL lookup and added the database name to audit rows |

**🧹 User data erasure**

| PR | What it does |
|---|---|
| [#1100](https://github.com/TinyPhi/OpenWind/pull/1100) | Worker erases a user's Superset data automatically and retries until done |
| [#1101](https://github.com/TinyPhi/OpenWind/pull/1101) | Admin UI: erase a user from the users page with a typed confirmation |

---

## 🔁 How I Ship

```mermaid
flowchart LR
    A[Design<br/>I own it] --> B[Build<br/>AI-assisted]
    B --> C[Test<br/>unit · integration · API]
    C --> D[Review<br/>every change]
    D --> E[Deploy<br/>Docker · Nginx · CI/CD]
    E --> F[Observe<br/>traces · logs · metrics]
    F -.root-cause fixes.-> A
```

- **Observability:** OpenTelemetry tracing, Loki centralized logging, Tempo distributed tracing, Prometheus metrics, Grafana dashboards
- **Quality:** I write unit, integration and API tests, and review every change before release
- **Decisions:** AI speeds up the typing. Architecture and production calls stay with me.

---

## 🛠️ Tech Stack

**Languages:**
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)

**Frontend:**
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**Backend:**
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=flat-square&logo=graphql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)

**Data and messaging:**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)

**DevOps and observability:**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![CI/CD](https://img.shields.io/badge/CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)

**AI / LLM:**
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)

Also: RAG pipelines, vector databases, Zitadel, OpenBao, Apache Superset, Shopify Liquid, Cloudinary, Vercel, Render, Netlify

---

## 💼 Experience

**Full Stack Software Engineer · JMV LPS Ltd.** (Mar 2026 – Present)
Asset Management System, notification platform, self-hosted AI service, WhatsApp Cloud API, SSO and RBAC, company websites, and 10+ production services with centralized logging and tracing.

**Software Engineer · Codem Inc., Chennai** (Oct 2025 – Mar 2026)
Built secure backend endpoints and authentication workflows. Built reusable Shopify Liquid sections and snippets, and refactored theme components for maintainability and page performance.

---

## 🔥 Personal Projects

### [CropConnect](https://crop-connect-zeta.vercel.app/) (MERN)
A real-time marketplace that connects buyers and vendors with farmers.

- 🔐 JWT authentication, password reset via email, role-based access for Farmers and Buyers
- 📬 Email alerts via NodeMailer
- 🌤️ Live weather updates from real-time APIs
- 🌽 Crop listings with images, descriptions and pricing, plus filtering and sorting by name, price and category
- ⏱️ Rate limiter: max 25 requests per 15 minutes
- 🤳 Profile images with Multer + Cloudinary

### [OKR Tracker](https://okr-trackerxvte.onrender.com)
A team goal tool for setting OKRs and tracking progress across a team.

---
## 📊 GitHub Stats

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/bikash-barnwal/bikash-barnwal/output/github-contribution-grid-snake-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/bikash-barnwal/bikash-barnwal/output/github-contribution-grid-snake.svg">
    <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/bikash-barnwal/bikash-barnwal/output/github-contribution-grid-snake.svg">
  </picture>
</p>
---

## 🎓 Learning

- PG Certificate in Cyber Security, IGNOU (pursuing)
- Full Stack Web Development, Masai School (2024 – 2025)
- B.Sc. Mathematics (Honours), TDB College (2020 – 2024)
- Currently going deeper into LLM hosting, RAG systems and production observability
- 🧩 50 days of LeetCode completed

---

<p align="center"><b>Let's build something extraordinary together.</b></p>
