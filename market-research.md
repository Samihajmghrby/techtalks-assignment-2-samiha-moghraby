# Market Research

Sections 1–4 of Assignment 2.

---

## 1. Chosen Niche

**Full-Stack Web Development (JavaScript / TypeScript), specialising in secure application development.**

- **Front end:** React, moving into Next.js
- **Back end:** Node.js with Express / NestJS, building REST APIs
- **Data:** PostgreSQL — schema design, indexing, query optimisation
- **Specialisation thread:** authentication and authorisation (JWT, OAuth 2.0/OIDC, RBAC), secure coding, and remediation of application vulnerabilities

### Why this niche

I came into this assignment interested in four things: cybersecurity, AI, penetration testing, and web development. Picking one meant being honest about which of them the evidence actually supports for someone graduating now.

I looked at dedicated application-security and penetration-testing roles first. The pattern there was consistent and discouraging for my situation: those postings ask for three to five years of prior security experience, and several explicitly ask for *prior software engineering experience, ideally full-stack*, as a prerequisite. Application security is a role you move **into** from development, not a role you enter from a bachelor's degree.

What made the decision for me was noticing that security had not disappeared from the full-stack listings — it was **inside** them. Seven of the nine listings I analysed name security work in their requirements or day-to-day responsibilities: implementing OAuth2/OIDC, JWT and RBAC; managing secrets and TLS; writing "secure server-side modules"; resolving "security vulnerabilities"; and maintaining "security and compliance standards." So the full-stack path does not cost me my security interest. It is the on-ramp to it, and it is where the entry-level door actually exists.

Full-stack also fits my current stack most efficiently. I already have JavaScript, HTML, CSS, React, SQL, and Git. Those are the exact foundations the listings ask for. Choosing DevOps or data engineering would mean discarding most of what I have; choosing frontend-only would leave me competing on a narrower skill set. This niche also matches the TechTalks Full-Stack Bootcamp track, so my coursework and my market research point the same direction.

**One niche, stated plainly:** I am targeting a junior/associate Full-Stack Developer role in the JavaScript/TypeScript ecosystem, and I intend to make secure implementation my differentiator rather than a second career.

---

## 2. Job Listing Research

Nine listings, all opened and read directly on the employer's own applicant-tracking page. Skills are separated into what the employer marked as **required** and what it marked as **preferred / nice-to-have**. Responsibilities use the employer's own stated wording, paraphrased.

---

### Job Listing 1 — XM

| Field | Detail |
|---|---|
| **Company** | XM (trading / fintech) |
| **Job Title** | FullStack Software Developer (React/Node.js) |
| **Location** | Limassol / Nicosia / Athens / Thessaloniki — Hybrid |
| **Experience** | Minimum 5 years of JavaScript development; BSc/MSc in Computer Science or related |

**Required skills:** JavaScript; React (including a solid understanding of the React lifecycle); Node.js; HTML; CSS/SCSS; REST or equivalent APIs; microservices architecture and web services implementation; basic SQL; Git; information design and UI/UX principles; fluency in English.

**Responsibilities:** Develop and maintain scalable applications across both front-end and back-end stacks; build user-facing applications in React and server-side components in Node.js; produce detailed technical specifications; contribute to system design and architecture; conduct code reviews; monitor application performance and proactively optimise; gather technical requirements with stakeholders; own tasks across the full SDLC.

**Nice-to-have:** TypeScript; AWS services; Kubernetes; Docker; ability to turn raw data into tables and graphs.

---

### Job Listing 2 — Tech Holding

| Field | Detail |
|---|---|
| **Company** | Tech Holding (consulting firm) |
| **Job Title** | Full Stack Engineer (Contract) — Remote |
| **Location** | Mexico — Remote |
| **Experience** | 4+ years of professional full-stack experience |

**Required skills:** Node.js and React (or Next.js); strong TypeScript; cloud engineering in Azure, AWS or GCP; relational database work including schema design, query optimisation and indexing (PostgreSQL preferred); REST and GraphQL API design, and the judgement to know when to use each; demonstrated active use of AI tools in the engineering workflow; auth patterns — JWT, OAuth 2.0, session handling; CI/CD pipelines (GitHub Actions, Azure DevOps or similar); strong asynchronous written English.

**Responsibilities:** Own full-stack feature delivery from schema design through API implementation to React UI and deployment; build scalable REST and GraphQL APIs; architect and integrate Azure-hosted services; embed AI capabilities by wrapping LLM APIs and building prompt pipelines; use AI tools daily for generation, debugging, test coverage and documentation; participate in code reviews and architecture discussions; instrument, monitor and optimise performance across the stack; contribute documentation, tooling and shared patterns, and mentor less senior teammates.

**Nice-to-have:** Azure OpenAI Service / Azure AI Search / Cognitive Services; Next.js and React Server Components or micro-frontends; LangChain or Semantic Kernel; message queues (Azure Service Bus, RabbitMQ, SQS); Kubernetes or infrastructure-as-code (Terraform, Bicep, Pulumi); prior consulting or client-facing experience.

---

### Job Listing 3 — Mattermost

| Field | Detail |
|---|---|
| **Company** | Mattermost (secure collaboration platform, open source) |
| **Job Title** | Senior Full Stack Engineer |
| **Location** | United States — Remote-first |
| **Experience** | Not stated as a number; "strong full-stack development experience" required |

**Required skills:** Strong full-stack development in Go and React, or a comparable stack; designing and consuming REST and WebSocket APIs with solid networking fundamentals; relational database experience including PostgreSQL, schema design and query optimisation; hands-on daily fluency directing AI coding agents such as Claude Code, Cursor or Copilot for scaffolding, refactors, code review and test generation — including the judgement to know when to trust the output; a bias toward shipping and owning complex software end-to-end without close supervision.

**Responsibilities:** Architect and build full-stack features across Go, React, TypeScript, PostgreSQL and Redis; use AI coding agents daily while retaining full accountability for correctness, security and design decisions; develop internal tooling and testing infrastructure; own the testing strategy for shipped code; design and consume REST and WebSocket APIs; maintain the security and compliance standards required by government and enterprise clients; contribute to the open-source codebase.

**Nice-to-have:** Distributed systems / high-availability architecture; familiarity with enterprise or regulated-environment security requirements; defence or critical-infrastructure background; open-source contributions; experience on distributed remote teams; building tools on top of AI coding agents, including MCP servers and CI-integrated agents.

---

### Job Listing 4 — LVT (LiveView Technologies)

| Field | Detail |
|---|---|
| **Company** | LVT (LiveView Technologies) — intelligent site security technology |
| **Job Title** | Senior Fullstack Software Engineer |
| **Location** | American Fork, Utah, USA — On-site |
| **Experience** | 5+ years of professional development experience |

**Required skills:** Full-stack TypeScript architectures; deep production React and modern Next.js (App Router, server actions); Node.js, NestJS preferred; GraphQL — designing schemas, resolvers and subscriptions with Apollo Server or similar; relational databases (MySQL preferred) and query builders/ORMs such as Knex; scaling real-time applications with WebSockets; modern authentication/authorisation patterns (OAuth/OIDC, JWT); Docker and containerisation; modern CI/CD practices; ability to work through unfamiliar or legacy codebases and refactor effectively.

**Responsibilities:** Design, build, test and ship features across the full stack from UI components to backend REST and GraphQL services; trace and resolve systemic bugs across service boundaries including legacy codebases; define data contracts between microservices, maintain schema federation hygiene, and architect secure, scalable real-time WebSocket data flows; write and run comprehensive tests, instrument system metrics and build operational dashboards; provide technical guidance and code reviews to mid-level and junior engineers; collaborate with QA, DevOps and architecture teams to accelerate CI/CD pipelines and improve stack-wide type safety.

**Nice-to-have:** Not separated by the employer; the listing presents an "ideal candidate" profile rather than a split list.

---

### Job Listing 5 — Appnovation Technologies

| Field | Detail |
|---|---|
| **Company** | Appnovation Technologies (global digital agency) |
| **Job Title** | **Associate** Full Stack Developer |
| **Location** | Hong Kong — Hybrid |
| **Experience** | **1–2+ years** — the only entry-accessible listing in this sample |

**Required skills:** React.js and Next.js including SSR and SSG; React Native and Flutter for cross-platform mobile; Node.js and Express.js (middleware, routing, API design); strong TypeScript, ES6+ and Dart; state management with Redux, Context API or Zustand; SQL and NoSQL schema design; Git; CI/CD pipelines; automated testing frameworks; strong foundational understanding of data structures, algorithms and clean code principles.

**Responsibilities:** Design and develop responsive, high-performance web applications with React and Next.js; build, test and deploy cross-platform mobile apps; build and maintain scalable server-side logic and RESTful APIs with Node.js and Express; implement TypeScript across the stack to reduce runtime errors; create dynamic UI components and manage complex application state; develop **secure** and efficient server-side modules and integrate third-party services; design schemas across SQL and NoSQL and manage data flow to the front end; participate in peer code reviews; take part in the full SDLC from architectural discussion through deployment.

**Nice-to-have:** Tailwind CSS, Styled Components, or mobile styling methodologies.

---

### Job Listing 6 — Serhant

| Field | Detail |
|---|---|
| **Company** | SERHANT. (real estate technology and media) |
| **Job Title** | Senior Full Stack Engineer |
| **Location** | Remote, USA |
| **Experience** | 5+ years across frontend and backend |

**Required skills:** Strong TypeScript as the primary language; multiple frontend frameworks (React, Svelte, Vue) with no strong allegiance to one; Next.js and SvelteKit; lightweight API frameworks such as Hono, Express or Fastify; deep PostgreSQL — indexing, query optimisation, schema design; familiarity with event-driven architectures and message queues; heavy daily use of AI coding assistants with established workflows; hands-on experience with frontier LLMs beyond surface-level prompting; a spec-driven approach — defining what is being built with precision before coding.

**Responsibilities:** Build and ship features across frontend and backend; move between Next.js, SvelteKit and Hono as the problem requires; work with PostgreSQL as the primary data layer designing schemas and optimising queries; write TypeScript across the stack; contribute Python services where appropriate; **write technical specifications defining APIs, data models and UI behaviour before coding**; use AI-assisted development to increase velocity and code quality; participate in code reviews, architecture discussions and technical planning; improve developer experience through tooling, documentation and automation.

**Nice-to-have:** Expo / React Native; GraphQL; serverless architectures; ClickHouse; background in real estate, marketplaces or consumer products; contributions to internal tooling or developer productivity.

---

### Job Listing 7 — Spry Methods

| Field | Detail |
|---|---|
| **Company** | Spry Methods (government technology contractor) |
| **Job Title** | Full Stack Software Developer |
| **Location** | Washington, DC — Remote |
| **Experience** | 5 years of full-stack software development |

**Required skills:** Python; FastAPI; ReactJS; PostgreSQL; Docker; familiarity with AWS services used to deploy, monitor and troubleshoot cloud-hosted applications; experience contributing to testing, code review and documentation workflows.

**Responsibilities:** Design, develop, test and deploy features across front-end and back-end layers; build and maintain REST APIs using FastAPI; develop responsive and **accessible** React front-end interfaces; implement and manage PostgreSQL data models, queries, migrations and stored procedures; work in a trunk-based development workflow using short-lived branches, frequent integration and feature flags; package and support containerised deployments using Docker in AWS-hosted environments; **investigate and resolve defects, performance issues and security vulnerabilities**; write and maintain unit, integration and regression tests and maintain technical documentation.

**Nice-to-have:** CI/CD concepts and infrastructure-as-code tooling such as Terraform and GitHub Actions.

---

### Job Listing 8 — Jobgether (on behalf of a partner company)

| Field | Detail |
|---|---|
| **Company** | Partner company hiring through Jobgether |
| **Job Title** | Senior Software Engineer, Full Stack (React, Python, Azure) |
| **Location** | Brazil — Fully remote |
| **Experience** | 6+ years of professional software engineering |

**Required skills:** TypeScript, React and Vite; monorepo environments (pnpm workspaces, Turborepo) including dependency management, pipelines and build optimisation; strong Node.js and Git-based development workflows; advanced PostgreSQL and SQL optimisation; Python backend development with FastAPI, NumPy and SciPy; deploying in Linux, Docker and reverse-proxy environments; Microsoft Azure (App Service, AKS or Container Apps, Azure Database for PostgreSQL, Key Vault, VNet); **identity and security practices — Microsoft Entra ID integration, OAuth2/OIDC, JWT, RBAC, API security and secrets management**; API and data-structure design; building or consuming MCP servers and agent tooling; familiarity with AI-native development tools; the ability to independently explore and extend unfamiliar codebases.

**Responsibilities:** Build and evolve frontend applications in TypeScript, React and Vite within a monorepo; develop and maintain backend services in Python, FastAPI and PostgreSQL with clean architecture; deploy and operate across self-hosted environments and Azure; **implement secure identity and access solutions including OAuth2/OIDC, JWT, RBAC, session management, TLS and secrets management**; build and integrate MCP servers and AI-enabled tooling; read, extend and maintain unfamiliar codebases; design APIs, data flows and integrations; create reliable testing strategies and maintain code quality.

**Nice-to-have:** Node editors and dataflow systems (React Flow, Rete.js); graph execution concepts including DAG processing and caching; node-based platforms such as Node-RED or ComfyUI; 3D technologies including Three.js, WebGL and GLSL shaders; background in computational design or generative engineering.

---

### Job Listing 9 — CodeRoad

| Field | Detail |
|---|---|
| **Company** | CodeRoad (nearshore software development services) |
| **Job Title** | Senior Fullstack Developer (Node/React) |
| **Location** | Latin America — 100% remote, contracting to US clients |
| **Experience** | 5+ years of professional full-stack development |

**Required skills:** Advanced Node.js (Express / NestJS); React.js (Hooks, Context, Redux/Zustand); expert TypeScript and ES6+; strong SQL (PostgreSQL/MySQL) or NoSQL (MongoDB) with optimisation; deep understanding of CI/CD, Git and cloud-native environments (AWS, Azure or GCP); advanced written and verbal English for collaboration with US-based clients; experience in nearshore/offshore client-facing startup cultures.

**Responsibilities:** Lead development of architectures in Node.js and React ensuring high performance, **security** and scalability; design and evolve RESTful or GraphQL integrations; build fluid, responsive and **accessible** user interfaces; manage data integrity and state across the stack with performance tuning; elevate team output through deep code reviews, mentorship of mid-level and junior engineers, and clear stakeholder communication.

**Nice-to-have:** Not separated by the employer.

---

### Consolidated research table

| # | Company | Job Title | Location | Experience | Core Skills | Key Responsibilities | Nice-to-Have |
|---|---|---|---|---|---|---|---|
| 1 | XM | FullStack Software Developer (React/Node.js) | Cyprus / Greece, hybrid | 5+ yrs | JS, React, Node.js, HTML, CSS/SCSS, REST APIs, microservices, basic SQL, Git, UI/UX | Full-stack feature build, tech specs, architecture, code review, performance optimisation | TypeScript, AWS, Docker, Kubernetes, data viz |
| 2 | Tech Holding | Full Stack Engineer (Contract) | Mexico, remote | 4+ yrs | Node.js, React/Next.js, TypeScript, cloud, PostgreSQL, REST + GraphQL, JWT/OAuth 2.0, CI/CD, AI tooling | Schema → API → UI → deploy ownership, LLM API integration, code review, performance instrumentation | Azure OpenAI, RSC, LangChain, queues, K8s, Terraform |
| 3 | Mattermost | Senior Full Stack Engineer | USA, remote-first | Not numeric | Go + React (or comparable), REST + WebSocket APIs, PostgreSQL, AI coding agents daily | Full-stack features, testing strategy ownership, security & compliance standards, open source | Distributed systems, regulated-environment security, MCP servers |
| 4 | LVT | Senior Fullstack Software Engineer | Utah, USA, on-site | 5+ yrs | TypeScript, React + Next.js, Node/NestJS, GraphQL/Apollo, MySQL + ORM, WebSockets, OAuth/OIDC + JWT, Docker, CI/CD | End-to-end delivery, cross-service debugging, secure real-time data flows, testing + metrics, mentorship | — (not split by employer) |
| 5 | **Appnovation** | **Associate Full Stack Developer** | Hong Kong, hybrid | **1–2+ yrs** | React + Next.js, React Native/Flutter, Node + Express, TypeScript, Redux/Zustand, SQL + NoSQL, Git, CI/CD, testing | Responsive web apps, REST APIs, secure server-side modules, schema design, peer code review, full SDLC | Tailwind CSS, Styled Components |
| 6 | Serhant | Senior Full Stack Engineer | Remote, USA | 5+ yrs | TypeScript (primary), React/Svelte/Vue, Next.js/SvelteKit, Hono/Express/Fastify, deep Postgres, event-driven, AI assistants | Ship FE+BE features, write specs before coding, schema + query optimisation, DX tooling | Expo/React Native, GraphQL, serverless, ClickHouse |
| 7 | Spry Methods | Full Stack Software Developer | Washington DC, remote | 5 yrs | Python, FastAPI, ReactJS, PostgreSQL, Docker, AWS, testing + code review + docs | REST APIs, accessible React UIs, migrations, trunk-based dev, containerised AWS deploys, fix security vulnerabilities | CI/CD, Terraform, GitHub Actions |
| 8 | Jobgether (partner) | Senior SWE, Full Stack (React, Python, Azure) | Brazil, remote | 6+ yrs | TypeScript, React, Vite, monorepo, Node.js, Git, PostgreSQL, Python/FastAPI, Linux + Docker, Azure, OAuth2/OIDC + JWT + RBAC + secrets | Frontend + backend build, Azure deploy/operate, secure identity & access, MCP/AI tooling, testing strategy | React Flow, DAG execution, Three.js/WebGL |
| 9 | CodeRoad | Senior Fullstack Developer (Node/React) | LATAM, remote | 5+ yrs | Node.js (Express/NestJS), React, TypeScript, SQL/NoSQL optimisation, CI/CD, Git, cloud-native, English | Node + React architecture with performance/security/scalability, REST/GraphQL, accessible UIs, code review + mentorship | — (not split by employer) |

---

## 3. Pattern Analysis

All percentages below are counted from the nine listings above and nothing else. Where a skill was listed by an employer only as preferred, it is counted separately and marked.

### Frequency table

| Skill / Technology / Practice | Times Mentioned | % of Listings | Priority |
|---|---:|---:|---|
| React | 9/9 | 100% | **High — non-negotiable** |
| Relational database / SQL | 9/9 | 100% | **High — non-negotiable** |
| REST API design & implementation | 9/9 | 100% | **High — non-negotiable** |
| Security: auth, secure coding, or vulnerability work | 7/9 | 78% | **High** |
| TypeScript (required, not preferred) | 7/9 | 78% | **High** |
| Node.js | 7/9 | 78% | **High** |
| Database schema design & query optimisation | 7/9 | 78% | **High** |
| Code review as a stated duty | 7/9 | 78% | **High** |
| System/architecture design & written technical specs | 7/9 | 78% | **High** |
| PostgreSQL specifically | 6/9 | 67% | **High** |
| Cloud platform (AWS / Azure / GCP) | 6/9 | 67% | Medium-High |
| Mentorship / stakeholder communication | 6/9 | 67% | Medium |
| CI/CD pipelines | 5/9 | 56% | Medium-High |
| Automated testing (unit / integration / E2E) | 5/9 | 56% | Medium-High |
| Git / explicit branching workflow | 5/9 | 56% | Medium (see note) |
| AI-assisted development / LLM integration | 4/9 | 44% | Medium — rising |
| Next.js | 4/9 | 44% | Medium |
| Docker / containerisation | 4/9 | 44% | Medium |
| GraphQL | 4/9 | 44% | Secondary |
| Named auth protocols (JWT / OAuth2 / OIDC / RBAC) | 3/9 | 33% | Medium |
| Accessibility | 3/9 | 33% | Secondary |
| Python | 3/9 | 33% | Secondary |
| Kubernetes | 2/9 | 22% | Lower |
| WebSockets / real-time | 2/9 | 22% | Lower |
| Microservices | 2/9 | 22% | Lower |
| Infrastructure-as-code (Terraform / Bicep) | 2/9 | 22% | Lower |
| Mobile (React Native / Flutter) | 2/9 | 22% | Lower |
| Go | 1/9 | 11% | Lower |
| **PHP / WordPress** | **0/9** | **0%** | **Not relevant to this niche** |
| **Java / C / C++** | **0/9** | **0%** | **Not relevant to this niche** |

*Note on Git:* only five listings name Git or a branching workflow explicitly, but every listing describes code review, pull-request collaboration or CI pipelines, all of which presuppose it. The 56% figure understates its real importance; I treat it as a baseline expectation rather than a differentiator.

### High-priority / core skills

These appear in three-quarters or more of the listings and are where the bulk of my six months goes.

1. **React** — 9/9. Not one listing in this niche omits it.
2. **Relational SQL, PostgreSQL-flavoured** — 9/9 for SQL, 6/9 name PostgreSQL. And crucially, 7/9 want more than "can write a SELECT": they want schema design, indexing, migrations and query optimisation.
3. **REST API design** — 9/9. Consistently framed as *designing* APIs, not just consuming them.
4. **TypeScript** — 7/9 as a hard requirement. In one listing it is described as the primary language; in another as something you reach for by default.
5. **Node.js** — 7/9, usually with Express or NestJS.
6. **Security in application code** — 7/9. This is the finding that shaped my whole plan and I detail it below.

### Secondary skills

Appear several times but not universally. Worth genuine but bounded time.

- **Cloud deployment** (6/9) — but split across AWS, Azure and GCP, so the transferable skill is deploying a containerised app to *a* cloud, not mastering one vendor.
- **CI/CD** (5/9) and **automated testing** (5/9) — these two travel together and are cheap to demonstrate in a portfolio.
- **Next.js** (4/9) — meaningful, but always as an extension of React, never instead of it.
- **Docker** (4/9) — the entry point to the cloud/CI/CD cluster of skills.
- **AI-assisted development** (4/9) — see the surprises section.

### Lower-priority / nice-to-have skills

- **Kubernetes** (2/9) — and in both cases only as a nice-to-have. I am deliberately not learning it in these six months.
- **GraphQL** (4/9, but required in only 3) — almost always phrased as "REST *or* GraphQL." REST first.
- **WebSockets** (2/9), **microservices** (2/9), **Terraform/IaC** (2/9), **React Native/Flutter** (2/9), **Go** (1/9).
- **Three.js/WebGL, ClickHouse, Kafka, node editors** — each appeared once, in a single employer's preferred list. Noise, not signal.

### Key observations

**Which skills appeared most often.** React, SQL and REST APIs, at 100% each. There is no ambiguity: if I cannot build a React interface that talks to a REST API backed by a relational database, I am not a candidate for any of these nine roles. Everything else in this document is built on top of that triangle.

**What surprised me — security is already inside the job.** I expected to find security only in dedicated security roles. Instead it is in 7 of 9 full-stack listings, and not as a slogan. Jobgether's partner asks for OAuth2/OIDC, JWT, RBAC, session management, TLS and secrets management as a named requirement. LVT wants OAuth/OIDC and JWT plus "secure real-time WebSocket data flows." Tech Holding lists JWT, OAuth 2.0 and session handling under requirements. Spry Methods puts "resolve security vulnerabilities" in the daily responsibilities. Mattermost asks the engineer to "maintain the security and compliance standards" and to stay accountable for security even when using AI agents. Appnovation — the *associate-level* posting — asks for "secure server-side modules." This changed my career thinking more than anything else in the research: I do not have to choose between security and development, and I do not have to wait for a security job title to do security work.

**What surprised me — AI tooling has become a requirement, not a perk.** Four of nine listings require it, and the phrasing is strong. Mattermost wants "hands-on daily fluency directing AI coding agents... with the judgment to know when to trust the output and when to take the wheel yourself." Serhant asks for "heavy daily use of AI coding assistants" and workflows the candidate has personally developed. Tech Holding wants engineers who can "speak concretely about how and where they help" and who can embed LLM APIs and prompt pipelines into products. A year or two ago I would have assumed this belonged in an ML role. It is now a general full-stack expectation, and it is something an interviewer can probe in thirty seconds.

**What was less common than I expected.** Kubernetes — I assumed it was table stakes; it appeared twice, both times as optional. GraphQL — heavily discussed online, but the listings almost always say "REST or GraphQL," and REST is the safe default. Microservices appeared only twice. This is a useful correction to what social media suggests I should learn.

**Which responsibilities repeated.** Four kept coming back:
1. **End-to-end feature ownership** — from database schema through API to UI to deployment. Named almost verbatim by Tech Holding, LVT, XM, Spry Methods and Appnovation.
2. **Code review and written communication** — 7/9. Serhant goes furthest, requiring specs that define APIs, data models and UI behaviour *before* coding starts.
3. **Performance and query optimisation** — 7/9, usually tied to the database layer specifically.
4. **Testing and debugging across boundaries** — tracing a fault from UI to API to database.

**What employers seem to value most.** Reading these nine together, the through-line is not a technology list — it is **autonomy over a vertical slice**. Phrases like "own complex software end-to-end without close supervision," "high agency," "ability to work independently with minimal supervision," "read, extend and maintain unfamiliar codebases," and "find solutions without needing detailed instructions" recur constantly. The stack is the entry ticket; the ability to take a feature from schema to production alone is what they are actually buying.

**What this means for my learning priorities.** Depth over breadth, in one lane: TypeScript → React/Next.js → Node/Express → PostgreSQL → auth and secure coding → testing → Docker/CI/CD → deploy. Every project should be a vertical slice I built alone and can defend line by line. And I should stop investing in PHP/WordPress as a *career* skill for this niche, because it appeared in zero of nine listings.

---

## 4. Current Skills vs. Market Requirements

Assessed honestly against what the nine listings ask for, and against what my experience actually is — university coursework, internships, training, personal projects and technical/teaching work. I have not counted classroom exposure as professional proficiency.

### Skills I already have

| Skill | Market frequency | My real level |
|---|---|---|
| HTML | Named in 1/9 explicitly, assumed in all | Solid, production-usable |
| CSS | Named in 1/9 explicitly, assumed in all | Solid |
| JavaScript (ES6+) | Foundation of 8/9 | Solid fundamentals |
| SQL (querying) | 9/9 | Comfortable writing queries |
| Git / GitHub | Baseline in all | Comfortable with day-to-day commands |
| Python | 3/9 | Comfortable as a language |
| Problem-solving, DSA, clean-code fundamentals | Explicit in Appnovation, implicit everywhere | CS-degree level, genuinely useful |

### Skills I have some exposure to

These are real but academic or project-scale, not production-scale. I would not claim professional depth in an interview.

- **React** — I have built with it, but not with production patterns: no serious state-management architecture, limited component testing, no performance profiling. Given React is 9/9, this gap is my single most expensive one.
- **REST APIs** — I have consumed them. I have not *designed* one — versioning, error contracts, pagination, status-code discipline — which is what 9/9 listings actually ask for.
- **SQL beyond querying** — I can query. I have not designed a normalised schema under real constraints, written migrations, or read an `EXPLAIN` plan and fixed an index. 7/9 listings want exactly that.
- **PHP, WordPress, Elementor, WooCommerce, CMS development, SEO** — genuine practical experience, and commercially useful freelance skills. But 0/9 in this niche. I am reclassifying these as *income skills*, not *career-path skills*, and I will not build my portfolio around them.
- **Java, C++, C** — solid academic grounding, 0/9 in these listings. Valuable as CS foundations, not as target-role evidence.

### Skills I need to strengthen

Things I have touched but must reach job-ready depth in:

1. **React → production React.** Hooks in anger, state management (Context/Zustand/Redux), component composition, controlled rendering behaviour, and accessibility (3/9).
2. **SQL → PostgreSQL engineering.** Schema design, indexes, migrations, transactions, `EXPLAIN ANALYZE`. This is a 7/9 requirement and currently one of my weakest points relative to demand.
3. **Git → team Git.** Branching strategy, pull requests, review etiquette, meaningful commit history, trunk-based flow with short-lived branches (named by Spry Methods). My commit history is currently a solo-student history, and a reviewer can tell.
4. **Written technical communication.** Serhant requires specs before coding; XM requires detailed technical specifications; six listings mention stakeholder communication. My repositories currently have thin READMEs.

### Skills I am missing

Recurring requirements with no meaningful presence in my profile. These drive the roadmap.

| Missing skill | Frequency | Why it matters |
|---|---:|---|
| **TypeScript** | 7/9 | The single largest hard gap. Required, not preferred, in seven listings. Everything else compounds off it. |
| **Node.js + Express/NestJS** | 7/9 | I have no server-side JavaScript. This is the other half of "full-stack." |
| **Applied auth & secure coding** (JWT, OAuth2/OIDC, RBAC, secrets, TLS, OWASP-style remediation) | 7/9 | My security interest is currently conceptual. Employers want it implemented in code. |
| **Automated testing** (Jest/Vitest, Playwright/Cypress) | 5/9 | I do not currently write tests. Three listings make testing an ownership responsibility. |
| **CI/CD** (GitHub Actions) | 5/9 | Zero exposure. Cheap to learn, highly visible in a repo. |
| **Docker** | 4/9 | Zero exposure. Gateway to cloud deployment. |
| **Cloud deployment** | 6/9 | I have deployed WordPress to shared hosting; I have not deployed a containerised app to a cloud provider. |
| **Next.js** | 4/9 | Extension of React, not a separate track. |
| **AI-assisted development as a documented practice** | 4/9 | I use AI tools informally. Employers want a workflow I can describe and defend. |

### Skills I should NOT prioritise yet

Deliberately excluded from the six months, with the evidence for excluding them:

- **Kubernetes** — 2/9, optional in both. Docker alone covers the containerisation signal.
- **GraphQL** — required in only 3/9, and always as an alternative to REST. I will learn the concept well enough to discuss it; I will not build a portfolio project on it.
- **React Native / Flutter** — 2/9. Would split my focus across a different platform.
- **Go** — 1/9. Interesting, not evidenced.
- **Terraform / IaC** — 2/9, preferred only.
- **Kafka, ClickHouse, Three.js/WebGL, node editors** — one mention each, single employers.
- **Penetration testing certifications (OSCP and similar)** — my interest is real, but the entry-level door here is application development with security depth. A pentest certification does not make me a stronger candidate for any of these nine roles. Revisit after two years of engineering experience.
- **Deepening PHP/WordPress** — 0/9. Maintain for freelance income, do not invest new learning hours.
