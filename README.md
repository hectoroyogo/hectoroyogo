<div align="center">

# Hector Oyogo

**Backend Developer in Training** · Java · SQL Server · Systems Architecture

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/hectoroyogo)
[![GitHub](https://img.shields.io/badge/GitHub-hectoroyogo-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/hectoroyogo)

</div>

---

<div align="center">

IT/DAM student focused on backend systems and data engineering.  
I build around the persistence layer — relational databases, application architecture,  
and the data flows that hold a system together.

My main work right now is a full-stack inventory system built from scratch in Java:  
multi-layer architecture, role-based access, audit logging via SQL triggers,  
and a lightweight HTTP interface alongside the core console app.  
Docker handles local infrastructure.

**Not chasing breadth. Building depth where it matters at this stage.**

</div>

---

## Stack

<div align="center">

[![Stack](https://skillicons.dev/icons?i=java,maven,docker,git,linux,idea&theme=dark)](https://skillicons.dev)

<br><br>

<table>
  <tr>
    <th></th>
    <th>Technologies</th>
  </tr>
  <tr>
    <td><strong>Language</strong></td>
    <td>Java 17</td>
  </tr>
  <tr>
    <td><strong>Data</strong></td>
    <td>SQL Server · T-SQL · JDBC · Triggers · Stored Procedures</td>
  </tr>
  <tr>
    <td><strong>Build & Dependencies</strong></td>
    <td>Maven</td>
  </tr>
  <tr>
    <td><strong>Infrastructure</strong></td>
    <td>Docker · Docker Compose</td>
  </tr>
  <tr>
    <td><strong>Version Control</strong></td>
    <td>Git · GitHub</td>
  </tr>
  <tr>
    <td><strong>Environment</strong></td>
    <td>Linux · Bash</td>
  </tr>
  <tr>
    <td><strong>Tooling</strong></td>
    <td>IntelliJ IDEA</td>
  </tr>
</table>

<br>

<strong>Currently learning</strong>

<br><br>

<table>
  <tr>
    <th></th>
    <th>Technologies</th>
  </tr>
  <tr>
    <td><strong>Framework</strong></td>
    <td>Spring Boot · Spring MVC</td>
  </tr>
  <tr>
    <td><strong>API Design</strong></td>
    <td>REST · HTTP semantics · JSON contracts</td>
  </tr>
  <tr>
    <td><strong>Database</strong></td>
    <td>PostgreSQL · Prisma</td>
  </tr>
  <tr>
    <td><strong>Testing</strong></td>
    <td>JUnit 5 · basic integration testing</td>
  </tr>
</table>

</div>

---

## Currently Focused On

<div align="center">

<table>
  <tr>
    <td>Transitioning from raw JDBC to Spring Boot</td>
  </tr>
  <tr>
    <td>REST API design: resource modeling, status codes, error handling conventions</td>
  </tr>
  <tr>
    <td>Docker multi-container setups: separating application and database services cleanly</td>
  </tr>
  <tr>
    <td>Layered architecture patterns and their trade-offs at junior scale</td>
  </tr>
  <tr>
    <td>SQL fluency: subqueries, window functions, execution plans, index basics</td>
  </tr>
</table>

</div>

---

## Projects

### [`inventario-logistica-jdbc`](https://github.com/hectoroyogo/inventario-logistica-jdbc)

<div align="center">

**Inventory management system — Java 17 · JDBC · SQL Server · Docker · Maven**

</div>

The main project. Started as a JDBC exercise and grew into a complete backend system with a web interface.

**What it actually does:**

- Console interface and a separate lightweight HTTP server serving a frontend — same service and DAO layer, no logic duplication
- Role-based access: admin and employee menus with different permission scopes
- Password storage with SHA-256 hashing — not plaintext
- Full audit trail via SQL Server `AFTER INSERT/UPDATE/DELETE` triggers on the `auditoria_productos` table
- Database initialization on startup: detects if the DB exists, offers to preserve or recreate it with seed data
- SQL Server runs in Docker — no local installation needed

```text
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
