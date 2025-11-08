# ⚙️ Microservices Architecture

Microservices split an application into small, independently deployable services that communicate over APIs to enable scalability and independent release cycles.

---

## ▶ Overview
- Service-per-business-capability
- Decentralized data management (database-per-service)
- Communication: synchronous (HTTP/gRPC) and asynchronous (messaging/event-driven)

---

## ▶ Key Patterns
- API Gateway, Service Discovery, Circuit Breaker, Saga (distributed transactions), Bulkhead, CQRS, Event Sourcing

---

## ▶ Design Considerations
- Decompose by bounded context, design for observability (tracing/metrics/logs), use CI/CD per service, automated testing, and contract versioning.

---

## 🧠 Exam Tips
- Use microservices for independent scaling and deployments; prefer event-driven patterns to reduce coupling.
- Combine API Gateway + Token-based auth + rate limiting for external access.

---

## 📚 Reference
- [Microservices Architecture](https://learn.microsoft.com/azure/architecture/microservices/)
