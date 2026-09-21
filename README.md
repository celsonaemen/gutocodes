# Celso Naemen

**Software Engineer** focused on building full-stack applications, designing security-aware systems, working with data pipelines, investigating Windows internals, and contributing to open source.

> Build systems. Understand systems. Break systems safely. Improve systems. Repeat.

## Engineering Focus

- Full Stack / Application Engineering
- Application Security
- Data Engineering
- Systems & Windows
- AI Engineering in evolution
- Digital Forensics
- Open Source

## Selected Engineering Work

- [**Orion**](https://github.com/celsonaemen/orion) — Full-stack system in development for authentication, administration, sectors, permissions, and audit logging. Built with TypeScript, Next.js, Tailwind, NestJS, Prisma, and PostgreSQL, with authentication and authorization as core architectural concerns. Operational communication is planned as a future evolution of the system.

- [**ETL-Manhu-MG**](https://github.com/celsonaemen/ETL-Manhu-MG) — Data pipeline for ingesting, transforming, and loading weather data from Manhuaçu, Minas Gerais. Uses Python, Apache Airflow, pandas, SQLAlchemy, PostgreSQL, Docker Compose, and the OpenWeather API.

- [**acer-a315-56-control**](https://github.com/celsonaemen/acer-a315-56-control) — Low-level research and diagnostics specific to the Acer Aspire A315-56. Uses C# to investigate Windows internals, ACPI, DSDT, embedded-controller behavior, MMIO, MSR, and IOCTL within a model-specific hardware scope.

- [**controle-de-solicita-es**](https://github.com/celsonaemen/controle-de-solicita-es) — Local desktop MVP for triage and tracking of requests, with email integration implemented. Combines Flask, React, Electron, and SQLite; support for additional channels and SLA-oriented workflows remains planned evolution rather than a consolidated feature set.

- [**Agentanalistyfiscal**](https://github.com/celsonaemen/Agentanalistyfiscal) — Exploration of AI-assisted automation applied to the fiscal and accounting domain, including agents, tools, domain knowledge, documentation, and tests. It is presented as an evolving technical project, not as a production-validated product.

- [**generatordash**](https://github.com/celsonaemen/generatordash) — Python/Streamlit dashboard with tests and validation scripts. Demonstrates experimentation with data interfaces and application behavior verification.

## Digital Forensics & Open Source

- [**IPED — PR #2979**](https://github.com/sepinf-inc/IPED/pull/2979) — Merged upstream contribution to IPED that fixed path normalization used in AppID calculation for Windows Jump Lists. The change handles `USERPROFILE` and `PUBLIC` paths, prevents the `PublicAlice` false match, and adds regression tests.

- [**PawnIO.Modules — PR #95**](https://github.com/namazso/PawnIO.Modules/pull/95) — Open pull request proposing a read-only module specific to the Acer A315-56, based on the extended ACPI embedded-controller mailbox. The PR documents hardware gating, access limits, and reverse-engineering context.

- [**PawnIO.Modules — PR #96**](https://github.com/namazso/PawnIO.Modules/pull/96) — Open pull request proposing semantic control of Intel `ENABLE_BIDIR_PROCHOT` in `MSR_POWER_CTL`, using constrained read-modify-write, environment validation, and read-back after state changes.

- [**OpenClaude — Issue #300**](https://github.com/Gitlawb/openclaude/issues/300) — Technical issue report covering OpenAI-compatible providers, Groq, Termux/Android, and related configuration behavior. This is presented as a bug report and reproduction-oriented contribution, not as project authorship.

## Technical Areas

### Software Engineering

**Languages:** Python, TypeScript, JavaScript

**Application Engineering:** React, Next.js, NestJS, Prisma, Flask, Electron, PostgreSQL, SQLite

### Data Engineering

Python, pandas, Apache Airflow, SQLAlchemy, PostgreSQL, Docker Compose, and OpenWeather API integration.

### Security Engineering

Authentication, authorization, JWT, RBAC/permissions, HttpOnly cookies, session management, refresh-token handling, bcrypt/password hashing, and audit logging.

### Systems & Windows

C#, Windows internals, ACPI, DSDT, embedded controllers, MMIO, MSR, IOCTL, and PawnIO. The public evidence is specific to hardware research, diagnostics, and PawnIO contributions; it is not presented as generic driver or firmware engineering experience.

### AI Engineering

Python, AI-assisted automation, agent tooling, domain knowledge workflows, and LLM-related tooling in projects that are still evolving. These repositories demonstrate experimentation and applied exploration, not consolidated production AI experience.

### Digital Forensics & Open Source

IPED, Windows artifacts, Windows Jump Lists, AppID calculation, path normalization, regression testing, and upstream contributions.

### Tools & Platforms

Git, GitHub, GitHub Actions, Docker, npm, pnpm, Maven, Gradle, PowerShell, and project-specific development tooling evidenced in the repositories.

## Engineering Approach

- Reproduce and test problems before proposing fixes.
- Treat security as an architectural concern.
- Document technical decisions, operational limits, and assumptions.
- Automate repetitive work while keeping project state understandable.
- Prefer evidence from code, tests, and configuration over unsupported claims.
- Contribute upstream when a fix can benefit the originating project.

## Current Interests

I am currently exploring **AI Engineering**, **Agentic Systems**, **LLM tooling**, **RAG**, **Application Security**, **Windows Internals**, **Digital Forensics**, and **Open Source**. These are areas of ongoing study and project evolution, not claims of consolidated professional experience in every topic.

## Contact

- [GitHub](https://github.com/celsonaemen)
- [Email](mailto:celso.naemen@proton.me)
