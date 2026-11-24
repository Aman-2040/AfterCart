# Architecture

```text
User
 |
 v
React + Vite
 |
 v
Spring Boot REST API -------- PostgreSQL
 |
 v
FastAPI AI Orchestrator
 |
 v
LLM + Planner + Tool Selector
 |
 v
Playwright Browser
 |
 v
Controlled Demo Store
```

Spring Boot owns persistent application state, offer calculations, order state and approval enforcement. Python handles AI orchestration and browser interaction.

## Main workflows
### Deal optimization
User request → product search → variant matching → offer eligibility → deterministic calculation → ranked recommendation.

### Return assistance
Order lookup → policy extraction → eligibility check → form autofill → user approval → submit → verify status.
