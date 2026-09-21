# GitHub Stack Audit — Classification Review

Revisão crítica da auditoria anterior, usando os 44 repositórios públicos identificados e evidências observáveis em código, manifests, configuração, workflows, testes e pull requests. A classificação abaixo não é ranking de qualidade nem de senioridade. Ela indica apenas o quanto cada tecnologia pode sustentar uma afirmação pública de stack.

## Escopo e método

- Repositórios públicos no escopo: 44.
- Itens tecnológicos normalizados para classificação: 38.
- READMEs foram usados como índice e contexto, não como prova isolada de implementação.
- Dependências foram separadas de uso direto.
- Forks, repositórios de curadoria, skills e protótipos não foram tratados como experiência de produção.
- A classificação considera profundidade, relevância arquitetural, evidência direta, recorrência e estado do projeto.

## 1. Classificação dos 38 itens tecnológicos

| Tecnologia | Classificação | Repositórios | Evidência concreta | Motivo |
|---|---|---|---|---|
| Python | CORE | ETL-Manhu-MG, generatordash, Agentanalistyfiscal, agentalterdata, automationprocsses, Systemtms, Exit.point.app e outros | `.py`, `requirements.txt`, `pyproject.toml`, DAGs e notebooks | Linguagem usada diretamente em vários projetos relevantes. |
| TypeScript | CORE | orion, controlpointid, dinamica.contabilidade, approject, site-empresa-rm, CursoCleanCodeRocketseat | `.ts`, `tsconfig.json`, `package.json`, `next.config.*` | Uso direto em aplicações e estruturas web. |
| JavaScript | CORE | controle-de-solicita-es, app-mensagem-local, app-mensagem-local-somente-msg, chromeextension, verificadoripost, Peacehealth.ia | `.js`, `package.json`, `server.js`, `popup.js` | Uso direto em front-end, servidores locais e extensões. |
| C# | SUPPORTING | acer-a315-56-control | Arquivos-fonte do projeto e linguagem principal do repositório | Evidência técnica significativa, mas concentrada em um projeto de hardware específico. |
| Kotlin | EXPERIMENTAL | exit-point-app- | Estrutura Android e `build.gradle.kts` | Uso real em projeto isolado; não sustenta stack mobile central. |
| HTML/CSS | SUPPORTING | Sitermk, celsonaemen.github.io, MobileApp, Peacehealth.ia, skyscan e outros | `index.html`, `styles.css`, `style.css` | Uso direto e recorrente, mas principalmente em sites, protótipos e interfaces estáticas. |
| Next.js | CORE | orion, controlpointid, dinamica.contabilidade, approject | `next.config.*`, `package.json`, `app/`, `src/` | Framework usado diretamente em múltiplas aplicações web. |
| React | CORE | controle-de-solicita-es, controlpointid, site-empresa-rm e projetos web relacionados | `frontend/src/App.js`, `frontend/src/index.js`, dependências e componentes | Uso direto em interface funcional. |
| NestJS | CORE | orion | `apps/backend`, módulos NestJS e `package.json` | Framework central do backend do Orion. |
| Flask | SUPPORTING | controle-de-solicita-es | `backend/app.py`, rotas, `requirements.txt` | Backend direto e funcional, porém concentrado em um MVP local. |
| Prisma | CORE | orion | `prisma/schema.prisma`, `prisma.config.ts`, `PrismaClient` | Parte central da persistência e do modelo de dados do Orion. |
| Electron | SUPPORTING | controle-de-solicita-es | `electron/main.js`, `package.json` | Shell desktop real, limitado a um projeto. |
| Tailwind | SUPPORTING | dinamica.contabilidade | `tailwind.config.ts`, configuração PostCSS e classes no projeto | Uso direto, mas em projeto web específico. |
| Vite | SUPPORTING | verificadoripost | `vite.config.js`, `package.json`, estrutura `src/` | Bundler usado diretamente em uma aplicação. |
| PostgreSQL | CORE | orion, ETL-Manhu-MG | `prisma` datasource, `docker-compose.yml`, SQLAlchemy engine e schema SQL | Banco usado diretamente em dois projetos relevantes. |
| SQLite | SUPPORTING | controle-de-solicita-es | `backend/db.py`, `sqlite3`, `CREATE TABLE` | Persistência direta de um MVP desktop/local. |
| Supabase | SUPPORTING | controlpointid | diretório `supabase/`, configuração e código do projeto | Evidência real em projeto específico; não recorrente na stack principal. |
| Apache Airflow | CORE | ETL-Manhu-MG | `dags/weather_dag.py`, imports Airflow, serviço Docker | Orquestração diretamente implementada no pipeline. |
| pandas | CORE | ETL-Manhu-MG, generatordash | DataFrames, `read_parquet`, `to_sql`, dependências e scripts | Uso direto em transformação e processamento de dados. |
| SQLAlchemy | CORE | ETL-Manhu-MG | `src/load_data.py`, `create_engine`, `text` | Uso direto na conexão e carga PostgreSQL. |
| Docker Compose | CORE | ETL-Manhu-MG, orion | `docker-compose.yml`, serviços e volumes | Configuração operacional relevante em dois projetos. |
| JWT | CORE | orion | `jwt-auth.guard.ts`, validação de access token e módulos de autenticação | Implementação direta de autenticação. |
| RBAC / permissions | CORE | orion | modelos `Role`, `Permission`, `RolePermission` e guards | Autorização estruturada diretamente no domínio. |
| bcrypt / password hashing | SUPPORTING | orion | import e uso em `prisma/seed.ts` | Uso direto, mas como componente específico do fluxo de autenticação. |
| HttpOnly cookies / sessions | CORE | orion | configuração de cookies, modelos `RefreshToken`/`UserSession` e módulos de auth | Evidência direta de sessão e proteção de tokens. |
| Audit logging | CORE | orion | modelo `AuditLog`, ações de auditoria e documentação técnica | Mecanismo explícito de auditoria no domínio. |
| OAuth / Gmail API | SUPPORTING | controle-de-solicita-es | `gmail_service.py`, dependências Google OAuth e fluxo de credenciais | Integração real, porém específica do MVP. |
| ACPI / DSDT / EC | CORE | acer-a315-56-control, PawnIO.Modules e PR #95 | documentação de hardware, DSDT, mailbox EC e módulos Pawn | Área de sistemas demonstrada por código/pesquisa específica. |
| MMIO / MSR / IOCTL | CORE | acer-a315-56-control, PawnIO.Modules e PR #96 | módulos, mapas de hardware, `MSR_POWER_CTL`, operações e limites | Uso técnico direto em pesquisa e módulos de baixo nível. |
| PawnIO | CORE | PawnIO.Modules, PRs #95 e #96 | módulos `.p`, `README.md`, PRs upstream | Tecnologia central nas contribuições de baixo nível. |
| IPED / forensic processing | CORE | IPED e PR #2979 | módulos `iped-*`, `pom.xml`, engine/parsers e contribuição upstream | Evidência direta de colaboração em ferramenta forense; não é projeto autoral original. |
| Windows Jump Lists / AppID | CORE | IPED PR #2979 | `AppIDCalculator`, testes e PR integrada | Contribuição upstream concreta em artefatos Windows. |
| GitHub Actions | SUPPORTING | IPED, awesome-llm-apps, superpowers, skills-engineer e outros | `.github/workflows` e configurações de CI | Configuração real em parte dos repositórios, mas não evidência de uma plataforma de produção própria. |
| npm / pnpm | SUPPORTING | orion, controlpointid, superpowers, skills-engineer, vários projetos JS/TS | `package.json`, lockfiles, `pnpm-workspace.yaml` | Ferramentas realmente usadas; não devem dominar o posicionamento. |
| Gradle / Maven | SUPPORTING | exit-point-app-, orbot-android, IPED | `build.gradle*`, `gradlew`, `pom.xml` | Evidência direta, mas distribuída entre Android e contribuição/fork upstream. |

### Tecnologias não incluídas nos 38 itens

Alguns nomes que apareceram na auditoria bruta foram tratados como integração, contexto ou exclusão, não como itens centrais da matriz: OpenWeather API, Vercel, GitHub Pages, PowerShell, Streamlit, RAG, LLMs, agentic systems, VS Code, Figma, Postman, Redis, MongoDB, AWS, Azure e GCP. Eles são classificados nas seções específicas abaixo para evitar misturar frameworks, linguagens, plataformas, práticas e interesses.

## 2. Core Stack

| Área | Tecnologias | Base de evidência |
|---|---|---|
| Languages | Python, TypeScript, JavaScript | Uso direto em múltiplos projetos com código-fonte e manifests. |
| Application Engineering | Next.js, React, NestJS, Prisma, PostgreSQL, Docker Compose | Orion, projetos web e configuração executável. |
| Data Engineering | Python, pandas, Apache Airflow, SQLAlchemy, PostgreSQL, Docker Compose | ETL-Manhu-MG, DAGs, carga SQL e containers. |
| Security Engineering | JWT, RBAC/permissions, authentication, authorization, HttpOnly sessions, audit logging | Código de autenticação, modelos de domínio e guards do Orion. |
| Systems & Windows | C#, ACPI, DSDT, EC, MMIO, MSR, IOCTL, PawnIO | Acer A315-56, PawnIO.Modules e PRs #95/#96. |
| AI Engineering | Python para automação assistida por IA e ferramentas de agentes | Agentanalistyfiscal/agentalterdata e repos de skills; classificado como implementação experimental, não como experiência de produção. |
| Digital Forensics | IPED, Windows artifacts, Jump Lists, AppID calculation | Repositório IPED e PR #2979. |

Nota: AI Engineering permanece no Core Stack apenas como área de implementação experimental verificável. LLM, RAG e vector search não entram como tecnologias core.

## 3. Supporting Stack

- C# — uso técnico relevante, mas concentrado no Acer A315-56.
- HTML/CSS — uso recorrente em sites e protótipos.
- Flask — backend funcional no MVP de solicitações.
- Electron — shell desktop do MVP.
- SQLite — persistência local.
- Supabase — projeto específico `controlpointid`.
- Tailwind — projeto específico `dinamica.contabilidade`.
- Vite — `verificadoripost`.
- bcrypt — componente direto do auth do Orion.
- Gmail API / OAuth — integração específica do MVP.
- GitHub Actions — configuração real em alguns repositórios.
- npm / pnpm — gerenciamento de pacotes.
- Gradle / Maven — Android e IPED/upstream.

## 4. Experimental / Current Interests

- Agentic systems — implementação em repositórios de skills e automação, sem evidência de produto de produção.
- AI coding skills / workflows — `superpowers`, `skills-engineer`, `skills-claudio` e `andrej-karpathy-skills`.
- AI-assisted automation — `Agentanalistyfiscal` e `agentalterdata`, projetos em evolução.
- LLM tooling — exemplos e curadoria em `awesome-llm-apps`.
- RAG — aparece em curadoria, documentação e direção de projetos; não há implementação end-to-end forte suficiente para Core.
- Embeddings / vector databases — não confirmados em implementação própria.
- Kotlin / Android — uso real em `exit-point-app-` e presença em `orbot-android`, mas fora do eixo principal.
- Streamlit — uso no `generatordash` e em componentes de interface de projeto fiscal; específico/experimental.
- PowerShell — scripts e automação local de Windows; não representa uma competência independente ampla.

## 5. Exclusions

| Item | Motivo para não colocar como stack pública principal |
|---|---|
| Redis | Nenhum uso direto confirmado. |
| MongoDB | Nenhum uso direto confirmado. |
| RabbitMQ / Kafka | Apenas ausência ou menções contextuais; sem implementação confirmada. |
| AWS / Azure / GCP | Não há configuração pública de uso próprio que sustente a afirmação. |
| Kubernetes / Terraform | Não há evidência direta suficiente. |
| S3 / Stripe / GraphQL | Não há uso direto confirmado nos projetos auditados. |
| RAG como competência consolidada | Curadoria/documentação e intenção não equivalem a implementação avaliada. |
| Vector databases / embeddings | Não há pipeline próprio comprovado. |
| PyTorch / TensorFlow | Não há uso direto confirmado. |
| Vercel como experiência de deployment | `vercel.json` em protótipos confirma configuração, não experiência ampla de plataforma. |
| GitHub Pages como competência cloud | Site estático e estrutura do repositório não comprovam engenharia de plataforma. |
| Generic driver development | Há pesquisa e módulos específicos, não experiência genérica com drivers de produção. |
| Generic firmware engineering | Há investigação específica do Acer/EC/ACPI, não uma stack geral de firmware. |
| Production scale, uptime, performance, CVEs e métricas | Não há fonte verificável suficiente nos repositórios auditados. |
| Senioridade, liderança e experiência profissional | Não podem ser derivadas apenas da existência dos projetos. |
| Next.js/Prisma/NestJS upstream contributions | Uso nos próprios projetos não comprova contribuição upstream nesses frameworks. |
| NPM package maintenance | Não há evidência pública suficiente de manutenção de pacotes próprios relevantes. |
| Mobile como eixo principal | Kotlin/Android aparece de forma isolada ou em fork/projeto específico. |

## 6. Potential Overclaims

- “AI Engineer” como experiência consolidada: os repositórios demonstram automação assistida por IA, skills e protótipos; não demonstram necessariamente sistemas de IA avaliados em produção.
- “RAG” ou “vector search” como stack: há diretórios, curadoria e interesses, mas não evidência suficiente de um pipeline próprio completo.
- “Agentic systems” sem qualificador: existe uso real em skills e tooling, porém em projetos experimentais e de metodologia.
- “Cloud engineering”: Vercel/GitHub Pages/Supabase aparecem em configuração ou projeto específico; não comprovam experiência ampla em AWS, Azure, GCP ou infraestrutura cloud.
- “Driver development” genérico: o Acer A315-56 e PawnIO demonstram pesquisa de baixo nível e módulos específicos, não drivers de produção generalizados.
- “Firmware engineering” genérico: há reverse engineering e interação ACPI/EC delimitada por modelo; não é evidência de engenharia geral de firmware.
- “Digital forensics” como autoria do IPED: o IPED é projeto externo; a evidência correta é contribuição upstream em uma ferramenta forense, não autoria do produto.
- “Full-stack production systems”: Orion e outros projetos demonstram arquitetura e código, mas não deployment, escala, disponibilidade ou operação profissional comprovados.
- “PostgreSQL expertise” sem contexto: PostgreSQL é usado diretamente em Orion e ETL, mas a auditoria não mede profundidade ou experiência profissional.
- “Security engineering” amplo: há auth, RBAC, sessão, hashing e auditoria no Orion; isso não comprova pentest, bug bounty, OWASP ou CVEs.
- “Data platform engineering”: o ETL comprova pipeline e orquestração, mas não escala, governança, qualidade de dados ou operação contínua.
- “Open source maintainer”: PRs e repositórios públicos comprovam contribuição e publicação; não comprovam manutenção de projetos de terceiros em sentido amplo.

## 7. Projetos por área

| Projeto | Área principal | Stack comprovada | Estado da evidência |
|---|---|---|---|
| `orion` | Application Engineering / Security | TypeScript, Next.js, NestJS, Prisma, PostgreSQL, JWT, RBAC | Direct; projeto em evolução |
| `ETL-Manhu-MG` | Data Engineering | Python, Airflow, pandas, SQLAlchemy, PostgreSQL, Docker Compose, OpenWeather API | Direct; pipeline de portfólio |
| `acer-a315-56-control` | Systems / Windows | C#, ACPI, DSDT, EC, MMIO, MSR, IOCTL | Direct/Experimental; hardware específico |
| `controle-de-solicita-es` | Application Engineering | Python, Flask, React, Electron, SQLite, Gmail API, OAuth | Direct; MVP local/mock |
| `Agentanalistyfiscal` | AI Engineering | Python, automação assistida por IA, Streamlit/componentes fiscais | Experimental |
| `agentalterdata` | AI / automation | prompts, conhecimento, scripts e skills | Experimental; dados e casos exigem cautela |
| `generatordash` | Data / UI tooling | Python, Streamlit, testes e scripts de validação | Experimental/aplicado |
| `IPED` | Digital Forensics | Java/Maven, engine, parsers e artefatos forenses | Upstream contribution; projeto externo |
| `PawnIO.Modules` | Systems / Windows | PawnIO, ACPI, EC, MMIO, MSR | Direct no repositório externo via PRs |
| `controlpointid` | Web / data platform | Next.js, JavaScript/TypeScript, Supabase | Direct em projeto específico |
| `exit-point-app-` | Mobile | Kotlin, Gradle, Android structure | Experimental/isolated |
| `app-mensagem-local` | Web / local application | JavaScript, Node-style server, static UI | Direct; aplicação local |
| `verificadoripost` | Web / data UI | JavaScript, Vite, JSON datasets | Direct; aplicação específica |
| `chromeextension` | Browser tooling | JavaScript, Chrome extension manifest | Direct; extensão específica |
| `superpowers` | AI / developer tooling | skills, agent configs, plugin manifests | Experimental/tooling |
| `skills-engineer` | AI / developer tooling | skills, agent configs, package tooling | Experimental/tooling |

## 8. Open Source Contributions

| Projeto | PR/Issue | Tecnologia | O que foi feito | Evidência |
|---|---|---|---|---|
| IPED | [PR #2979](https://github.com/sepinf-inc/IPED/pull/2979) | Java, Windows Jump Lists, AppID calculation | Corrigiu a normalização de caminhos para executáveis em pastas de usuário e pública; tratou `USERPROFILE` e `PUBLIC`, evitou o falso match `PublicAlice` e adicionou testes de regressão. A PR foi integrada. | PR, diff e arquivos `AppIDCalculator.java` / `AppIDCalculatorTest.java` |
| PawnIO.Modules | [PR #95](https://github.com/namazso/PawnIO.Modules/pull/95) | PawnIO, ACPI/EC, MMIO | Propõe módulo read-only específico do Acer A315-56, com gate de hardware, mailbox EC, limites de acesso e validação descrita na PR. A PR permanece aberta/draft no estado auditado. | Descrição, diff e validação da PR |
| PawnIO.Modules | [PR #96](https://github.com/namazso/PawnIO.Modules/pull/96) | PawnIO, Intel MSR | Propõe controle semântico de `ENABLE_BIDIR_PROCHOT` em `MSR_POWER_CTL`, com read-modify-write, validação e read-back. A PR permanece aberta/draft no estado auditado. | Descrição, diff e validação da PR |

## 9. Inconsistências relevantes

- A auditoria anterior misturava tecnologias, práticas, plataformas e áreas compostas como se todas fossem itens comparáveis.
- A contagem anterior de 38 não correspondia claramente a 38 linhas normalizadas; esta revisão define explicitamente os 38 itens classificados.
- `controle-de-solicita-es` é descrito em metadados como multicanal/enterprise, mas o README e o código demonstram principalmente um MVP local com Gmail, mock e SQLite.
- `ETL-Manhu-MG` contém diferenças entre documentação, DAGs e configurações Docker; Airflow/PostgreSQL são evidências diretas, mas maturidade operacional não deve ser inferida.
- `orion` possui base full stack e segurança implementada, mas comunicação operacional real aparece na documentação como evolução planejada.
- `awesome-llm-apps` é repositório de curadoria/exemplos; não deve ser contado como prova de autoria de cada framework, agente ou aplicação listada.
- `orbot-android` é um repositório associado ao projeto Orbot; sua estrutura Android não deve ser tratada automaticamente como autoria integral.
- `IPED` e `PawnIO.Modules` são repositórios externos; devem aparecer como contribuição upstream, não como projetos autorais.
- `vercel.json`, `.env`, lockfiles e diretórios de configuração confirmam configuração ou intenção em alguns casos, mas não necessariamente deployment, uso em produção ou domínio amplo da plataforma.
- A presença de uma dependência em `package.json` ou `requirements.txt` foi rebaixada quando não havia uso direto verificável.

## 10. Evidências prioritárias para documentação

1. Orion — autenticação e autorização
   - Repositório: `celsonaemen/orion`
   - Arquivos: `apps/backend/src/modules/auth/guards/jwt-auth.guard.ts`, `apps/backend/prisma/schema.prisma`
   - Evidência: JWT, usuários, roles, permissions, refresh tokens, sessões e auditoria.
   - Demonstra: Application Engineering e Security Engineering diretamente implementadas.

2. Orion — stack full stack
   - Repositório: `celsonaemen/orion`
   - Arquivos: `apps/`, `package.json`, `pnpm-workspace.yaml`, `docker-compose.yml`
   - Evidência: Next.js, NestJS, TypeScript, Prisma e PostgreSQL.
   - Demonstra: arquitetura de aplicação web em monorepo.

3. ETL-Manhu-MG — Airflow DAG
   - Repositório: `celsonaemen/ETL-Manhu-MG`
   - Arquivo: `dags/weather_dag.py`
   - Evidência: extração OpenWeather, transformação pandas e carga PostgreSQL encadeadas em DAG.
   - Demonstra: pipeline de Data Engineering implementado.

4. ETL-Manhu-MG — carga SQL
   - Repositório: `celsonaemen/ETL-Manhu-MG`
   - Arquivo: `src/load_data.py`
   - Evidência: SQLAlchemy, PostgreSQL, criação de tabela e `to_sql`.
   - Demonstra: persistência e integração de dados.

5. ETL-Manhu-MG — containerização
   - Repositório: `celsonaemen/ETL-Manhu-MG`
   - Arquivo: `docker-compose.yml`
   - Evidência: serviços Airflow e PostgreSQL.
   - Demonstra: configuração de execução local containerizada.

6. Acer A315-56 — diagnóstico específico
   - Repositório: `celsonaemen/acer-a315-56-control`
   - Arquivos: `src/`, `docs/`, `research/`, `README.md`
   - Evidência: C#, ACPI/DSDT, EC, MMIO e escopo de hardware.
   - Demonstra: pesquisa aplicada de baixo nível, limitada ao modelo documentado.

7. PawnIO PR #95 — módulo EC read-only
   - Repositório externo: `namazso/PawnIO.Modules`
   - Arquivo: PR [#95](https://github.com/namazso/PawnIO.Modules/pull/95)
   - Evidência: módulo específico do Acer A315-56, gate de hardware e mailbox EC.
   - Demonstra: contribuição upstream de baixo nível; PR aberta/draft.

8. PawnIO PR #96 — PROCHOT
   - Repositório externo: `namazso/PawnIO.Modules`
   - Arquivo: PR [#96](https://github.com/namazso/PawnIO.Modules/pull/96)
   - Evidência: `MSR_POWER_CTL`, read-modify-write, read-back e gates.
   - Demonstra: contribuição upstream de controle semântico de MSR; PR aberta/draft.

9. IPED PR #2979 — Jump Lists
   - Repositório externo: `sepinf-inc/IPED`
   - Arquivo: PR [#2979](https://github.com/sepinf-inc/IPED/pull/2979)
   - Evidência: normalização de caminhos, `USERPROFILE`, `PUBLIC`, `PublicAlice` e testes.
   - Demonstra: contribuição upstream integrada em processamento forense de artefatos Windows.

10. controle-de-solicita-es — backend
    - Repositório: `celsonaemen/controle-de-solicita-es`
    - Arquivos: `backend/app.py`, `backend/db.py`, `backend/gmail_service.py`
    - Evidência: Flask, SQLite, Gmail, filtros, status e controles locais.
    - Demonstra: aplicação local integrada, não operação multicanal consolidada.

11. controle-de-solicita-es — desktop
    - Repositório: `celsonaemen/controle-de-solicita-es`
    - Arquivo: `electron/main.js`
    - Evidência: BrowserWindow, context isolation e shell Electron.
    - Demonstra: empacotamento desktop de aplicação local.

12. Agentanalistyfiscal — automação de domínio
    - Repositório: `celsonaemen/Agentanalistyfiscal`
    - Arquivos: `app/`, `conhecimento/`, `requirements.txt`, `tests/`
    - Evidência: componentes Python e documentação de automação fiscal assistida por IA.
    - Demonstra: exploração aplicada de AI Engineering, sem prova de produção.

13. generatordash — validação
    - Repositório: `celsonaemen/generatordash`
    - Arquivos: `app.py`, `tests/`, `run_tests.py`, `verify_dry_run.py`
    - Evidência: Streamlit e scripts de teste/validação.
    - Demonstra: protótipo/aplicação Python com preocupação de verificação.

14. controlpointid — Supabase
    - Repositório: `celsonaemen/controlpointid`
    - Arquivos: `supabase/`, `package.json`, `app/`
    - Evidência: integração e configuração Supabase em aplicação web.
    - Demonstra: uso específico de plataforma backend.

15. dinamica.contabilidade — Next/Tailwind
    - Repositório: `celsonaemen/dinamica.contabilidade`
    - Arquivos: `next.config.ts`, `tailwind.config.ts`, `src/`, `package.json`
    - Evidência: aplicação web TypeScript com Next/Tailwind.
    - Demonstra: supporting stack de frontend.

16. verificadoripost — Vite
    - Repositório: `celsonaemen/verificadoripost`
    - Arquivo: `vite.config.js`, `src/`, `package.json`
    - Evidência: build e aplicação web em Vite.
    - Demonstra: uso direto de ferramenta de frontend.

17. chromeextension — extensão
    - Repositório: `celsonaemen/chromeextension`
    - Arquivo: `manifest.json`, `popup.js`, `popup.html`
    - Evidência: manifest e popup executável.
    - Demonstra: browser extension tooling.

18. app-mensagem-local — servidor local
    - Repositório: `celsonaemen/app-mensagem-local`
    - Arquivo: `server.js`
    - Evidência: servidor JavaScript local e interface pública.
    - Demonstra: aplicação local/web experimental.

19. exit-point-app- — Android
    - Repositório: `celsonaemen/exit-point-app-`
    - Arquivos: `build.gradle.kts`, `app/`, `gradlew`
    - Evidência: estrutura Android/Kotlin com Gradle.
    - Demonstra: experiência experimental/isolada em mobile.

20. skills repositories — agent tooling
    - Repositórios: `superpowers`, `skills-engineer`, `skills-claudio`, `andrej-karpathy-skills`
    - Arquivos: `.agents`, `.claude-plugin`, `AGENTS.md`, `CLAUDE.md`, `skills/`
    - Evidência: frameworks de skills, instruções e plugins para assistentes de código.
    - Demonstra: tooling e experimentação, não experiência de produção com LLM.

## 11. Decisão final para o README

A narrativa mais defensável é:

- Core: Python, TypeScript, JavaScript; Next.js, React, NestJS, Prisma; PostgreSQL; Airflow/pandas/SQLAlchemy; auth/JWT/RBAC/sessões/auditoria; Windows low-level específico com C#/ACPI/EC/MMIO/MSR/IOCTL/PawnIO; IPED/Jump Lists como contribuição forense.
- Supporting: Flask, Electron, SQLite, Supabase, Tailwind, Vite, Gmail/OAuth, npm/pnpm, Gradle/Maven, GitHub Actions, HTML/CSS.
- Experimental / interests: agentic systems, AI coding skills, automação assistida por IA, LLM tooling, RAG, Kotlin/Android, Streamlit.
- Exclude: cloud genérica, Redis, MongoDB, Kafka/RabbitMQ, Kubernetes/Terraform, AWS/Azure/GCP, S3/Stripe/GraphQL, métricas, senioridade, escala e produção sem evidência.

## Resultado da revisão

- Tecnologias classificadas como CORE: 17
- Tecnologias classificadas como SUPPORTING: 15
- Tecnologias classificadas como EXPERIMENTAL: 2
- Tecnologias classificadas como INTEREST: 0 dentro dos 38 itens normalizados
- Tecnologias classificadas como EXCLUDE: 4 dentro dos 38 itens normalizados

Os itens de interesse que não entraram na matriz dos 38 — RAG, vector search, LLM tooling, agentic systems, Kotlin/Android, Streamlit e PowerShell — foram tratados explicitamente nas seções Experimental / Current Interests e Exclusions para evitar dupla contagem.

Esta revisão altera somente este arquivo de auditoria. O README.md do perfil e os demais repositórios não foram alterados.
