# Architecture documentation

We will add and maintain these documents as the system evolves:

- `system-context.md` — actors and system boundary
- `container-architecture.md` — frontend, gateway, services and infrastructure
- `order-lifecycle.md` — order, payment and inventory event flow
- `architecture-decisions/` — decisions and trade-offs (ADRs)

Architecture principle: each microservice owns its data and exposes capabilities
through explicit APIs or events. Services must not directly read or write another
service's database.
