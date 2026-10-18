# Hey, I'm Jorge Rodriguez

**Founder & Full-Stack AI Platform Engineer** at [Florida Hitech Services](https://floridahitech.com) — Miami, FL

I build production AI platforms end to end: multi-tenant SaaS where AI agents do real work for small businesses — answering phone calls, booking appointments, processing documents — and the multi-agent system that builds them.

---

### What I'm building

📞 **Mely — AI phone receptionist for small businesses** *(live in production)*
Answers the calls a business misses, in English and Spanish, using only the business's real information — then takes a message, books an appointment or transfers the call.
- Voice AI agent with swappable language models, chosen per business from the admin console
- Books appointments in its own calendar or in the business's booking system
- Multi-tenant by design: row-level security, and the tenant always comes from the authenticated call — never from the AI
- Nothing is lost silently: every webhook is verified, stored and processed in the background; every side effect is idempotent
- Guardrails against phone manipulation, server-side checks the AI cannot bypass, and an adversarial test battery every prompt version must pass before it ships
- Owner panel (messages, calls, transcripts, recordings, agenda) and admin console (one-click onboarding, per-call costs and usage)

🏭 **Agent Factory — an orchestration layer above the agent harness** *(builds the projects here)*
A coding-agent harness runs one agent. The Factory runs a team of them: it turns a feature request into reviewed pull requests.
- An architect agent reads the repo and writes a machine-validated contract first — schema, routes, file-by-file split, every migration with its rollback — before any parallel work starts
- 16 specialist agents (data, backend, frontend, security, legal, payments, copy, SEO, infra, review…) wake only when the contract needs them, in waves, each owning its own files: collisions are caught before a merge, not after
- Every branch passes the same verification as CI; an integrator merges in order and re-verifies; an independent AI reviewer checks before anything ships
- It learns: every manual fix becomes a rule or a test, so the same mistake isn't made twice

🧾 **Consulting CRM** — Multi-tenant AI SaaS for credit-repair agencies
- AI-powered dispute automation
- PDF credit report parsing into structured data
- Token-based onboarding and built-in billing
- Row-level security for tenant isolation

---

### Stack

**Frontend:** Next.js (App Router) · React · TypeScript · Tailwind CSS

**Backend & data:** Node.js · Python · PostgreSQL · Supabase · REST APIs & webhooks

**AI:** LLM agents · Voice AI · Tool calling · MCP · Prompt evals · Multi-agent orchestration

**Infra:** Vercel · Docker · CI/CD

**Testing:** Automated tests on a real database · Adversarial AI test batteries

---

### En español

Construyo plataformas de IA para pequeños negocios: **Mely**, una recepcionista telefónica con IA que contesta en español e inglés, deja recados y agenda citas; un **CRM con IA** para empresas de reparación de crédito; y una **fábrica de agentes de IA** que construye y revisa el software.

---

### Certifications

**20x Anthropic Certified** (June 2026) — Claude API, MCP, Agents, Subagents, Claude Code, Bedrock, Vertex AI

**Google IT Support Professional** (2024) — Networking, Security, System Administration

---

### Let's connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jorge-rodriguez-level-up/)
[![Website](https://img.shields.io/badge/Website-000?style=flat&logo=google-chrome&logoColor=white)](https://floridahitech.com)
