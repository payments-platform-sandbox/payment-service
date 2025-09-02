# Payment Service (`payment-service`)

> Public Payments API handling **payment requests, refunds, and cancellations** with **idempotency** and **workflow orchestration**.  


## 1) Overview
This service is the **entrypoint for clients**. It provides REST APIs for initiating and managing payments.  
Requests are validated, made idempotent, checked against compliance policies, and delegated to the orchestration engine.  

**Responsibilities**
- Expose REST endpoints for payments  
- Handle **idempotency** with Redis  
- Forward requests to Orkes workflows  
- Enforce policies via OPA decisions  


## 2) Functional Requirements
- **FR1 (Workflow Execution):** Starts payment workflows via Orkes  
- **FR2 (Webhook Handling):** Provides callback endpoints for async updates  
- **FR4 (Refunds & Cancellations):** Supports refund/cancel endpoints, OPA-gated  


## 3) API Endpoints
- `POST /payments` → create a payment  
- `POST /payments/{id}/refunds` → refund a payment  
- `POST /payments/{id}/cancel` → cancel a payment  

(OpenAPI specs live in [`contracts`](../contracts/openapi/payment-service.yaml))  


## 4) Tech Stack
- Java 17 + Spring Boot  
- Maven build  
- Redis for idempotency  
- Orkes Conductor for workflow execution  
- OPA for compliance decisions  


## 5) Metrics
- Exposes `/actuator/prometheus` for Prometheus scrapes  
- Metrics: request rate, latency, error %, idempotency conflicts  


## 6) License
MIT
