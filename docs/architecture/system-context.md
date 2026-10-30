# System context

Customers use the Next.js storefront. Requests reach backend capabilities through
an API Gateway (to be implemented). Spring Boot services own business capabilities.

PostgreSQL stores durable relational data, Redis supports low-latency ephemeral data
and caching, and Kafka transports asynchronous domain events. REST is the public
HTTP API style; gRPC is reserved for selected internal synchronous calls.
