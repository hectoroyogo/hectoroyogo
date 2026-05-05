<div align="center">

```
██████╗  █████╗  ██████╗██╗  ██╗███████╗███╗   ██╗██████╗
██╔══██╗██╔══██╗██╔════╝██║ ██╔╝██╔════╝████╗  ██║██╔══██╗
██████╔╝███████║██║     █████╔╝ █████╗  ██╔██╗ ██║██║  ██║
██╔══██╗██╔══██║██║     ██╔═██╗ ██╔══╝  ██║╚██╗██║██║  ██║
██████╔╝██║  ██║╚██████╗██║  ██╗███████╗██║ ╚████║██████╔╝
╚═════╝ ╚═╝  ╚═╝ ╚═════╝╚═╝  ╚═╝╚══════╝╚═╝  ╚═══╝╚═════╝
```

**Backend Developer · Systems & Data Focus**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_PROFILE)
[![Email](https://img.shields.io/badge/Email-333333?style=flat-square&logo=gmail&logoColor=white)](mailto:your@email.com)

</div>

---

## About

IT/DAM student building toward backend and systems engineering. My work centers on relational databases, data persistence layers, and application architecture — the parts of software that handle real complexity under the surface.

Currently focused on Java-based backend systems, SQL Server database design, and understanding how software components communicate with data at scale. Interested in clean architecture, audit-grade data integrity, and writing systems that are correct before they are clever.

---

## Tech Stack

<div align="center">

[![Tech Stack](https://skillicons.dev/icons?i=java,linux,git,github,idea&theme=dark)](https://skillicons.dev)

</div>

<br>

| Layer | Tools & Technologies |
|---|---|
| **Language** | Java 21 |
| **Database** | SQL Server · JDBC |
| **Query & Schema** | T-SQL · Triggers · Stored Procedures |
| **Version Control** | Git · GitHub |
| **Environment** | Linux · Bash |
| **Tooling** | IntelliJ IDEA |

---

## Current Focus

- Relational database design and advanced SQL query patterns
- Audit logging and data integrity enforcement via SQL Server triggers
- Layered backend architecture — DAO, service, and presentation separation
- JDBC internals: connection management, prepared statements, transaction control
- Linux fundamentals and command-line workflows for development environments
- Application architecture decisions and their long-term trade-offs

---

## Featured Project

### [`inventory-management-system`](https://github.com/YOUR_USERNAME/inventory-management-system)

> A complete inventory management backend built with Java 21, JDBC, and SQL Server.

Built to go beyond basic CRUD — this system handles real business logic including movement tracking, access control, and a full audit trail at the database level.

**Architecture**

```
src/
├── dao/          # Data access layer — all DB interaction isolated here
├── service/      # Business logic, validation, transaction coordination
├── model/        # Domain entities: Product, Movement, User, Role
├── util/         # DB connection pool, config loader
└── main/         # Entry point and console interface
```

**Key features**

- Stock management with product categorization and real-time movement history
- Role-based access control — admin and operator permission tiers
- Full audit trail implemented with SQL Server `AFTER INSERT/UPDATE/DELETE` triggers
- Parameterized queries throughout — no raw string concatenation
- Advanced reporting: stock levels, movement logs, anomaly flags via correlated subqueries

```
Stack  →  Java 21 · SQL Server · JDBC · T-SQL · Triggers
Pattern →  DAO / Service / Domain Model
```

---

## Contact

| | |
|---|---|
| **GitHub** | [@YOUR_USERNAME](https://github.com/YOUR_USERNAME) |
| **LinkedIn** | [linkedin.com/in/YOUR_PROFILE](https://linkedin.com/in/YOUR_PROFILE) |
| **Email** | your@email.com |

---

<div align="right">

*Always building.*

</div>
