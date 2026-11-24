# API Contracts (initial planning)

Agree request/response schemas before parallel implementation.

## Suggested Spring Boot endpoints
- `POST /api/products/search`
- `GET /api/products/{id}/listings`
- `POST /api/products/compare`
- `GET /api/payment-methods`
- `POST /api/payment-methods`
- `POST /api/deals/calculate`
- `GET /api/orders`
- `GET /api/orders/{id}`
- `POST /api/agent/tasks`
- `GET /api/agent/tasks/{id}`
- `POST /api/agent/tasks/{id}/approve`
- `POST /api/agent/tasks/{id}/cancel`

## Internal AI service
- `POST /agent/execute`

The backend must validate task ownership, allowed actions and approval state. Finalize exact schemas with the team before implementation.
