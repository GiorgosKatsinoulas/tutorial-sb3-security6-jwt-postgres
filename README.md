# tutorial-sb3-security6-jwt-postgres
Spring Boot 3 + Spring Security 6 JWT auth with Postgres. Register/login, role-based access, refresh tokens, and example protected endpoints with Postman tests.

Secure REST API with **JWT authentication & authorization** using **Spring Boot 3**, **Spring Security 6**, and **PostgreSQL**.  
Includes registration, login, role-based access, access/refresh tokens, and example protected endpoints (with cURL + Postman).

---

## Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Quick Start](#quick-start)
  - [1) Database](#1-database)
  - [2) Configuration](#2-configuration)
  - [3) Run the App](#3-run-the-app)
- [API](#api)
  - [Auth Endpoints](#auth-endpoints)
  - [Protected Endpoints](#protected-endpoints)
  - [cURL Examples](#curl-examples)
- [Suggested Package Structure](#suggested-package-structure)
- [Security Overview](#security-overview)
- [Token Details](#token-details)
- [Next Steps](#next-steps)
- [License](#license)

---

## Features
- User **registration** and **login** (BCrypt password hashing)
- **Access** and **Refresh** JWTs (stateless server)
- **Role-based**/authority-based authorization (`ROLE_USER`, `ROLE_ADMIN`)
- Global exception handling for authentication/authorization errors
- Ready-to-import **Postman** collection (optional)
- Works with **PostgreSQL** (local or Docker)

---

## Tech Stack
- **Java 17+**, **Spring Boot 3.x**
- **Spring Security 6**
- **Spring Data JPA/Hibernate**
- **PostgreSQL**
- Build: **Maven** or **Gradle**

---

## Prerequisites
- Java 17+
- PostgreSQL (installed locally or via Docker)
- Maven or Gradle
- (Optional) Postman & `jq` for quick testing

---

## Quick Start

### 1) Database
Create a database and user (local Postgres):
```sql
CREATE DATABASE sb3_security_jwt;
CREATE USER sb_user WITH ENCRYPTED PASSWORD 'sb_pass';
GRANT ALL PRIVILEGES ON DATABASE sb3_security_jwt TO sb_user;

