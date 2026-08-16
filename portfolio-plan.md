# Portfolio Plan & Final Reflection

Sections 6 and 7 of Assignment 2.

Three projects. Each one exists because of a specific frequency figure in `market-research.md`, and each one is scoped to something a senior CS student can actually finish. None of them is included because it sounds impressive.

**Coverage check** — between them, the three projects demonstrate every skill that appeared in 44% or more of the listings:

| Requirement | Frequency | P1 | P2 | P3 |
|---|---:|:--:|:--:|:--:|
| React | 9/9 | ✓ | ✓ | ✓ |
| Relational SQL / PostgreSQL | 9/9 | ✓ | ✓ | ✓ |
| REST API design | 9/9 | ✓ | ✓ | ✓ |
| Security / auth / secure coding | 7/9 | ✓✓ | ✓ | ✓✓ |
| TypeScript | 7/9 | ✓ | ✓ | ✓ |
| Node.js | 7/9 | ✓ | ✓ | ✓ |
| Schema design & query optimisation | 7/9 | ✓ | ✓✓ | — |
| Code review / written technical communication | 7/9 | ✓ | ✓ | ✓ |
| Cloud deployment | 6/9 | ✓ | ✓ | ✓ |
| CI/CD | 5/9 | ✓ | ✓ | ✓ |
| Automated testing | 5/9 | ✓ | ✓ | ✓ |
| Docker | 4/9 | ✓ | ✓ | ✓ |
| Next.js | 4/9 | — | ✓ | — |
| AI-assisted development / LLM integration | 4/9 | — | — | ✓✓ |
| Legacy / unfamiliar codebase migration | 2/9 (LVT, Jobgether) | — | ✓✓ | — |

`✓✓` = the project's headline demonstration.

---

## Project 1 — **SentryDesk**: a role-secured multi-tenant support desk

### Problem
Small clinics, agencies and SMEs in Lebanon run their client requests over WhatsApp and email. Nothing is tracked, and — more importantly — nothing is *isolated*. When one shared account holds several clients' data, any staff member can see everything. Multi-tenant data isolation is a genuine access-control problem, and broken access control is the most common serious flaw in real applications.

### Solution
A support-ticket system where multiple organisations share one deployment but can never see each other's data. Three roles — Owner, Agent, Client — with permissions enforced on the **server**, at the query layer, not in the UI. Every access-control decision is a documented, tested design choice.

### Main features
- Email/password registration with argon2 hashing, plus a "Sign in with Google" OAuth 2.0 / OIDC flow
- JWT access tokens with refresh-token rotation and server-side revocation
- Role-based access control with organisation-scoped queries enforced in the data layer
- Ticket lifecycle: create, assign, comment, change status, close, with a full audit trail
- Rate limiting on authentication endpoints and validation on every input boundary
- A `SECURITY.md` containing a threat model and a documented vulnerable-branch-and-fix log

### Technologies
TypeScript · React · Node.js + Express · PostgreSQL + Prisma · Zod validation · JWT + OAuth 2.0/OIDC · argon2 · Vitest + Supertest · Docker + docker-compose · GitHub Actions · deployed to a cloud provider

### Skills demonstrated
The core triangle (React 9/9, SQL 9/9, REST 9/9) plus the security cluster: JWT, OAuth 2.0/OIDC and RBAC as named by Tech Holding, LVT and the Jobgether partner; secrets management; and the "secure server-side modules" Appnovation asks of an associate developer. Also schema design under real constraints, migrations, testing, containerisation and CI.

### Why employers would care
Seven of nine listings put security in requirements or responsibilities, and yet almost no junior portfolio contains a real permission model. Most junior projects hide the admin button and call it authorisation. This project's headline artefact is the deliberately-vulnerable branch: I introduce an IDOR — an agent from Organisation A fetching a ticket belonging to Organisation B by changing an ID in the URL — demonstrate the exploit, then fix it by scoping the query rather than patching the controller, and write up both. That is the closest a student can get to Spry Methods' "investigate and resolve defects, performance issues, and security vulnerabilities."

### GitHub requirements
- Clear README: problem, architecture diagram, one-command local setup, live demo link
- `ARCHITECTURE.md`, `SECURITY.md` (threat model + vulnerability log), `TESTING.md`
- Meaningful commit history on short-lived feature branches merged via pull request, matching Spry Methods' trunk-based workflow
- Passing CI badge; `docker compose up` brings the whole stack up
- Seeded demo data and read-only demo credentials in the README

### What I should explain in an interview
- Why RBAC is enforced at the query layer and not in the controller or the UI, and what breaks if it is not
- The trade-offs between JWTs and server-side sessions, and why I chose refresh-token rotation
- The IDOR I introduced: how I found it, how I fixed it, and how the regression test now prevents it returning
- How I keep secrets out of the repository and how configuration differs between local, CI and production
- One schema decision I would make differently now, and why

---

## Project 2 — **Mouneh**: migrating a legacy WordPress storefront to a typed full-stack application

### Problem
I have real WordPress, WooCommerce and Elementor experience — and my research found that skill in **zero of nine** listings in my target niche. Rather than pretend that experience does not exist, this project converts it into evidence for the niche I *am* targeting: taking a working legacy system, understanding it, and rebuilding it properly.

The business case is real. A small Lebanese food producer selling *mouneh* (preserves, za'atar, olive oil) runs a WooCommerce store that is slow, hard to extend, and impossible to test.

### Solution
Rebuild it as a typed full-stack application: migrate the product and order data out of the WordPress/MySQL schema into a normalised PostgreSQL schema, expose a documented REST API, and serve a Next.js storefront. The engineering story is the **migration and the measured performance improvement**, not the shop itself.

### Main features
- A repeatable, idempotent migration script that reads the WordPress schema and loads a normalised PostgreSQL schema, with data-integrity verification
- Product catalogue with search, filtering and pagination, backed by real indexes
- Cart and order flow with server-side price and stock validation (never trusting the client)
- An admin area reusing the RBAC pattern from Project 1
- A `PERFORMANCE.md` recording query timings before and after indexing, with `EXPLAIN ANALYZE` output
- Bilingual Arabic/English interface with proper RTL support and keyboard accessibility

### Technologies
TypeScript · Next.js (App Router, server components) · Node.js · PostgreSQL + Prisma · Docker · GitHub Actions · Playwright for one end-to-end purchase flow · deployed to a cloud provider

### Skills demonstrated
Schema design and query optimisation as a measured result (7/9); Next.js (4/9); accessibility (3/9); and — the differentiator here — the ability to "read, extend, and maintain unfamiliar codebases" (Jobgether partner) and "dive into unfamiliar or legacy codebases, deduce business logic, and refactor effectively" (LVT). Two employers named this explicitly, and it is a skill almost no student portfolio addresses.

### Why employers would care
It answers the question my CV otherwise raises. An interviewer looking at my WordPress background will wonder whether I am a CMS configurator or an engineer. This project answers it in the strongest possible way: I understood the legacy system well enough to migrate it, and I can quantify the improvement. Real engineering teams spend far more time on existing systems than greenfield ones, which is exactly why LVT and the Jobgether partner ask for it.

### GitHub requirements
- README leading with the migration story and the before/after performance numbers
- `MIGRATION.md` documenting the source schema, the target schema, and the mapping decisions
- `PERFORMANCE.md` with `EXPLAIN ANALYZE` output before and after indexing
- Migration script runnable against a seeded sample WordPress database included in the repo
- Playwright end-to-end test covering browse → cart → checkout, running in CI

### What I should explain in an interview
- How WordPress's `wp_postmeta` key-value storage works, why it makes product queries slow, and how normalising it fixed that
- The specific index I added, the `EXPLAIN` plan before and after, and the millisecond difference
- How I guaranteed the migration was idempotent and verifiable, and what I did about rows that would not map cleanly
- Why prices and stock are validated server-side, and the attack that becomes possible if they are not
- What RTL support actually required beyond `direction: rtl`

---

## Project 3 — **Naqqid**: an AI-assisted document triage tool with a hardened LLM boundary

### Problem
Four of nine listings require AI-assisted development or LLM integration. But the interesting engineering problem is not calling an API — it is that an LLM boundary is an **untrusted input boundary**. Prompt injection, unsafe output handling and data leakage are real application-security concerns, and they sit exactly where my two interests meet.

### Solution
An internal tool that ingests documents, uses an LLM API to classify and summarise them, and routes them to the right queue — built so that the LLM is treated as untrusted throughout. Every model output is schema-validated before use; every model input is scoped so that a malicious document cannot escalate its own privileges.

### Main features
- Document upload with type/size validation and content sanitisation
- LLM classification and summarisation through a prompt pipeline with structured JSON output
- **Strict output validation:** every model response parsed against a schema and rejected on mismatch — the model never returns anything that is executed or trusted directly
- Prompt-injection defences: instruction/data separation, and a documented test suite of adversarial documents that attempt to override system instructions
- Per-user rate limiting and cost controls, with token usage logged per request
- Graceful degradation when the API is slow, rate-limited or unavailable
- A `AI-WORKFLOW.md` documenting how I used AI coding agents to build this, including two cases where I rejected their output and why

### Technologies
TypeScript · React · Node.js + Express · PostgreSQL · an LLM API · Zod for output-schema validation · Vitest · Docker · GitHub Actions

### Skills demonstrated
LLM integration and prompt pipelines (Tech Holding: "embed AI capabilities into products wrapping LLM APIs, building prompt pipelines"; 4/9 overall); the security cluster applied to a novel boundary; input validation, rate limiting and structured error handling; and — through `AI-WORKFLOW.md` — the documented AI development practice that Mattermost, Serhant and Tech Holding all require.

### Why employers would care
This project targets the finding that most surprised me. Mattermost wants engineers with "the judgment to know when to trust the output and when to take the wheel yourself." Serhant wants candidates who have "developed workflows that make you faster." Tech Holding wants engineers who can "speak concretely about how and where they help." Those are all questions about *judgement*, and judgement is very hard to claim and very easy to demonstrate. The adversarial test suite is the proof: it shows I treat a model as an untrusted boundary rather than a magic box, which is precisely the instinct a security-minded developer should have.

### GitHub requirements
- README explaining the LLM-as-untrusted-boundary design decision up front
- `AI-WORKFLOW.md` with concrete examples, including the two rejected outputs
- `PROMPT-SECURITY.md` documenting the injection test cases and the mitigations
- Adversarial test suite runnable in CI
- Costs and API keys handled through environment configuration, never committed

### What I should explain in an interview
- Why I validate LLM output against a schema instead of trusting it, and what happens when validation fails
- A specific prompt-injection payload from my test suite, and the mechanism that stops it
- A case where an AI coding agent produced plausible but wrong code, how I caught it, and what that taught me about reviewing generated code
- How I control cost and latency, and how the system behaves when the API is unavailable
- Where I think LLM integration is genuinely the right tool, and where it is not

---

## Project sequencing

| Timing | Project |
|---|---|
| Months 3–4 | Project 1 (SentryDesk) — establishes the core triangle and the security differentiator |
| Months 5–6 | Project 2 (Mouneh) — adds Next.js, migration credibility and measured optimisation |
| Month 6 | Project 3 (Naqqid) — smallest in scope, targets the AI requirement, finishes the set |

If time runs short, **Project 3 is the one to cut.** Projects 1 and 2 between them already cover every requirement appearing in 56% or more of the listings.

---

# 7. Final Reflection

I came into this assignment expecting the research to tell me which of my four interests to pick. What it actually did was show me that I had framed the question wrong.

My assumption was that cybersecurity and development were two doors, and I had to choose one. So I went looking at application security and penetration testing roles first, and I found a wall: three to five years of prior experience, and in several cases an explicit requirement of prior software engineering experience. Application security is not an entry-level field. That was disappointing for about a day.

Then I noticed something in the full-stack listings I had almost skimmed past. Seven of the nine of them have security *inside* the job. The Jobgether partner's listing asks for OAuth2/OIDC, JWT, RBAC, session management, TLS and secrets management as a named requirement. Spry Methods puts "resolve security vulnerabilities" in the daily responsibilities. Mattermost asks the engineer to stay accountable for security even when using AI agents. And Appnovation — the one associate-level role in my whole sample, the one job I could realistically apply for right now — asks for "secure server-side modules."

So the research did not make me abandon my security interest. It relocated it. The path in is to be the full-stack developer who is unusually good at auth and access control, and to move toward a security specialisation from inside engineering rather than trying to enter beside it. That is a more honest plan than the one I arrived with, and it is one where the door is actually open.

The frequency analysis was uncomfortable in a useful way. React, SQL and REST APIs at 100% each was reassuring, because I have real foundations in all three. But TypeScript at 78% required — not preferred, *required* — was a gap I had been underestimating, and Node.js at 78% meant that half of "full-stack" simply is not in my profile yet. The hardest number to look at was PHP and WordPress at **zero out of nine**. I have genuine commercial experience there. It has been useful, it has paid, and in the niche I am targeting it counts for nothing. Java, C and C++ were the same at zero. I am not throwing that experience away — WordPress work is still income while I study, and my CS foundations are why I can learn quickly — but I have stopped treating them as career evidence for this direction. That reclassification was probably the single most valuable thing this exercise did for me.

The other surprise was AI tooling. I expected it in machine-learning roles. Instead, four of nine general full-stack listings require it, and the phrasing is demanding rather than decorative — Mattermost wants the judgement to know when to trust an agent's output and when to override it. I use these tools already, but casually, without a defensible account of my own process. That is now something I have to be able to articulate, which is why Project 3 exists.

Some things the research told me *not* to do were just as useful. Kubernetes appeared twice, optional both times. GraphQL was almost always phrased as an alternative to REST. Microservices came up twice. Every one of those is something I might have spent a month on because it is loud online, and now I have counted evidence for skipping them.

My highest priorities are settled and ordered: TypeScript, then Node with real REST design, then PostgreSQL as an engineering discipline rather than a query language, then applied authentication and secure coding. The roadmap follows that order deliberately — TypeScript first because it makes every subsequent month's work better, security in Month 4 because it is where I stop being interchangeable with every other graduate, and deployment last because it needs something to deploy.

The projects are designed to answer the specific doubts my CV creates. SentryDesk turns "interested in cybersecurity" into a real permission model and a documented vulnerability I introduced and fixed myself. Mouneh answers the question an interviewer will inevitably have about my WordPress background — it proves I can read a legacy system, migrate it, and quantify the improvement, which two employers named as a requirement. Naqqid targets the AI expectation and puts my security instinct on a boundary most developers do not yet think of as one.

One thing I want to be honest about, because it affects how I read all of this: only one of the nine listings is genuinely open to someone at my experience level. Seven ask for four or more years. That is not a reason to change niche, but it does change what the portfolio has to do. It cannot be a set of tutorials with my name on them. It has to be three deployed applications where I can be interrogated about any layer and answer from memory, because that is the only substitute I have for the years I do not yet have.

Six months from now the goal is not that I will have learned more technologies. It is that I will be able to take a feature from database schema through API to interface to production, alone, and explain and defend every decision along the way. Reading these nine listings side by side, that autonomy — not the specific stack — is what they are all actually asking for.
