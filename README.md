# Hey, I'm Jorge Rodriguez

**Founder & Full-Stack AI Platform Engineer** at [Florida Hitech Services](https://floridahitech.com) — Miami, FL · English / Español

I build production AI platforms end to end: multi-tenant SaaS where AI agents do real work for small businesses — answering phone calls, booking appointments, processing documents — and the Meta Harness that builds them. Claude Code is my primary way of building, and I build my own tools on top of it, made to fit the way I work.

**In the last eight months:** 5,400+ commits across 19 private repositories · 100+ runs of my own agent factory · 3 platforms live in production.

**What I bring**
- **AI agents in production, talking to real customers** — Mely answers real business phone lines, books appointments and hands calls to people
- **MCP servers** — Credit4Ever exposes its data to any MCP-compatible agent, read-only and scoped per key
- **Agentic systems** — The Factory orchestrates up to 16 agents with tool use, a deterministic validator and adversarial test batteries as evals
- **The full lifecycle, shipped solo** — backend, frontend, database, deployment, monitoring and iteration in production
- **Integrations** — Stripe, Twilio, ElevenLabs, Square, Inngest, Supabase, Google OAuth, Sentry

> My repositories are private because they hold client data. Happy to walk you through any of them live.

---

### Live in production

📞 **[Mely](https://mely.floridahitech.com) — AI phone receptionist for small businesses**
Answers the calls a business misses, in English and Spanish, using only the business's real information — then takes a message, books an appointment or transfers the call. Started October 6, 2026; 88 pull requests merged since. Its first phases were built by The Factory; as it specialized, I took it further by hand.
- Voice AI agent with swappable language models, chosen per business from the admin console
- Books appointments in its own calendar or in the business's booking system
- Multi-tenant by design: row-level security, and the tenant always comes from the authenticated call — never from the AI
- Nothing is lost silently: every webhook is verified, stored and processed in the background; every side effect is idempotent
- Guardrails against phone manipulation, server-side checks the AI cannot bypass, and an adversarial test battery every prompt version must pass before it ships
- Owner panel (messages, calls, transcripts, recordings, agenda) and admin console (one-click onboarding, per-call costs and usage)
- Connected to the Florida Hitech platform: during a call it checks availability and books appointments in its agenda, and on the 1st of every month it sends each business's usage so Florida Hitech can bill the client — both through versioned, idempotent API contracts
- Monitored in production with scheduled health checks that alert when a service stops answering

🧾 **[Credit4Ever](https://credit4ever.com) — white-label CRM for credit-repair companies**
A company signs up, picks a plan, invites its team and manages clients end to end.
- Multi-tenant: every table carries the tenant, and row-level security keeps data from ever crossing between companies
- AI-powered dispute workflow and PDF credit-report parsing into structured data
- **Funding module** — a Credit Karma-style financial recommender: a catalog of lenders where every field keeps its source and date, and a matching engine that compares each client's credit profile against lender eligibility to surface the best personal-loan options
- **Business financing is the next vertical** — the data model and the lender list for business cards, lines of credit, term loans, SBA and factoring are already in place
- **MCP server**: any MCP-compatible agent (Claude, Cursor and others) can connect directly with a key. Read-only, scoped to what that key may see, with per-key rate limits and an append-only call log — if the log fails, no data is returned
- Multi-tenant billing with Stripe Connect, plans per company and token-based onboarding

🏢 **[Florida Hitech](https://floridahitech.com) — my company's platform and CRM**
- Public site plus a private CRM for clients, contracts and invoicing
- AI assistant on chat, SMS and social DMs, with a multi-provider model dispatcher (Anthropic and others) configurable from the admin panel
- Live Stripe billing: card and ACH, hosted checkout — card data never touches our servers
- Receives Mely's monthly usage per business and bills each client; exposes the agenda Mely books into during live calls

🖨️ **PrintVibe Miami — bilingual e-commerce and quoting site for a print shop**
Catalog the owner edits himself in English and Spanish, product configurator with tiered pricing by quantity, cart and order tracking. One of the first projects launched with The Factory (50+ runs), then refined by hand.

---

### How I ship: The Factory — a Meta Harness for software delivery

A coding-agent harness makes one model reliable. A Meta Harness coordinates many of them.
The Factory turns a one-line goal into reviewed pull requests: deterministic scaffolding around probabilistic agents.
- **Contract first, machine-checked.** An architect agent reads the repo and writes a contract — schema, routes, file-by-file ownership, every migration with its rollback. A deterministic validator (bash + jq, no model) rejects it if two agents would touch the same file, a port repeats or a migration has no way back, before any agent writes code.
- **Specialists on demand.** 16 agents (data, backend, frontend, security, legal, payments, copy, SEO, infra, review…) wake only when the contract needs them, in waves, each in its own git worktree, and a hook blocks any write outside its assigned files.
- **Verified, not trusted.** Every branch runs the same verification as CI; an integrator merges in order and re-verifies; an independent AI reviewer checks before anything ships.
- **Learns, with a human in the loop.** Every manual fix becomes a rule or a test, so the same mistake isn't made twice. A person decides what becomes a rule.
- **In numbers:** up to 16 agents per run · 8 of 96 plans rejected by the validator · 4,700+ tests guard the factory · a typical run takes ~24 minutes and ~$8.50.

**Built with The Factory:** Mely · PrintVibe Miami · a client platform for a financial services firm · The Factory itself, which ships its own improvements through the same pipeline.

---

### Data and integrations

🗂️ **FL Data Engine** — ingests official Florida public sources (Sunbiz, CFPB, bank pages, county records), normalizes them and serves them through a read-only API to B2B clients. Business entities only — never data about people.

🏗️ **CRM rebuild for a construction company** — rewriting a single-file app with an exposed database key into a proper platform: security and business logic on the server and in the database, row-level security, bilingual.

---

### Internal tools I've built

📣 **Marketing office** — a marketing department made of Claude Code agents. It takes a brief for a brand and delivers a batch of ready-to-publish pieces, one per network, as a pull request. Approving the batch is merging it; publishing stays manual.

🎬 **Video editing workshop**
- **efectos-video** — takes a short talking-head clip and returns a vertical 1080×1920 video with word-by-word subtitles, zooms and editor-grade touches
- **Multi-brand editing kit** — reels, animated Instagram carousels and per-brand identity as Claude Code skills (built on Erik Taveras' open kit)
- **videos-web** — turns a website or a repo into a 15–25 second video, ready to post
- **Podcast to clips** — splits a vertical podcast into one clip per question for Instagram, TikTok and YouTube Shorts

⚖️ **Legal review skill** — checks what a video says (the transcript, to the second) and what it shows on screen against rules written in code, before it gets published.

🗄️ **Brand archive** — scripts, voice, context and decisions for each brand in plain Markdown, YAML and TSV, so every agent reads the same source.

🔒 **Sandboxed local agent** — an AI assistant locked in Docker that cannot see the Mac's files, keys, browser sessions or local network.

📚 **Knowledge base** — distilled notes from the sources I learn from, searchable by my agents instead of loaded whole.

---

### Stack

**Frontend:** Next.js (App Router) · React · TypeScript · Tailwind CSS

**Backend & data:** Node.js · Python · PostgreSQL · Supabase · REST APIs & webhooks · Stripe

**AI:** Claude Code · LLM agents · Voice AI (ElevenLabs, Twilio) · Tool calling · MCP servers · Prompt evals · Harness engineering · Meta Harness orchestration

**Infra:** Vercel · Docker · GitHub Actions CI · Sentry

**Testing:** Automated tests on a real database · Adversarial AI test batteries

---

### Certifications

**19x Anthropic Certified** (June 2026) — Claude API, MCP, Agents, Subagents, Claude Code, Bedrock, Vertex AI

**Google IT Support Professional** (2024) — Networking, Security, System Administration

---

### Let's connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jorge-rodriguez-usa/)
[![Website](https://img.shields.io/badge/Website-000?style=flat&logo=google-chrome&logoColor=white)](https://floridahitech.com)
