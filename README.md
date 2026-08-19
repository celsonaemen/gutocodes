🎯 Who Am I

Fullstack Engineer com Application Security embutida no DNA.

Não construo apenas features — construo sistemas pensando em como eles podem falhar, onde estão os gargalos e como torná-los mais resilientes. Minha abordagem une engenharia de software com segurança ofensiva: se eu não consigo quebrar, provavelmente construí bem.

· 7+ anos construindo aplicações web, APIs e sistemas distribuídos
· Application Security como disciplina central desde o design
· Fullstack com ênfase em arquitetura, performance e observabilidade
· Automação como ferramenta para eliminar repetição e focar no que importa

---___________------------______________---------

⚡ Impact Metrics

Área Realizações
Performance Redução de 42% no tempo de carregamento de páginas em aplicações Next.js
Arquitetura Migração de monólito para microsserviços, reduzindo 63% no tempo de deploy
Segurança Identificação e correção de 17 vulnerabilidades em produção antes de qualquer exploração
Banco de Dados Otimização de queries que reduziu 55% no tempo de resposta de APIs
Automação Pipeline CI/CD que reduziu 70% do tempo de release manual

---___________------------______________---------

🛠️ Tech Stack

Frontend

```
TypeScript · React · Next.js · TanStack Query · Tailwind · Framer Motion
```

Backend

```
TypeScript · NestJS · Node.js · Fastify · GraphQL · WebSockets
```

Database & Storage

```
PostgreSQL · Prisma · Supabase · Redis · AWS S3
```

Security (Core)

```
OWASP Top 10 · JWT · OAuth2 · RBAC · API Security · Penetration Testing
```

DevOps & Cloud

```
Docker · Kubernetes · AWS · Vercel · GitHub Actions · Terraform
```

---

🚀 Featured Work

ControlPointID — Fullstack Application

Sistema de gerenciamento de identidade com foco em controle de acesso e segurança de dados.

Stack: Next.js · TypeScript · Supabase · PostgreSQL · Prisma · Vercel

Desafio: Construir uma aplicação com autenticação robusta, RBAC granular e dados sensíveis protegidos.

Resultados:

· ✅ 99.9% uptime desde o lançamento
· ✅ 0 vulnerabilidades reportadas em 3 meses de uso
· ✅ 300ms de tempo médio de resposta
· ✅ Deploy contínuo com rollback automático


---

Realtime Target Tracker — Computer Vision

Sistema de detecção e rastreamento de objetos em tempo real usando YOLOv5.

Stack: Python · YOLOv5 · OpenCV · WebRTC · FastAPI

Desafio: Processar vídeo em tempo real com latência < 100ms em hardware modesto.

Resultados:

· ✅ 45 FPS em GPUs consumer-grade
· ✅ Detecção com 87% de precisão média (mAP)
· ✅ Suporte a múltiplas fontes: webcam, vídeo, imagem


---

Security Labs — Research Environment

Ambiente controlado para estudo de vulnerabilidades web e APIs.

Foco:

· Authentication Bypass
· JWT Manipulation
· IDOR (Insecure Direct Object References)
· SQL/NoSQL Injection
· Business Logic Flaws
· Rate Limiting Bypass

Metodologia:

```
Reconnaissance → Attack Surface → Vulnerability Analysis → 
Controlled Exploitation → Impact Assessment → Root Cause → 
Mitigation → Secure Implementation
```

Diferencial: Cada vulnerabilidade é documentada com Proof of Concept e mitigação implementável, não apenas teoria.



---___________------------______________---------

🧠 Engineering Philosophy

```
┌──────────────────────────────────────────────────┐
│                                                  │
│   BUILD          →  Criar sistemas simples       │
│   BREAK          →  Testar limites               │
│   MEASURE        →  Validar com dados            │
│   SECURE         →  Segurança na arquitetura     │
│   AUTOMATE       →  Eliminar repetição           │
│                                                  │
└──────────────────────────────────────────────────┘
```

Princípios que guiam meu trabalho:

1. Simplicidade > Complexidade — Todo sistema complexo é frágil
2. Segurança nativa — Não é camada, é fundação
3. Observabilidade primeiro — Se não dá pra medir, não dá pra melhorar
4. Automação agressiva — Máquinas pra repetição, humanos pra decisão
5. Ceticismo saudável — "Funciona" não é resposta final

---

📊 Architectural Approach

```
                    ┌─────────────────────┐
                    │    Frontend Layer    │
                    │  Next.js / React     │
                    └──────────┬───────────┘
                               │
                    ┌──────────▼───────────┐
                    │     API Gateway       │
                    │  NestJS / Fastify     │
                    └──────────┬───────────┘
                               │
          ┌────────────────────┼────────────────────┐
          │                    │                    │
┌─────────▼─────────┐ ┌───────▼───────┐ ┌──────────▼──────────┐
│   Service Layer    │ │   Cache       │ │   Queue / Workers   │
│   Business Logic   │ │   Redis       │ │   Bull / RabbitMQ   │
└─────────┬─────────┘ └───────────────┘ └──────────┬──────────┘
          │                                        │
┌─────────▼─────────┐                     ┌─────────▼──────────┐
│  Data Layer        │                     │   External APIs    │
│  PostgreSQL        │                     │   Stripe / etc     │
└────────────────────┘                     └────────────────────┘

                    ┌─────────────────────────────────────┐
                    │       Security Layer (Cross-Cutting)│
                    │  Auth · RBAC · Validation · Audit  │
                    └─────────────────────────────────────┘
```

---___________------------______________---------

🔐 Security Research

Áreas de estudo contínuo:

· Web Application Security — OWASP Top 10, ataque e defesa
· API Security — GraphQL, REST, gRPC
· Authentication & Authorization — OAuth2, JWT, SAML, RBAC, ABAC
· Cryptography — TLS, hashing, encryption at rest/in transit
· Cloud Security — AWS, containers, Kubernetes
· Bug Bounty — Participação ativa em programas privados

Metodologia de pesquisa:

```
1. Reconnaissance    → Mapeamento do sistema
2. Attack Surface    → Identificação de pontos de entrada
3. Vulnerability     → Análise aprofundada
4. Exploitation      → Validação controlada
5. Impact            → Avaliação de risco real
6. Root Cause        → Entendimento da falha
7. Mitigation        → Correção aplicável
8. Implementation    → Prevenção futura
```

Resultados:

· 17 vulnerabilidades reportadas em programas de bug bounty (privados)
· 5 CVEs atribuídas (em processo)
· Colaboração em 3 projetos open source de segurança

---

📚 Currently Exploring

Security

· Web3 Security (Smart Contracts, DeFi)
· AI/ML Security (Adversarial ML, Prompt Injection)
· Cloud Native Security (Service Mesh, Zero Trust)

Engineering

· Distributed Systems (CAP Theorem, Consistency)
· Event-Driven Architecture (Kafka, Event Sourcing)
· Database Engineering (Internals, Query Optimization)

Research

· Post-Quantum Cryptography
· Supply Chain Security
· Threat Modeling Frameworks

---

💼 Professional Experience

Senior Fullstack Engineer | Remote

2022 - Present

· Liderança técnica em projetos com times de 5-8 engenheiros
· Arquitetura de microsserviços com NestJS e PostgreSQL
· Implementação de pipelines CI/CD com segurança integrada
· Mentoria de engenheiros juniores em práticas de segurança

Fullstack Developer | Remote

2019 - 2022

· Desenvolvimento de aplicações web com React/Next.js
· Construção de APIs RESTful com Node.js/Express
· Otimização de performance e banco de dados
· Primeiros passos em Application Security

Security Researcher | Independent

2020 - Present

· Estudo autodirigido de vulnerabilidades web
· Participação em programas de bug bounty
· Desenvolvimento de ferramentas de segurança
· Documentação pública de técnicas e descobertas

---

🤝 Open Source & Community

· Contribuições ativas em projetos como Next.js, Prisma e NestJS
· Mantenedor de 2 pacotes NPM para segurança
· Palestras em meetups locais sobre segurança de aplicações
· Mentoria em comunidades de desenvolvimento e segurança

---

📫 Let's Connect

· GitHub: @celsonaemen
· LinkedIn: Celso Naemen
· X: @celsonaemen
· Email: celso.naemen@proton.me

---

🎯 Looking For

Colaborações em:

· Projetos open source com foco em segurança
· Ferramentas de análise de vulnerabilidades
· Arquitetura de sistemas resilientes
· Pesquisa em segurança de aplicações
· Engenharia de dados e performance

Se envolve construir, quebrar ou melhorar sistemas — vamos conversar.

---

<div align="center">

"Segurança não é um recurso, é uma propriedade do sistema bem projetado."

</div>