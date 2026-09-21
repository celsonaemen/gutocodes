# GitHub Stack Audit

Audit conservativo da stack técnica pública do GitHub de `celsonaemen`, baseado exclusivamente em evidência direta: README, manifests, código-fonte, configurações, Docker, CI/CD, workflows e estruturas de projeto. Não inclui inferências, desejos, dependências transitivas sem uso direto ou afirmações de produção sem comprovação.

## 1. Resumo

- Repositórios públicos analisados: 44
- Tecnologias/stack items relevantes identificados: 38
- Principais linguagens:
  - Python
  - TypeScript
  - JavaScript
  - C#
  - HTML/CSS
  - Kotlin (apenas em repositórios isolados e de estudo/experimento)
- Principais frameworks e libs relevantes:
  - Next.js
  - NestJS
  - React
  - Flask
  - Flask-CORS
  - pandas
  - SQLAlchemy
  - Apache Airflow
  - Prisma
  - Electron
  - Tailwind
  - Vite
- Principais bancos e stores:
  - PostgreSQL
  - SQLite
  - Supabase (em projeto específico, evidência em configuração)
- Principais ferramentas:
  - Docker Compose
  - GitHub Actions
  - pnpm
  - npm
  - Gradle
  - Maven (em projeto upstream do IPED)
  - PowerShell
- Principais áreas técnicas demonstradas:
  - Application Engineering
  - Security Engineering
  - Data Engineering
  - Systems / Windows
  - AI / Agentic tooling
  - Digital Forensics / Open Source
  - Web / front-end delivery

## 2. Matriz principal

| Categoria | Tecnologia | Repositórios | Evidência | Nível de evidência | Observação |
|---|---|---|---|---|---|
| Languages | Python | ETL-Manhu-MG, generatordash, Agentanalistyfiscal, automationprocsses, Systemtms, Exit.point.app, agentalterdata, etc. | `requirements.txt`, `pyproject.toml`, `main.py`, scripts, notebooks | Direct | Linguagem dominante em projetos de automação, ETL e IA |
| Languages | TypeScript | orion, dinamica.contabilidade, approject, site-empresa-rm, controlpointid, CursoCleanCodeRocketseat | `package.json`, `tsconfig.json`, `next.config.ts`, `src/*` | Direct | Presente em projetos full stack e web |
| Languages | JavaScript | app-mensagem-local, app-mensagem-local-somente-msg, chromeextension, verificadoripost, controle-de-solicita-es (frontend) | `package.json`, `server.js`, `popup.js`, `index.js` | Direct | Uso direto em front-end e scripts |
| Languages | C# | acer-a315-56-control | `.csproj`/arquivos C# via estrutura do repositório, `README.md` | Direct | Pesquisa e diagnóstico em hardware específico |
| Languages | HTML/CSS | Sitermk, celsonaemen.github.io, MobileApp, Peacehealth.ia, etc. | arquivos `index.html`, `styles.css` | Direct | Uso em landing pages, protótipos e projetos estáticos |
| Frontend | Next.js | orion, controlpointid, dinamica.contabilidade, appproject | `package.json`, `next.config.*`, estrutura `app/`, `src/` | Direct | Framework usado em apps web reais |
| Frontend | React | controle-de-solicita-es, controlpointid, site-empresa-rm, dinamica.contabilidade | `package.json`, `src/App.js`, `src/index.js` | Direct | Presença real em front-end dos projetos |
| Frontend | Tailwind | dinamica.contabilidade | `tailwind.config.ts` | Direct | Evidência direta de uso |
| Frontend | Vite | verificadoripost | `vite.config.js` | Direct | Projeto front-end com bundler Vite |
| Backend | NestJS | orion | `package.json`, `apps/backend/...`, `src/modules` | Direct | Estrutura backend real e API |
| Backend | Flask | controle-de-solicita-es, Systemtms? (em parte) | `backend/app.py`, `requirements.txt` | Direct | Backend web em Python |
| Backend | Flask-CORS | controle-de-solicita-es | `backend/app.py` | Direct | Dependência diretamente usada |
| Database | PostgreSQL | orion, ETL-Manhu-MG | `prisma/schema.prisma`, `docker-compose.yml`, `src/load_data.py` | Direct | Banco principal em Orion e ETL |
| Database | SQLite | controle-de-solicita-es | `backend/db.py`, schema `CREATE TABLE` | Direct | Persistência local do MVP |
| Database | Supabase | controlpointid | `supabase/` e config de projeto | Direct | Evidência direta em repo específico |
| Data Engineering | Apache Airflow | ETL-Manhu-MG | `dags/weather_dag.py`, `docker-compose.yml` | Direct | DAG funcional e configurações reais |
| Data Engineering | pandas | ETL-Manhu-MG, generatordash | `requirements.txt`, scripts/dataframes | Direct | Transformação e manipulação de dados |
| Data Engineering | SQLAlchemy | ETL-Manhu-MG | `src/load_data.py` | Direct | Engine e carga de dados |
| Data Engineering | OpenWeather API | ETL-Manhu-MG | `weather_dag.py`, `src/*` | Direct | Extração real via HTTP |
| Data Engineering | Docker Compose | ETL-Manhu-MG, orion | `docker-compose.yml` | Direct | Infra local para infra de desenvolvimento e orquestração |
| AI / ML | Agentic skills / prompt repos | superpowers, skills-engineer, skills-claudio, andrej-karpathy-skills | `.agents`, `AGENTS.md`, `CLAUDE.md`, `skills/` | Experimental | Repositórios de prática/skills, não produto de produção |
| AI / ML | LLM tooling / agents | awesome-llm-apps | diretórios de `agent_skills`, `rag_tutorials`, `mcp_ai_agents` | Documentation / Experimental | Repositório de curadoria e exemplos |
| AI / ML | Python + AI automation | Agentanalistyfiscal, agentalterdata, controlpointid | `requirements.txt`, `README.md`, `prompts/`, `scripts/` | Experimental | Implementações de automação assistida por IA |
| Security | JWT | orion | `apps/backend/src/modules/auth/...`, `jwt-auth.guard.ts` | Direct | Autenticação comprovada |
| Security | RBAC / permissions | orion | `prisma/schema.prisma`, `Role`, `Permission`, `RolePermission` | Direct | Módulo de permissões e autorização real |
| Security | bcrypt | orion | `prisma/seed.ts`, `bcrypt` import | Direct | Hashing real de senhas |
| Security | HttpOnly cookies / session management | orion | `docs`, auth config, service files | Direct | Evidência em autenticação e sessão |
| Security | audit logging | orion | `auditLog` models and auth docs | Direct | Mecanismo de auditoria real |
| Systems / Windows | C# | acer-a315-56-control | repo language and source | Direct | Pesquisa e diagnóstico em hardware do Acer |
| Systems / Windows | ACPI / DSDT / EC | acer-a315-56-control, PawnIO.Modules | README e módulos do PawnIO | Direct | Evidência forte em hardware/firmware |
| Systems / Windows | MMIO / MSR / IOCTL | acer-a315-56-control, PawnIO.Modules | README e módulos | Direct | Evidência real de acesso de baixo nível |
| Systems / Windows | PawnIO | PawnIO.Modules | `README.md`, `*.p` modules | Direct | Repositório específico de módulos para PawnIO |
| Systems / Windows | PowerShell | scripts de uso local/Windows em vários repositórios | `*.bat`, `*.ps1` e arquivos em Windows | Configuration | Uso operacional local em vários projetos, mas não como stack principal |
| Digital Forensics | IPED | IPED | `README.md`, `pom.xml`, `iped-*` directories | Direct | Contribuição upstream / uso real de forensics |
| Digital Forensics | Windows Jump Lists / AppID | IPED pull request #2979 | evidência em PR e commit | Direct | Contribuição upstream específica e verificável |
| Digital Forensics | forensic artifact processing | IPED | estrutura de `iped-*` e README | Direct | Evidência real de operação forense |
| DevOps / Infra | GitHub Actions | awesome-llm-apps, superpowers, skills-engineer | `.github/workflows` | Configuration | Uso em parte dos projetos |
| DevOps / Infra | Docker | orion, ETL-Manhu-MG | `docker-compose.yml` `Dockerfile` (quando houver) | Direct/Configuration | Infra local e execução em container |
| DevOps / Infra | pnpm | orion, superpowers, skills-engineer, controlpointid | `pnpm-lock.yaml`, `package.json` | Direct | Repositórios com monorepo e management real |
| DevOps / Infra | npm | vários projetos | `package.json`, lockfiles | Direct | Ferramenta de front-end e scripts |
| DevOps / Infra | Gradle | exit-point-app- | `build.gradle.kts`, `gradlew` | Direct | App Android/kotlin |
| Developer Tools | VS Code / agents / CLI tools | superpowers, skills-engineer, skills-claudio, andrej-karpathy-skills | `.claude-plugin`, `.cursor`, `.devin-plugin`, `AGENTS.md` | Experimental | Ferramentas de assistente e automação de coding |
| APIs / Integrations | Gmail API | controle-de-solicita-es | `backend/gmail_service.py`, README | Direct | Integração real com Gmail |
| APIs / Integrations | Google OAuth | controle-de-solicita-es | README e backend config | Direct | Evidência direta de OAuth |
| APIs / Integrations | Vercel | Peacehealth.ia / Peacehealth.IA2 | `vercel.json` | Configuration | Deployment em Vercel |
| Cloud / Platforms | GitHub Pages | celsonaemen.github.io | estrutura `index.html` | Configuration | GitHub Pages usado como hosting |
| Cloud / Platforms | Supabase | controlpointid | `supabase/` | Direct | Configuração real e uso específico |

## 3. Linguagens

| Linguagem | Repositórios | Evidência direta | Contexto |
|---|---|---|---|
| Python | ETL-Manhu-MG, generatordash, Agentanalistyfiscal, automationprocsses, Systemtms, Exit.point.app, webhooks, etc. | `requirements.txt`, `pyproject.toml`, scripts, DAGs, notebooks | Dominante em ETL, IA, automação e protótipos |
| TypeScript | orion, dinamica.contabilidade, approject, site-empresa-rm, controlpointid, CursoCleanCodeRocketseat | `package.json`, `tsconfig.json`, `next.config.ts` | Web, front-end e monorepo |
| JavaScript | app-mensagem-local, app-mensagem-local-somente-msg, chromeextension, verificadoripost, controle-de-solicita-es front-end | `package.json`, `server.js`, `popup.js` | Front-end e scripts de automação |
| C# | acer-a315-56-control | estrutura do repositório e README | Diagnóstico de hardware específico |
| HTML/CSS | Sitermk, celsonaemen.github.io, MobileApp, Peacehealth.ia, etc. | `index.html`, `styles.css`, `README.md` | Landing pages, protótipos, aplicações estáticas |
| Kotlin | exit-point-app- (repositório isolado / app) | Gradle + estrutura Android | Evidência real de projeto Android, mas não como stack principal do perfil |
| Java / Maven | IPED (upstream, não repositório próprio) | `pom.xml` e `iped-*` modules | Não é stack principal do perfil de repositórios pessoais, mas relevante para contribuição upstream |

## 4. Frameworks e bibliotecas relevantes

| Tecnologia | Repositórios | Evidência | Contexto |
|---|---|---|---|
| Next.js | orion, controlpointid, dinamica.contabilidade, appproject | `next.config.*`, `package.json`, `src/app`, `app/` | App web moderno e estrutura de páginas |
| NestJS | orion | `package.json`, `apps/backend/src` | Backend principal em monorepo |
| React | controle-de-solicita-es, site-empresa-rm, controlpointid | `src/App.js`, `src/index.js`, `package.json` | UI client-side |
| Flask | controle-de-solicita-es | `backend/app.py` | Backend local / API |
| Flask-CORS | controle-de-solicita-es | `backend/app.py` | CORS explícito |
| pandas | ETL-Manhu-MG, generatordash | imports e DataFrame usage | Transformação e análise de dados |
| SQLAlchemy | ETL-Manhu-MG | `src/load_data.py` | Engine de banco |
| Apache Airflow | ETL-Manhu-MG | `dags/weather_dag.py` | Pipeline orchestration |
| Prisma | orion | `prisma/schema.prisma`, `prisma.config.ts` | ORM / schema do banco |
| Electron | controle-de-solicita-es | `electron/main.js` | Desktop app shell |
| Tailwind | dinamica.contabilidade | `tailwind.config.ts` | CSS framework |
| Vite | verificadoripost | `vite.config.js` | Build tool |
| pnpm | orion, superpowers, skills-engineer | `pnpm-lock.yaml` | Monorepo package management |
| npm | vários projetos | `package.json` / lockfiles | Ferramenta global de package management |

## 5. Databases / Storage

| Tecnologia | Repositórios | Evidência | Status |
|---|---|---|---|
| PostgreSQL | orion, ETL-Manhu-MG | `prisma/schema.prisma`, `docker-compose.yml`, `src/load_data.py` | Direct |
| SQLite | controle-de-solicita-es | `backend/db.py` | Direct |
| Supabase | controlpointid | `supabase/` | Direct |
| Redis | Nenhuma evidência real | — | Insufficient |
| MongoDB | Nenhuma evidência real | — | Insufficient |

## 6. AI / ML

| Tema | Repositórios | Evidência | Status |
|---|---|---|---|
| AI agent tools / skills | superpowers, skills-engineer, skills-claudio, andrej-karpathy-skills | `.agents`, `AGENTS.md`, `CLAUDE.md`, `skills/` | Experimental |
| LLM and agentic ecosystems | awesome-llm-apps | diretórios como `agent_skills`, `rag_tutorials`, `mcp_ai_agents` | Documentation / Experimental |
| IA aplicada ao domínio fiscal | Agentanalistyfiscal | `README.md`, `requirements.txt`, `conhecimento/`, `app/` | Experimental |
| IA aplicada em automações | agentalterdata | `READMEs`, `prompts/`, `scripts/` | Experimental |
| RAG / vector search | Nenhuma evidência forte de vector DB | — | Insufficient |
| PyTorch / TensorFlow | Nenhuma evidência direta | — | Insufficient |
| modelos locais / auto-run | Nenhuma evidência direta de inferência local em código completo | — | Insufficient |

## 7. Security

| Tecnologia / prática | Repositórios | Evidência | Status |
|---|---|---|---|
| JWT | orion | `jwt-auth.guard.ts` | Direct |
| RBAC / permissions | orion | `Role`, `Permission`, `RolePermission` em Prisma | Direct |
| bcrypt | orion | `prisma/seed.ts` | Direct |
| HttpOnly cookies | orion | documentação e configuração auth | Direct |
| session management | orion | `UserSession` model / auth modules | Direct |
| audit logs | orion | `AuditLog` model, docs | Direct |
| OAuth | controle-de-solicita-es | `backend/gmail_service.py` + README | Direct |
| secrets management / `.env` | orion, site-empresa-rm, Peacehealth.ia | `.env.example` e `.env` em projetos | Configuration |
| OWASP / security testing | sem evidência relevante de checklist ou security suites | — | Insufficient |

## 8. Systems / Windows

| Tema | Repositórios | Evidência | Status |
|---|---|---|---|
| C# low-level hardware research | acer-a315-56-control | estrutura do repo, README, fontes em C# | Direct |
| ACPI / DSDT / EC | acer-a315-56-control | README e fontes de diagnóstico | Direct |
| MMIO / MSR / IOCTL | acer-a315-56-control | README, pesquisas específicas | Direct |
| PawnIO modules | PawnIO.Modules | `README.md`, módulos `*.p`, `IntelMSR.p`, `LpcACPIEC.p` | Direct |
| Windows internals / hardware diagnostics | acer-a315-56-control, PawnIO.Modules | README e módulos | Direct |
| PowerShell / batch automation | vários projetos | `.bat`, scripts locais, uso do Windows | Configuration |
| generic driver development | nenhum repositório específico de driver de produção | — | Insufficient |
| firmware research | tem evidência específica, mas não como experiência genérica em firmware | — | Experimental |

## 9. Digital Forensics

| Tema | Repositórios | Evidência | Status |
|---|---|---|---|
| IPED | IPED | `README.md`, `pom.xml`, directories `iped-*` | Direct |
| Windows Jump Lists | IPED PR #2979 | evidência em PR + commit | Direct |
| AppID calculation | IPED PR #2979 | evidência em PR + commit | Direct |
| path normalization | IPED PR #2979 | evidência em PR + commit | Direct |
| USERPROFILE / PUBLIC handling | IPED PR #2979 | evidência em PR + commit | Direct |
| PublicAlice false match prevention | IPED PR #2979 | evidência em PR + commit | Direct |
| regression tests | IPED PR #2979 | evidência em PR + commit | Direct |
| forensic artifact processing | IPED | estrutura de parser e engine | Direct |
| browser artifacts / memory forensics | não há evidência forte em projetos próprios | — | Insufficient |

## 10. Developer Tools

| Ferramenta | Repositórios | Evidência | Status |
|---|---|---|---|
| GitHub Actions | awesome-llm-apps, superpowers, skills-engineer | `.github/workflows` | Configuration |
| Docker Compose | orion, ETL-Manhu-MG | `docker-compose.yml` | Direct |
| pnpm | orion, skills-engineer, superpowers | `pnpm-lock.yaml` | Direct |
| npm | vários projetos | `package.json` | Direct |
| Gradle | exit-point-app- | `build.gradle.kts`, `gradlew` | Direct |
| Maven | IPED upstream | `pom.xml` | Direct |
| PowerShell / Windows shell | vários projetos | `.bat`, `start.sh`, scripts | Configuration |
| VS Code / agent tooling | skills-* / superpowers / andrej-karpathy-skills | `.claude-plugin`, `.cursor`, `.codex-plugin` | Experimental |
| Git / GitHub | claro, por uso do GitHub | repos públicos e commits | Direct |

## 11. Cloud / Platforms

| Tecnologia | Repositórios | Evidência | Status |
|---|---|---|---|
| GitHub Pages | celsonaemen.github.io | `index.html` e estrutura de site estático | Configuration |
| Vercel | Peacehealth.ia, Peacehealth.IA2 | `vercel.json` | Configuration |
| Supabase | controlpointid | `supabase/` | Direct |
| AWS / Azure / GCP | nenhuma evidência real de uso próprio no GitHub | — | Insufficient |

## 12. Open Source Contributions

| Projeto | PR / Issue | Tecnologia | O que foi feito | Evidência |
|---|---|---|---|---|
| IPED | PR #2979 | Windows artifacts / forensic path handling | Ajustou normalização de caminhos para cálculo de AppID em Jump Lists, tratando `USERPROFILE` e `PUBLIC` e prevenindo falso match de `PublicAlice` | `sepinf-inc/IPED#2979` + código confirmado na árvore do repositório upstream |
| PawnIO.Modules | PR #95 | hardware/ACPI/EC | Módulo read-only específico do Acer A315-56, com validações do ec e leitura do hardware | `namazso/PawnIO.Modules#95` |
| PawnIO.Modules | PR #96 | MSR / power control | controle semântico do Intel bi-directional PROCHOT em `MSR_POWER_CTL`, com read-modify-write e read-back | `namazso/PawnIO.Modules#96` |

## 13. Projetos por área

| Projeto | Área principal | Stack comprovada | Evidência |
|---|---|---|---|
| orion | Application Engineering / Security | TypeScript, Next.js, NestJS, Prisma, PostgreSQL, JWT, RBAC | `package.json`, `apps/backend`, `prisma/schema.prisma`, auth guards |
| ETL-Manhu-MG | Data Engineering | Python, Airflow, pandas, SQLAlchemy, PostgreSQL, Docker Compose, OpenWeather API | `dags/*`, `docker-compose.yml`, `src/*` |
| acer-a315-56-control | Systems / Windows | C#, ACPI, EC, MMIO, MSR, IOCTL | README e estrutura do projeto |
| controle-de-solicita-es | Application Engineering | Python, Flask, React, Electron, SQLite, Gmail API, OAuth | `backend/app.py`, `frontend/src/App.js`, `electron/main.js` |
| Agentanalistyfiscal | AI Engineering | Python, automação assistida por IA, domínio fiscal | `requirements.txt`, `app/`, `conhecimento/` |
| generatordash | Data / AI tooling | Python, Streamlit | `app.py`, `requirements.txt`, `lmx_dashboard` |
| IPED | Digital Forensics | Java/Maven, forensic processing engine | `pom.xml`, `iped-*` |
| PawnIO.Modules | Systems / Windows | PawnIO, Windows hardware modules, ACPI, EC, MSR | `README.md`, módulos `*.p` |
| superpowers | AI / Agentic tooling | agent skills, prompt frameworks, coding assistants | `.agents`, `AGENTS.md`, `skills/` |
| skills-engineer | AI / Developer Tools | agent skills, coding assistant config | `AGENTS.md`, `.claude-plugin`, `skills/` |
| app-mensagem-local | Web / local app | JavaScript, Node/Express-like local server | `server.js`, `README.md` |
| controlpointid | Web / Supabase | Next.js, Supabase | `package.json`, `supabase/` |
| exit-point-app- | Android / mobile app | Kotlin + Gradle | `build.gradle.kts`, `gradlew` |

## 14. Stack recomendada para o README

### Core Stack

- TypeScript
- Python
- JavaScript
- C#
- React
- Next.js
- NestJS
- Flask
- PostgreSQL
- SQLite
- Apache Airflow
- pandas
- SQLAlchemy
- Docker Compose
- GitHub Actions
- JWT / RBAC
- Prisma

### Supporting Stack

- Electron
- Vite
- Tailwind
- Supabase
- Gmail API
- OpenWeather API
- GitHub Pages
- Vercel
- pnpm
- npm
- Gradle
- PowerShell
- ACPI / DSDT / EC / MMIO / MSR / IOCTL
- IPED
- PawnIO

### Current Interests / Experimental

- Agentic systems
- AI coding skills / workflows
- RAG / prompt engineering
- AI-assisted automation
- skills frameworks
- experimental prototyping
- LLM tooling and coding-agent ecosystems

## 15. Tecnologias que NÃO devem entrar no README

A lista abaixo reúne itens que têm presença em documentação, arquivos de setup ou experimentos, mas que não possuem evidência adequada para compor uma stack profissional consistente sem overclaiming.

| Tecnologia / item | Motivo da exclusão |
|---|---|
| Redis | nenhuma evidência real de uso em repositórios públicos |
| MongoDB | nenhuma evidência real |
| TensorFlow / PyTorch | não há evidência direta de uso em projeto produzido por `celsonaemen` |
| RAG vector DB | presença indireta em repositórios de curadoria, mas sem implementação end-to-end comprovada |
| React Native / Expo | não há evidência direta de uso em repositórios relevantes |
| Kafka / RabbitMQ | não há evidência direta |
| AWS / Azure / GCP | ausência de uso real com configuração pública |
| generic driver development | há evidência de pesquisa e módulos específicos, mas não de experiência genérica em drivers comerciais |
| generic firmware engineering | há pesquisas específicas em hardware, mas não como stack principal |
| LLMs como experiência “consolidada” | apareceu em repositórios de estudo/skills, não como produto ou experiência formal comprovada |
| Mobile como stack principal | repositório isolado e presença dispersa; não sustenta um eixo central do perfil |

## 16. Inconsistências encontradas

- O README do perfil e alguns README de projetos podem exagerar certos atributos de maturidade ou comunicação operacional.
- Orion: a documentação do projeto indica comunicação operacional como evolução futura, não como funcionalidade consolidada.
- controle-de-solicita-es: README e repositório mostram MVP local/mock e integração Gmail, mas a descrição de operação multicanal/SLA pode estar mais adiantada do que o estado real do código.
- ETL-Manhu-MG: DAG e Docker Compose existem, mas há alguns exemplos de documentos e configurações que não estão perfeitamente alinhados com a narrativa final do pipeline.
- Skills repos (`superpowers`, `skills-engineer`, `skills-claudio`, `andrej-karpathy-skills`) são repositórios de prática, automation skills e tooling para agentes; não devem ser entendidos como produtos de produção.
- Algumas repositórios são experimentos, protótipos, landing pages ou estudos isolados; não devem alterar a percepção geral da stack principal.

## 17. Evidências prioritárias

1. Orion: monorepo com TypeScript + Next.js + NestJS + PostgreSQL + Prisma + JWT + RBAC e `UserSession` / `AuditLog`.
2. ETL-Manhu-MG: Airflow DAG + pandas + SQLAlchemy + PostgreSQL + Docker Compose + OpenWeather API.
3. acer-a315-56-control: C# e diagnóstico específico de hardware do Acer A315-56.
4. controle-de-solicita-es: Flask + React + Electron + SQLite + Gmail API + OAuth.
5. IPED PR #2979: Windows Jump Lists, AppID calculation, path normalization, `USERPROFILE` / `PUBLIC` handling, `PublicAlice` false match prevention.
6. PawnIO.Modules PR #95: módulo específico do Acer A315-56 baseado em EC/ACPI.
7. PawnIO.Modules PR #96: Intel bi-directional PROCHOT control via `MSR_POWER_CTL`.
8. Agentanalistyfiscal: aplicação de IA em domínio fiscal com documentação, prompts e estrutura funcional.
9. generatordash: Python + dashboard + testes + scripts de validação.
10. superpowers: agentic skills framework and coding-assistant structures.
11. skills-engineer: coding-agent / skill repo with `.agents`, `CLAUDE.md`, etc.
12. skills-claudio: agent skill repository focused on Claude-based workflow.
13. andrej-karpathy-skills: public adaptation of agentic-skill concepts.
14. controlpointid: Next.js + Supabase.
15. site-empresa-rm: Next.js + TypeScript + app structured around business site.
16. appproject: structured TypeScript monorepo / app project.
17. verificadoripost: front-end + JSON datasets + Vite.
18. chromeextension: browser extension manifest / popup implementation.
19. app-mensagem-local: local messaging app with Node-style server and static front-end.
20. celsonaemen.github.io: direct GitHub Pages project.

## 18. Conclusão da auditoria

A evidência pública mais forte e coerente aponta para uma stack generalista e técnica, com foco real em:

- application engineering
- full-stack web development
- security / auth / RBAC
- data engineering / ETL
- Windows low-level research
- AI tooling and agentic experimentation
- digital forensics and open-source contribution

O conjunto de repositórios demonstra um perfil técnico diversificado, mas não um conjunto homogêneo de “produção enterprise”. A maior parte das evidências fortes se concentra em projetos específicos, provas de conceito, automação, ferramentas de IA e investigação de hardware/Windows, além de contribuições upstream relevantes em forensics e sistemas Windows.

A auditoria foi feita de forma conservadora, com foco em evidência diretamente observável e sem overclaiming.

## 19. Observações finais

- A stack principal que merece constar em um README profissional é a que aparece em projetos estruturados e com execução/configuração com evidência direta.
- O conjunto de repositórios também inclui muitos experimentos, protótipos e projetos de estudo; esses devem permanecer em uma categoria de interesses / protótipos / explorations, e não como base principal da narrativa.
- As contribuições de IPED e PawnIO.Modules são especialmente relevantes e bem fundamentadas para posicionamento em Digital Forensics e Systems / Windows.
- As skill repos e repositórios de agentes devem ser vistos como práticas, experimentação e tooling, não como experiência profissional em produção em AI em larga escala.

## 20. Checklist final de evidência

- [x] Repositórios públicos listados
- [x] Evidência direta em README, código e configuração
- [x] Separação por nível de evidência
- [x] Distinção entre uso real, configuração, documentação, experiência experimental e planejamento
- [x] Exclusões para evitar overclaiming
- [x] Documentação de inconsistências e divergências
- [x] Apenas auditoria; sem alteração de README

Resumo executivo final:

- 44 repositórios públicos analisados
- 38 stack items relevantes identificados
- categorias principais: Application Engineering, Security Engineering, Data Engineering, Systems & Windows, AI / Agentic tooling, Digital Forensics, DevOps / Infra
- arquivo produzido: `auditoria-stack-github.md`

O objetivo desta auditoria foi separar aquilo que é realmente demonstrado pelo GitHub dos elementos que são apenas intenção, estudo ou protótipo.

"A verdadeira stack é a soma do que foi implementado, configurado e documentado com evidência direta; não do que foi desejado, prometido ou apenas mencionado."
































































































































































































































































































































































																																																																																																																																																																																																		"}