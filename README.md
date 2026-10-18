# Hey, I'm Jorge Rodriguez

**Founder & Full-Stack AI Platform Engineer** at [Florida Hitech Services](https://floridahitech.com) — Miami, FL

I build production AI platforms end to end: multi-tenant SaaS where AI agents do real work for small businesses — answering phone calls, booking appointments, processing documents — and the Meta Harness that builds them.

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

🏭 **The Factory — a Meta Harness for software delivery** *(builds everything here)*
A coding-agent harness makes one model reliable. A Meta Harness coordinates many of them.
The Factory turns a feature request into reviewed pull requests: deterministic scaffolding around probabilistic agents.
- **Contract first, machine-checked.** An architect agent reads the repo and writes a contract — schema, routes, file-by-file ownership, every migration with its rollback. A validator rejects it if two agents would touch the same file, a port repeats or a migration has no way back, before any agent writes code.
- **Specialists on demand.** 16 agents (data, backend, frontend, security, legal, payments, copy, SEO, infra, review…) wake only when the contract needs them, in waves, each owning its own files.
- **Verified, not trusted.** Every branch runs the same verification as CI; an integrator merges in order and re-verifies; an independent AI reviewer checks before anything ships.
- **Learns, with a human in the loop.** Every manual fix becomes a rule or a test, so the same mistake isn't made twice. The harness improves from its failures, but a person decides what becomes a rule.

**Built with The Factory:**
- **Mely**, the AI phone receptionist above
- A bilingual e-commerce and quoting site for a Miami print shop — product configurator with tiered pricing, cart and order tracking
- A client platform for a financial services firm
- The Factory itself: it ships its own improvements through the same pipeline

🧾 **Consulting CRM** — Multi-tenant AI SaaS for credit-repair agencies
- AI-powered dispute automation
- PDF credit report parsing into structured data
- Token-based onboarding and built-in billing
- Row-level security for tenant isolation

---

### Stack

**Frontend:** Next.js (App Router) · React · TypeScript · Tailwind CSS

**Backend & data:** Node.js · Python · PostgreSQL · Supabase · REST APIs & webhooks

**AI:** LLM agents · Voice AI · Tool calling · MCP · Prompt evals · Harness engineering · Meta Harness orchestration

**Infra:** Vercel · Docker · CI/CD

**Testing:** Automated tests on a real database · Adversarial AI test batteries

---

### En español

Construyo plataformas de IA para pequeños negocios: **Mely**, una recepcionista telefónica con IA que contesta en español e inglés, deja recados y agenda citas; un **CRM con IA** para empresas de reparación de crédito; y **The Factory**, un Meta Harness: una fábrica de agentes de IA que construye y revisa el software.

---

### Certifications

**20x Anthropic Certified** (June 2026) — Claude API, MCP, Agents, Subagents, Claude Code, Bedrock, Vertex AI

**Google IT Support Professional** (2024) — Networking, Security, System Administration

---

### Let's connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jorge-rodriguez-level-up/)
[![Website](https://img.shields.io/badge/Website-000?style=flat&logo=google-chrome&logoColor=white)](https://floridahitech.com)
