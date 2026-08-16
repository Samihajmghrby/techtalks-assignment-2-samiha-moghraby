# Six-Month Learning Roadmap

Section 5 of Assignment 2.

Every month below is justified by a frequency figure from `market-research.md`. Nothing is included because it is trendy; three technologies I was tempted to add (Kubernetes, GraphQL, React Native) are deliberately absent because the evidence did not support them.

**Design principles**

1. **Depth in one lane.** TypeScript → React/Next.js → Node/Express → PostgreSQL → security → testing/CI → deploy. No detours.
2. **Every month ships something.** Nine of nine listings describe shipping and owning features; a roadmap of tutorials would prove nothing.
3. **Compounding order.** TypeScript first because 7/9 require it and it makes every later month's code better. Deployment last because it needs something to deploy.
4. **Realistic load.** Roughly 12–15 hours per week alongside final-year coursework. Months 1–3 overlap my last semester and are deliberately lighter in scope than Months 4–6.

---

## Month-by-month plan

| Month | Main Focus | Skills / Technologies | Practice | Project / Deliverable | Expected Outcome |
|---|---|---|---|---|---|
| **1** | TypeScript + production React | TypeScript (types, interfaces, generics, narrowing, strict mode), modern ES6+, React hooks in depth, state management (Context + Zustand), accessible components | Convert two existing JavaScript React projects to strict TypeScript; rebuild three components with proper typing and keyboard accessibility; daily type-error triage | A public repo: a fully typed React dashboard UI with a documented component structure and a real README | I can write React in TypeScript without reaching for `any`, and I can explain why a type error is a design signal |
| **2** | Node.js + REST API design | Node.js, Express (with a look at NestJS structure), REST design — resources, verbs, status codes, versioning, pagination, error contracts; request validation (Zod) | Build three small APIs from scratch; write an OpenAPI description for one; deliberately break and fix my own error handling | A documented REST API (Node + Express + TypeScript) with an OpenAPI spec, consumed by the Month 1 React front end | I can *design* an API, not just call one — the exact phrasing 9/9 listings use |
| **3** | PostgreSQL as an engineering discipline | PostgreSQL, normalised schema design, indexes, migrations, transactions, `EXPLAIN ANALYZE`, ORM/query builder (Prisma), N+1 avoidance | Design a multi-table schema from written requirements; write forward and rollback migrations; deliberately create a slow query, diagnose it with `EXPLAIN`, fix it with an index, and record the before/after timings | **Portfolio Project 1 begins.** Schema + migrations + data layer, with a `PERFORMANCE.md` documenting one real query optimisation | I stop being someone who "knows SQL" and become someone who can defend a schema decision in an interview |
| **4** | Authentication, authorisation and secure coding | JWT vs. sessions, OAuth 2.0 / OIDC flows, RBAC, password hashing (argon2/bcrypt), secrets management and environment hygiene, TLS basics, OWASP Top 10 applied — injection, broken access control, XSS, CSRF, IDOR; input validation and rate limiting | Implement email/password auth *and* an OAuth provider login; build a role-based permission layer; write a deliberately vulnerable branch of my own app and then fix it, documenting each vulnerability and remediation | **Portfolio Project 1 completed.** Auth + RBAC shipped, plus a written `SECURITY.md` documenting the threat model and the fixes | This is my differentiator month. 7/9 listings want this and almost no junior portfolio has it |
| **5** | Testing, Docker and CI/CD | Vitest/Jest for unit tests, Supertest for API integration tests, Playwright for one end-to-end flow; Docker and docker-compose; GitHub Actions; trunk-based workflow with short-lived branches and pull requests | Retro-fit a meaningful test suite to Project 1; containerise the app and its database; build a pipeline that runs lint → typecheck → test → build on every PR and blocks merges on failure | **Portfolio Project 2 begins.** Project 1 gets a green CI badge, a Dockerfile, and a compose file that brings the whole stack up with one command | A grader or a hiring manager can clone my repo and run it in one command — and can see the pipeline enforcing quality |
| **6** | Next.js, cloud deployment, and interview readiness | Next.js (App Router, server components, server actions), deploying containers to a cloud provider, environment/secrets configuration in production, basic monitoring and logging, AI-assisted development as a documented workflow | Deploy Projects 1 and 2 publicly with real environment separation; write technical specs *before* building Project 3's features, in the spec-driven style Serhant requires; document how I use AI tools and where I override them | **Portfolio Projects 2 and 3 completed and deployed.** All three repos have README, ARCHITECTURE, SECURITY and TESTING docs. CV and GitHub profile rewritten around the evidence | I have three live, defensible, deployed applications and I can hold a technical conversation about every layer of them |

---

## Why each month matters, tied to the research

### Month 1 — TypeScript + production React
**Evidence:** React 9/9 (100%). TypeScript required in 7/9 (78%).

These are the two highest-frequency technical requirements in the entire dataset, and TypeScript is my single largest hard gap. It goes first because it is a *multiplier*: every line of Node, every API contract and every database model I write in Months 2–6 is better if it is typed. Doing it later would mean rewriting everything. Appnovation's associate-level listing — the one role in the sample I could realistically apply for today — asks for "strong proficiency in TypeScript" and for TypeScript "across the stack," so this is not a senior-only expectation.

I am strengthening React rather than learning it, so this month is partly consolidation: taking code I already wrote and making it production-shaped.

### Month 2 — Node.js + REST API design
**Evidence:** REST API design 9/9 (100%). Node.js 7/9 (78%).

This is the half of "full-stack" I do not currently have. Every listing frames APIs as something you *design* — Tech Holding explicitly wants the judgement to choose between REST and GraphQL; XM asks for REST or equivalent APIs plus microservices understanding; Appnovation wants "middleware, routing, API design" in Express. Consuming an API proves nothing; designing one with coherent error contracts and versioning is a demonstrable skill.

I am learning Express rather than NestJS because it teaches the underlying HTTP model rather than hiding it, but I will study NestJS's structure since LVT and CodeRoad both prefer it.

### Month 3 — PostgreSQL as an engineering discipline
**Evidence:** SQL 9/9 (100%). PostgreSQL named in 6/9. Schema design and query optimisation as an explicit expectation in 7/9 (78%).

The gap between "I know SQL" and what these employers want is wide, and it is where I am most likely to be caught out. Tech Holding asks for "schema design, query optimization, indexing." Serhant wants "deep Postgres experience — you understand indexing, query optimization, and schema design." Spry Methods lists "data models, queries, migrations, and stored procedures" as day-to-day work. The `EXPLAIN ANALYZE` exercise with recorded before/after timings is deliberate: it produces a concrete number I can quote in an interview instead of a vague claim.

### Month 4 — Authentication, authorisation and secure coding
**Evidence:** Security in requirements or responsibilities 7/9 (78%). Named auth protocols 3/9.

This is the month that makes my profile distinctive rather than interchangeable, and it is the honest expression of my cybersecurity interest inside a development career. The listings are specific: OAuth2/OIDC, JWT, RBAC, session management, TLS and secrets management (Jobgether partner); OAuth/OIDC and JWT (LVT); JWT, OAuth 2.0 and session handling (Tech Holding); "secure server-side modules" (Appnovation); "resolve security vulnerabilities" (Spry Methods); "maintain the security and compliance standards" (Mattermost).

The deliberately-vulnerable-then-fixed branch is the highest-value exercise in this entire roadmap. Almost no junior candidate can walk an interviewer through an IDOR they introduced, detected and patched in their own code. That single artefact converts my security interest from a stated preference into evidence.

### Month 5 — Testing, Docker and CI/CD
**Evidence:** Automated testing 5/9 (56%). CI/CD 5/9 (56%). Docker 4/9 (44%).

These three cluster together and are the cheapest high-visibility wins available. Mattermost requires the engineer to "own testing strategy across frontend and backend code you ship." LVT lists writing and running comprehensive tests plus accelerating CI/CD pipelines. Spry Methods requires unit, integration and regression tests, plus Docker and a trunk-based workflow with short-lived branches.

A repository with a passing pipeline badge, a real test suite and a working `docker compose up` is immediately legible to a reviewer in under a minute. It also fixes my "team Git" gap, because a pipeline that blocks merges forces me into proper branch-and-PR habits.

### Month 6 — Next.js, cloud deployment and interview readiness
**Evidence:** Cloud 6/9 (67%). Next.js 4/9 (44%). AI-assisted development 4/9 (44%). Written specs and technical communication 7/9 (78%).

Deployment goes last because it needs finished applications. Since the cloud requirement is split across AWS, Azure and GCP with no single winner, I am learning the transferable pattern — deploy a container, configure environments and secrets, read logs — rather than chasing one vendor's certification.

The spec-writing habit is deliberate and comes straight from Serhant's requirement to "write technical specifications that define APIs, data models, and UI behavior before coding," reinforced by XM's "produce detailed technical specifications." Documenting my AI workflow addresses a requirement in four listings phrased in unusually demanding terms — Mattermost wants the judgement "to know when to trust the output and when to take the wheel yourself," which is exactly the kind of thing an interviewer will ask me to demonstrate with a real example.

---

## What I am explicitly not doing, and why

| Excluded | Frequency | Reason |
|---|---:|---|
| Kubernetes | 2/9, optional both times | Docker delivers the containerisation signal at a fraction of the cost |
| GraphQL (as a build target) | Required in 3/9, always as "REST *or* GraphQL" | I will learn the trade-offs well enough to discuss; REST is the safe investment |
| React Native / Flutter | 2/9 | Splits focus onto a different platform |
| Go | 1/9 | Single mention |
| Terraform / IaC | 2/9, preferred only | Premature before I have production systems to manage |
| New PHP / WordPress learning | 0/9 | Keep for freelance income; zero career signal in this niche |
| Pentesting certification | 0/9 in this sample | Application security roles asked for 3–5 years' prior experience; the route in is through engineering, not around it |

---

## How I will know it is working

- **End of Month 2:** a front end I built talks to a back end I built, both in TypeScript.
- **End of Month 4:** Project 1 is complete, with a real auth system and a written threat model — my differentiator is on the table.
- **End of Month 5:** any stranger can clone my repo, run one command, and see a green pipeline.
- **End of Month 6:** three deployed applications, each of which I can explain from database index to rendered pixel.

If I fall behind, the order of sacrifice is: Next.js first, then the third portfolio project, then Docker. **Months 1 through 4 are not negotiable** — they map directly to the six requirements that appear in 78% or more of the listings.
