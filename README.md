# Rafael Andrés García G.

Hi, I'm Rafael 👋

**AI implementation and automation for financial services, operations, and development programs** · LatAm + Africa

## What I do

I build AI workflows and automation systems that work in production. My focus is at the intersection of AI implementation, financial inclusion, and technical assistance programs: monitoring and scoring agents, document intelligence, and pipelines that remove repetitive work from a team's week.

## What you'll find here

This GitHub is a **portfolio of low/mid-code and AI integration work**, not traditional software engineering output. Most projects are built with combinations of:

- Claude Code / Cursor (frontend prototyping)
- Supabase (backend / data)
- N8N self-hosted (automation workflows)
- Claude API + OpenAI API (LLM systems)
- Python (basic, for scripts and data processing)

I came to software from finance and operations, which shapes how I work: I start from the business process, decide what's actually worth building, and then build it. I use AI assistants heavily in the process, and I own the architecture and the review.

## My background

- Over a decade in operations, finance, and project delivery, including corporate roles at multinational companies in Latin America
- Five years delivering projects for financial inclusion and technical assistance programs across Latin America and Africa, as project manager, financial modeler, and AI implementation specialist
- Co-author of "Maximizing the credit potential in Mexican financial cooperatives" (Portal FinDev, CGAP, 2023), 2nd most-read publication in 2023

## Get in touch

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/ragarciaga)

---

## Featured Projects

Systems I designed and built end to end, including the web application, the AI and automation backend, and the integrations between them. Only projects I own or have permission to show are named here; client work appears further down as capabilities, without names, data, or screenshots.

---

### 🎓 Maysachart - AI Trading Tutor
> Full-stack EdTech SaaS that teaches retail traders methodology through an AI tutor backed by 40+ proprietary documents.

**The problem:** Beginner traders buy courses but can't apply what they learned facing a real chart. Human mentoring doesn't scale, and existing tools offer signals, not education.

**What I built:** A freemium web platform where users chat with an AI tutor that retrieves answers from a vectorized knowledge base of trading methodology. The frontend handles auth, conversation management, market news filtered by tracked assets, and usage metering. The N8N backend handles JWT validation, plan-limit enforcement, RAG retrieval, prompt construction with conversation history, and response storage in one orchestrated workflow. A separate ingestion pipeline auto-processes new documents from Google Drive into the vector store.

**Integrations:** Supabase (Auth, PostgreSQL, pgvector, Storage), OpenAI (GPT-4.1 + embeddings), Google Drive, N8N

🔗 [Live app](https://maysachart.com)

![MaysaChart](https://raw.githubusercontent.com/ragarciaga/portfolio/main/maysachart.png)

---

### 🏢 Copain ERP - Cloud ERP for Colombian SMBs
> Full-stack cloud ERP covering sales, purchasing, inventory, treasury, payroll, and tax compliance, with automated IVA calculation.

**The problem:** A Colombian small business managed invoicing, inventory, and finances across disconnected spreadsheets and paper ledgers, with no automated tax calculation and no visibility into cash flow.

**What I built:** A modular web ERP with more than 12 functional areas. The sales flow goes from quotation to invoice to payment collection, with every transaction automatically creating treasury movements. Purchases follow the same pattern. Inventory updates in real time via Kardex entries on every sale or purchase. IVA (19%) is calculated and tracked automatically, with a dedicated tax report showing generated vs. deductible amounts. Role-based access (admin, accountant, sales, user) with Row-Level Security. Includes bulk data import for migration.

**Integrations:** Supabase (Auth, PostgreSQL, Edge Functions, RLS)

*Built for my own company.*

![Copain](https://raw.githubusercontent.com/ragarciaga/portfolio/main/copain_erp.png)

---

## Capabilities

Types of systems I design and build. Descriptions are generic by design: specific implementations are covered by confidentiality, so no client names, no client data, and no screenshots of client operations.

| Capability | What it does |
|---|---|
| **Multi-role operational platforms** | Order-to-delivery and workflow platforms with role-based portals, prepaid credit or limits, automatic routing, approvals, and real-time notifications. |
| **Spreadsheet-to-system migrations** | Replacing spreadsheet-driven operations with production systems: sales, inventory, treasury, and tax, connected and updated in real time. |
| **Guided financial modeling tools** | Web applications that turn structured business inputs into multi-year projections, with automated analysis of key metrics, findings, and recommendations. Also ingest existing models for structured review. |
| **Monitoring and scoring agents** | Scheduled agents that watch external sources, normalize what they find, classify it against defined criteria, deduplicate, and alert the team only when something needs a human decision. |
| **Document intelligence and RAG assistants** | Assistants that answer from an organization's own documents: extraction, chunking, vectorization, retrieval, and conversational memory. |
| **Advisory and simulation tools** | Single-screen tools for front-line staff: live product data, real-time amortization and savings calculations, branded PDF export, and an AI sidebar for questions. |
| **Compliance and tracking systems** | Ticketing and regulatory tracking with Kanban boards, templated email notifications, cron-based reminders, and audit logging. |
| **Bilingual program management apps** | Enrollment, purchases, claims lifecycle, and fund ledger applications for programs operating in more than one language and calendar system. |
| **Learning and engagement microsites** | Gamified education modules with video, infographics, quizzes, certificate generation, and lead capture. Invitation-based LMS with sequential unlocking. |
| **Conversational sales and education bots** | Guided multi-module flows and RAG-powered chat and Telegram bots for prospect education, with ROI simulators and scheduling CTAs. |
| **Voice and field data capture** | Voice notes to transcription to AI extraction to structured storage, built for teams working in the field. |
| **Survey and indicator collection** | Multi-organization wizards collecting text, audio, and file responses, with auto-save, admin panel, and webhook processing. |
| **Analytics dashboards** | Profitability and KPI dashboards with waterfall charts, cost attribution, and what-if simulators. |
| **Automated mailing systems** | Personalized batch email with templates, attachments, and send-status tracking. |

---

## Tech Stack

| Category | Technologies |
|---|---|
| **Frontend** | React 18, Next.js, TypeScript, Tailwind CSS, shadcn/ui, Recharts, Vite 5 |
| **Backend** | Supabase (PostgreSQL, Auth, Edge Functions, Storage, pgvector, RLS) |
| **AI / LLM** | OpenAI (GPT-4.1, GPT-4o-mini, Whisper, Embeddings), RAG pipelines |
| **Automation** | N8N (webhooks, scheduled triggers, AI agents, error handling) |
| **Integrations** | Google Drive, Google Sheets, Gmail, Telegram, Resend, Stripe, Firecrawl |
| **Export** | jsPDF, html2canvas, SheetJS (xlsx), CSV |

---

## 🛠️ Languages & Tools

<p align="left">
  <img src="https://img.shields.io/badge/N8N-EA4B71?style=for-the-badge&logo=n8n&logoColor=white"/>
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"/>
  <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white"/>
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white"/>
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white"/>
</p>

---

## Let's Talk

I work with organizations that need to go from manual processes to automated, AI-enhanced systems, and want someone who can own the full delivery: diagnosis, architecture, build, and deployment.

🔗 **[Connect on LinkedIn](https://linkedin.com/in/ragarciaga)**

---

*Last updated: August 2026*
