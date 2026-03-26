# Rafael García Gallego

**AI Automation & Business Process Consultant**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/ragarciaga)

---

I build the full stack behind business automation — the web application, the AI backend, and the workflow engine that connects them. I work with clients in financial services, logistics, agriculture, and education across the US, Latin America, and the Caribbean. Most of my projects replace spreadsheet‑driven operations with production systems that run with minimal manual intervention.

Previously, I held corporate roles at multinational companies in Latin America. I now focus on applied AI consulting, where I design and deliver automation solutions for organizations ranging from credit unions to international development programs.

---

## Featured Projects

These are end-to-end systems I designed and built — including the web application, the AI/automation backend, and the integrations between them.

---

### 🎓 Maysachart — AI Trading Tutor
> Full-stack EdTech SaaS that teaches retail traders methodology through an AI tutor backed by 40+ proprietary documents.

**The problem:** Beginner traders buy courses but can't apply what they learned facing a real chart. Human mentoring doesn't scale, and existing tools offer signals, not education.

**What I built:** A freemium web platform ($9.99/month) where users chat with an AI tutor that retrieves answers from a vectorized knowledge base of trading methodology. The frontend handles auth, conversation management, market news filtered by tracked assets, and usage metering. The N8N backend handles JWT validation, plan-limit enforcement, RAG retrieval, prompt construction with conversation history, and response storage in one orchestrated workflow. A separate ingestion pipeline auto-processes new documents from Google Drive into the vector store.

**Integrations:** Supabase (Auth, PostgreSQL, pgvector, Storage), OpenAI (GPT-4.1 + embeddings), Google Drive, N8N

🔗 [Live app](https://maysachart.com)

![MaysaChart](https://raw.githubusercontent.com/ragarciaga/portfolio/main/screenshots/maysachart.png)

---

### 📊 Financial Modeling Assistant
> AI-powered platform that lets entrepreneurs create investor-ready 5-year financial projections in minutes — or upload existing models for automated analysis.

**The problem:** Early-stage founders in Latin America's accelerator ecosystem lack the financial modeling expertise to build structured forecasts. Existing tools are too complex, too generic, or too expensive.

**What I built:** A guided web application with sector-specific workflows (SaaS, Marketplace, E-commerce, and several other verticals). Users fill in business inputs through a 5-tab form; the N8N backend (3 workflows) processes the data, generates a complete projection in Google Sheets, and returns AI-generated analysis with key metrics, findings, and recommendations. A second path lets users upload existing Excel/PDF models — the backend extracts, chunks, and vectorizes the content, then runs an AI agent to produce structured analysis. A persistent chat agent answers follow-up questions using the model's context and conversation memory.

**Integrations:** Supabase (PostgreSQL, pgvector, Storage), OpenAI (GPT-4o-mini + embeddings), Google Drive, Google Sheets, N8N

![Financial Modeling Tool](https://raw.githubusercontent.com/ragarciaga/portfolio/main/screenshots/jta_modeling_tool.png)

---

### 🚢 Caribbean Xpress — Shipping Management Platform
> Multi-role logistics platform for Caribbean food package delivery, serving agents, fulfillment partners, and administrators across 4 portals.

**The problem:** A food shipping operation across the Caribbean ran on spreadsheets, phone calls, and WhatsApp — leading to lost orders, credit disputes, and no visibility into fulfillment status.

**What I built:** A complete order-to-delivery platform with 4 role-based portals. Agents place orders through a guided wizard that auto-deducts from their prepaid credit. Orders route automatically to the fulfillment company matching the receiver's region. Master agents oversee agent networks. Admins manage the full ecosystem: credit limits, commissions, packages, analytics, and change request approvals. Includes real-time notifications via Supabase Edge Functions.

**Integrations:** Supabase (Auth, PostgreSQL, Edge Functions, RLS, Realtime), Resend (email)

![Caribbean](https://raw.githubusercontent.com/ragarciaga/portfolio/main/screenshots/caribbean_xpress.png)

---

### 🏢 Copain ERP — Cloud ERP for Colombian SMBs
> Full-stack cloud ERP covering sales, purchasing, inventory, treasury, payroll, and tax compliance — with automated IVA calculation.

**The problem:** A Colombian small business managed invoicing, inventory, and finances across disconnected spreadsheets and paper ledgers — with no automated tax calculation and no visibility into cash flow.

**What I built:** A modular web ERP with more than 12 functional areas. The sales flow goes from quotation to invoice to payment collection, with every transaction automatically creating treasury movements. Purchases follow the same pattern. Inventory updates in real-time via Kardex entries on every sale or purchase. IVA (19%) is calculated and tracked automatically, with a dedicated tax report showing generated vs. deductible amounts. Role-based access (admin, accountant, sales, user) with Row-Level Security. Includes bulk data import for migration.

**Integrations:** Supabase (Auth, PostgreSQL, Edge Functions, RLS)

![Copain](https://raw.githubusercontent.com/ragarciaga/portfolio/main/screenshots/copain_erp.png)

---

### 🔍 Procurement Opportunity Scanner
> Automated pipeline that monitors international development procurement portals and classifies opportunities using AI.

**The problem:** A global consulting firm needed to scan several portals daily. Manual monitoring across multiple sources meant opportunities were missed and the process consumed significant team time each week.

**What I built:** A scheduled N8N workflow that scrapes procurement portals (through API's, plus web scraping via Firecrawl for additional sources), normalizes the results into a common structure, runs each opportunity through an OpenAI-powered classifier configured around the firm’s focus areas, logs qualified matches to a Google Sheet with structured metadata (deadline, country, sector, relevance score), and sends an email digest when new opportunities are found. Includes deduplication against previously seen listings.

**Integrations:** Platforms API, Firecrawl, OpenAI, Google Sheets, Gmail

 ![Procuremen](https://raw.githubusercontent.com/ragarciaga/portfolio/main/screenshots/procurement_scanner.png)

---

### 💳 ConsolidApp — Credit Advisory Tool
> Real-time debt-consolidation simulator for branch advisors at a Mexican credit union, with AI-powered assistant.

**The problem:** Branch advisors at a Mexican credit union spent 15-30 minutes per client manually looking up bureau data, calculating loan scenarios in Excel, and preparing proposals. The process was slow, inconsistent across branches, and error-prone.

**What I built:** A single-screen advisory tool where advisors search a member by ID and instantly see their full credit profile (score, debts, payments, classification). They select a credit product from a live database, input amount and term, and get real-time amortization tables with monthly/annual savings calculations. Results export as branded PDFs. An AI sidebar (OpenAI via Supabase Edge Function) answers questions about products and consolidation strategy. Deployed across five pilot branches.

**Integrations:** Supabase (PostgreSQL, Edge Functions), OpenAI, jsPDF

![Consolidapp](https://raw.githubusercontent.com/ragarciaga/portfolio/main/screenshots/consolidapp.png)

---

## More Projects

| Project | Type | What it does |
|---|---|---|
| **Ticket Tracker** | Web App | Ticket management + regulatory compliance tracking for a Mexican financial services company. Kanban board, 8 email notification templates, cron-based reminders, audit logging. |
| **Resilience+** | Web App | Bilingual (EN/Nepali) cooperative insurance management for agricultural programs in Nepal. Member enrollment, crop purchases, claims lifecycle, fund ledger with Bikram Sambat calendar. |
| **AkibaBot** | Web App | AI sales chatbot for a fintech company — 5-module guided flow with GPT-4.1, embedded videos, ROI simulator, and call scheduling CTA. |
| **Reto Akiba** | Web App | Gamified financial education microsite — 5 modules with video, infographics, drag-and-drop quizzes, certificate generation, and lead capture. |
| **Escuela CVI** | Web App | Private LMS for a ministry organization — invitation-based access, sequential course unlocking, student reflections, certificate issuance. |
| **Impact Indicators** | Web + N8N | Multi-org survey wizard collecting text, audio, and file responses on KPI preferences — with auto-save, admin panel, and webhook processing. |
| **Finmetrics** | Prototype | Profitability analytics dashboard for credit unions — waterfall charts, cost attribution, what-if simulators. Bilingual (EN/ES). *Demo data only.* |
| **Gestiactivos** | Prototype | CMMS for healthcare biomedical equipment — asset lifecycle, PM scheduling, service requests (Kanban), KPI dashboard. *Client-side only.* |
| **Akiba Telegram Bot** | N8N | RAG-powered Telegram bot for prospect education on employee savings plans — vector retrieval + GPT-4o-mini responses. |
| **Voice-to-Data Logger** | N8N | Telegram voice notes → Whisper transcription → AI data extraction → Google Sheets. Built for agricultural field teams. |
| **Automated Mailing** | N8N | Personalized batch email system for corporate campaigns — template-based with attachments and send-status tracking. |

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

I work with organizations that need to go from manual processes to automated, AI-enhanced systems — and want someone who can own the full delivery: diagnosis, architecture, build, and deployment.

🔗 **[Connect on LinkedIn](https://linkedin.com/in/ragarciaga)**

---

*Last updated: March 2026*
