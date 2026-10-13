# Rafael Andrés García G.

Hi, I'm Rafael 👋

**Less repetitive work. More judgment where it matters.** AI and automation for operations teams · Financial services · LatAm + Africa

## What I do

I build automation and AI systems that run in production: monitoring and scoring agents, document intelligence, and pipelines that take repetitive work out of a team's week. Most of it is for operations and finance teams in emerging markets, where the data is dirty, the budget is a fraction of what the case assumes, and the system has to keep working after the consultant leaves.

## What you'll find here

This GitHub is a portfolio of low/mid-code and AI integration work. I came to software from finance and operations, which shapes how I work: I start from the business process, decide what is worth building, and own the architecture and the review.

Most projects are built with combinations of:

- Claude Code / Cursor (frontend prototyping)
- Supabase (backend / data)
- N8N self-hosted (automation workflows)
- Claude API + OpenAI API (LLM systems)
- Python (basic, for scripts and data processing)

I use AI assistants heavily in the process. The decisions about what to build, and what to leave alone, are mine.

## My background

- Over a decade in operations, finance, and project delivery, including corporate roles at multinational companies in Latin America
- Five years delivering projects for financial inclusion and technical assistance programs across Latin America and Africa, as project manager, financial modeler, and AI implementation specialist
- Co-author of "Maximizing the credit potential in Mexican financial cooperatives" (Portal FinDev, CGAP, 2023), 2nd most-read publication in 2023

## Get in touch

🔗 [maysasp.com](https://maysasp.com) · [LinkedIn](https://linkedin.com/in/ragarciaga)

---

## Featured Projects

Systems I designed and built end to end, including the web application, the AI and automation backend, and the integrations between them. Only projects I own or have permission to show are named here. Client work appears further down as case notes and capabilities, without names, data, or screenshots.

---

### 🏢 Copain ERP - Cloud ERP for Colombian SMBs
> Full-stack cloud ERP covering sales, purchasing, inventory, treasury, payroll, and tax compliance, with automated IVA calculation.

**The problem:** A Colombian small business managed invoicing, inventory, and finances across disconnected spreadsheets and paper ledgers, with no automated tax calculation and no visibility into cash flow.

**What I built:** A modular web ERP with more than 12 functional areas. The sales flow goes from quotation to invoice to payment collection, with every transaction automatically creating treasury movements. Purchases follow the same pattern. Inventory updates in real time via Kardex entries on every sale or purchase. IVA (19%) is calculated and tracked automatically, with a dedicated tax report showing generated vs. deductible amounts. Role-based access (admin, accountant, sales, user) with Row-Level Security. Includes bulk data import for migration.

**Integrations:** Supabase (Auth, PostgreSQL, Edge Functions, RLS)

*Built for my own company.*

![Copain](https://raw.githubusercontent.com/ragarciaga/portfolio/main/copain_erp.png)

---

### 🪨 Rockbuilt - A development harness for AI coding agents
> You decide what to build. Rockbuilt plans it, builds it, has it reviewed by agents that did not write it, and stops to ask you only for design decisions, anything that costs money, and changes that are hard to undo.

**The problem:** AI coding agents fail in predictable ways. They build the wrong thing from a vague request, grade their own work, forget everything between sessions, and spend money or touch production while nobody is watching.

**What I built:** A planner that writes one plan per task with its risk tier and costs. An implementer that writes code and tests but cannot touch git, GitHub or secrets. A verifier that plants bugs on purpose to prove the tests catch them. A blind auditor that tests the running software without seeing the plan or the code. And a merge gate written in code, so low-risk work merges on its own and anything costly or risky waits for a person.

**Stack:** Claude Code, Cursor, Node.js, GitHub Actions, Playwright

🔗 [Repository](https://github.com/ragarciaga/rockbuilt)

---

### 🎓 Maysachart - AI Trading Tutor
> Full-stack EdTech SaaS that teaches retail traders methodology through an AI tutor backed by 40+ proprietary documents.

**The problem:** Beginner traders buy courses but can't apply what they learned facing a real chart. Human mentoring doesn't scale, and existing tools offer signals, not education.

**What I built:** A freemium web platform where users chat with an AI tutor that retrieves answers from a vectorized knowledge base of trading methodology. The frontend handles auth, conversation management, market news filtered by tracked assets, and usage metering. The N8N backend handles JWT validation, plan-limit enforcement, RAG retrieval, prompt construction with conversation history, and response storage in one orchestrated workflow. A separate ingestion pipeline auto-processes new documents from Google Drive into the vector store.

**Integrations:** Supabase (Auth, PostgreSQL, pgvector, Storage), OpenAI (GPT-4.1 + embeddings), Google Drive, N8N

🔗 [Live app](https://maysachart.com)

![MaysaChart](https://raw.githubusercontent.com/ragarciaga/portfolio/main/maysachart.png)

---

## Case notes

Client work, written the way I write about it publicly: no names, no client data, no screenshots of their operation. The architecture and the numbers are real.

---

### Receivables and payables · Colombian SMB

**Before:** One person entering every purchase and every sale by hand, about three hours a day, on the single desktop computer that could open the accounting program. Around 60 hours a month. The manager had to walk to that machine to know what he was owed.

**What I built:** Colombian electronic invoicing requires every invoice as a PDF and an XML. Supplier invoices arrive by email, a Gmail filter forwards them to a dedicated mailbox the workflow is allowed to read, and the XML is parsed straight into a sheet. The company's main inbox never gets connected to the automation. Withholding rules (retención en la fuente, ICA, IVA) are encoded per client so the payable amount is exact. A generated page behind a username and password reads the sheet, so the position is current from any device. A weekly summary goes out by email, plus an alert on every invoice that comes due and a reminder every five days it stays overdue. Any client's statement of account exports as a branded PDF, ready to send.

**After:** Around 10 hours a month. No AI calls, so no per-run cost. It runs on a server that was already paid for, so no new infrastructure. Handed over with the repository, so the team can change it themselves from Claude Code.

**What stayed manual, on purpose:** Sales invoices. The issuing portal will not copy a second address, so someone uploads the zip to a folder and the folder triggers the rest. About thirty seconds per sale. Automating around that would mean driving a browser against a portal that changes, inside the one process where a wrong number becomes a tax problem.

---

### Expense categorization · consulting firm

**The request:** Pull expense and contractor fee data out of a time tracking tool, reshape it, and push it into the accounting system every month.

**What I did not build:** The categorization. Every expense had to be assigned a category, and the answer changed depending on the project, the funder and how the contract was written. One person had read the contracts, and that judgment was his.

**What I built instead:** A script inside the spreadsheet the team already used. It pulls, reshapes, and hands over a file in the exact format the accounting system expects. No workflow engine, no model, no API cost. The categorization stayed with the person who could do it.

---

## Capabilities

Types of systems I design and build. Descriptions are generic by design: specific implementations are covered by confidentiality, so no client names, no client data, and no screenshots of client operations.

| Capability | What it does |
|---|---|
| **Spreadsheet-to-system migrations** | Replacing spreadsheet-driven operations with production systems: sales, inventory, treasury, and tax, connected and updated in real time. |
| **Multi-role operational platforms** | Order-to-delivery and workflow platforms with role-based portals, prepaid credit or limits, automatic routing, approvals, and real-time notifications. |
| **Monitoring and scoring agents** | Scheduled agents that watch external sources, normalize what they find, classify it against defined criteria, deduplicate, and alert the team only when something needs a human decision. |
| **Document intelligence and RAG assistants** | Assistants that answer from an organization's own documents: extraction, chunking, vectorization, retrieval, and conversational memory. |
| **Guided financial modeling tools** | Web applications that turn structured business inputs into multi-year projections, with automated analysis of key metrics, findings, and recommendations. Also ingest existing models for structured review. |
| **Advisory and simulation tools** | Single-screen tools for front-line staff: live product data, real-time amortization and savings calculations, branded PDF export, and an AI sidebar for questions. |
| **Compliance and tracking systems** | Ticketing and regulatory tracking with Kanban boards, templated email notifications, cron-based reminders, and audit logging. |
| **Analytics dashboards** | Profitability and KPI dashboards with waterfall charts, cost attribution, and what-if simulators. |
| **Bilingual program management apps** | Enrollment, purchases, claims lifecycle, and fund ledger applications for programs operating in more than one language and calendar system. |
| **Voice and field data capture** | Voice notes to transcription to AI extraction to structured storage, plus multi-organization survey wizards collecting text, audio, and file responses. Built for teams working in the field. |

---

## Tech Stack

| Category | Technologies |
|---|---|
| **Frontend** | React 18, Next.js, TypeScript, Tailwind CSS, shadcn/ui, Recharts, Vite 5 |
| **Backend** | Supabase (PostgreSQL, Auth, Edge Functions, Storage, pgvector, RLS) |
| **AI / LLM** | Claude API, OpenAI (GPT-4.1, GPT-4o-mini, Whisper, Embeddings), RAG pipelines |
| **Automation** | N8N (webhooks, scheduled triggers, AI agents, error handling), Google Apps Script |
| **Integrations** | Google Drive, Google Sheets, Gmail, Telegram, Resend, Stripe, Firecrawl |
| **Export** | jsPDF, html2canvas, SheetJS (xlsx), CSV |

---

## Let's Talk

I work with organizations that want to move from manual processes to systems that run on their own, and that want someone who owns the whole thing: diagnosis, architecture, build, and what happens after it is deployed.

🔗 [maysasp.com](https://maysasp.com) · [LinkedIn](https://linkedin.com/in/ragarciaga)

---

*Last updated: October 2026*
