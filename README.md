<div align="center">

# Hector Oyogo

**Backend Developer in Training** · Java · SQL Server · Systems Architecture

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/hectoroyogo)
[![GitHub](https://img.shields.io/badge/GitHub-hectoroyogo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/hectoroyogo)

</div>

---

IT/DAM student focused on backend systems and data engineering. I build around the persistence layer — relational databases, application architecture, and the data flows that hold a system together.

My main work right now is a full-stack inventory system built from scratch in Java: multi-layer architecture, role-based access, audit logging via SQL triggers, and a lightweight HTTP interface alongside the core console app. Docker handles local infrastructure.

Not chasing breadth. Building depth where it matters at this stage.

---

## Stack

<div align="center">

[![Stack](https://skillicons.dev/icons?i=java,maven,docker,git,linux,idea&theme=dark)](https://skillicons.dev)

</div>

<br>

| | Technologies |
|---|---|
| **Language** | Java 17 |
| **Data** | SQL Server · T-SQL · JDBC · Triggers · Stored Procedures |
| **Build & Dependencies** | Maven |
| **Infrastructure** | Docker · Docker Compose |
| **Version Control** | Git · GitHub |
| **Environment** | Linux · Bash |
| **Tooling** | IntelliJ IDEA |

**Currently learning**

| | Technologies |
|---|---|
| **Framework** | Spring Boot · Spring MVC |
| **API Design** | REST · HTTP semantics · JSON contracts |
| **Database** | PostgreSQL · Prisma (schema-first modeling) |
| **Testing** | JUnit 5 · basic integration testing |

---

## Currently Focused On

- Transitioning from raw JDBC to Spring Boot — understanding what the framework abstracts and why
- REST API design: resource modeling, status codes, error handling conventions
- Docker multi-container setups: separating application and database services cleanly
- Layered architecture patterns and their trade-offs at junior scale
- SQL fluency: subqueries, window functions, execution plans, index basics

---

## Projects

### [`inventario-logistica-jdbc`](https://github.com/hectoroyogo/inventario-logistica-jdbc)
> Inventory management system — Java 17 · JDBC · SQL Server · Docker · Maven

The main project. Started as a JDBC exercise and grew into a complete backend system with a web interface.

**What it actually does:**

- Console interface and a separate lightweight HTTP server serving a frontend — same service and DAO layer, no logic duplication
- Role-based access: admin and employee menus with different permission scopes
- Password storage with SHA-256 hashing — not plaintext
- Full audit trail via SQL Server `AFTER INSERT/UPDATE/DELETE` triggers on the `auditoria_productos` table
- Database initialization on startup: detects if the DB exists, offers to preserve or recreate it with seed data
- SQL Server runs in Docker — no local installation needed

```
src/main/java/
  app/       →  startup, mode selection (console / web)
  config/    →  JDBC connection, environment-aware config resolution
  model/     →  domain entities
  dao/       →  all database interaction
  service/   →  business logic, transaction coordination
  ui/        →  console menus
  web/       →  HTTP server, session management, REST-like API
  util/      →  shared validators
sql/
  init.sql   →  schema + seed data
```

```
Stack  →  Java 17 · SQL Server · JDBC · T-SQL · Maven · Docker
Pattern →  DAO / Service / Domain Model
```

---

### [`gestor-personal`](https://github.com/hectoroyogo/gestor-personal)
> Personal management system — TypeScript · Next.js · PostgreSQL · Prisma · Docker

A separate exploration outside Java. Monorepo with pnpm workspaces, a Next.js web app, Prisma-managed migrations, Docker Compose infrastructure, and a React Native mobile client.

Primary value here was learning: monorepo structure, Docker Compose service orchestration, Prisma schema-first database modeling, and TypeScript across the stack. Work in progress.

```
apps/web      →  Next.js with integrated backend
apps/mobile   →  Expo + React Native
packages/db   →  Prisma + PostgreSQL
infra/        →  Docker Compose for dev and production
```

---

## Roadmap

Where I'm heading over the next few months:

- [ ] Rebuild the inventory system's API layer in Spring Boot
- [ ] Add JUnit integration tests covering the service layer
- [ ] Deploy a containerized Java + PostgreSQL app with Docker Compose
- [ ] Implement proper REST conventions: pagination, error responses, validation
- [ ] First contact with GitHub Actions for basic CI on a Java project

---

## GitHub Stats

<div align="center">

<img height="180em" src="https://github-readme-stats.vercel.app/api?username=hectoroyogo&show_icons=true&theme=transparent&hide_border=true"/>

<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=hectoroyogo&layout=compact&theme=transparent&hide_border=true"/>

</div>

---

## Contact

| | |
|---|---|
| **GitHub** | [@hectoroyogo](https://github.com/hectoroyogo) |
| **LinkedIn** | [linkedin.com/in/hectoroyogo](https://linkedin.com/in/hectoroyogo) |

---

<div align="right">
<sub>Spain · IT/DAM · Open to junior backend opportunities</sub>
</div>
