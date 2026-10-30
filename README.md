# E-Commerce Platform

A portfolio-grade e-commerce platform built with Next.js, Spring Boot microservices,
PostgreSQL, Redis, Apache Kafka, REST, gRPC, and Docker.

## Repository layout

- `ecommerce-frontend/` — Next.js + TypeScript customer application
- `ecommerce-backend/auth-service/` — first Spring Boot microservice
- `infrastructure/` — Docker Compose and local infrastructure (added in later steps)
- `docs/` — architecture, decisions, API and workflow documentation

## Prerequisites

- Git
- Node.js 22 or 24 LTS and npm
- Java 21 JDK
- Docker Desktop with Docker Compose
- PowerShell on Windows

Verify installations:

```powershell
git --version
node -v
npm -v
java -version
docker --version
docker compose version
```

## Start the frontend

```powershell
cd ecommerce-frontend
npm install
npm run dev
```

Open http://localhost:3000.

## Start the Auth Service

The Maven project is included. If Maven is installed:

```powershell
cd ecommerce-backend/auth-service
mvn spring-boot:run
```

Alternatively, generate a Maven Wrapper from the service directory:

```powershell
mvn wrapper:wrapper
.\mvnw.cmd spring-boot:run
```

The service listens on http://localhost:8080. The root URL may return 404 until an endpoint is added.

## Important

This is the initial starter scaffold. PostgreSQL, Redis, Kafka, API Gateway, additional
microservices, gRPC contracts, authentication flows, and Docker Compose orchestration
will be introduced and tested incrementally during the project roadmap.

Never commit real passwords, API keys, JWT secrets, or `.env` files.
