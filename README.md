# AfterCart — Your Personal AI Shopping Agent

**Shop smarter. Save more. Let AI handle the rest.**

AfterCart is a browser-based AI shopping agent concept for helping users compare products, optimize eligible payment offers, and manage post-purchase tasks.

## Problem
Online shopping is fragmented across product discovery, retailer comparisons, bank-offer conditions, order tracking and return workflows. The lowest listed price may not be the lowest payable price after offer eligibility, discount caps, coupons and delivery fees.

## Proposed solution
AfterCart brings these tasks into one conversational experience:
- **Discover:** Search products using natural language.
- **Compare:** Compare equivalent product variants across supported retailer listings.
- **Optimize:** Validate eligible offers and calculate the payable price.
- **Resolve:** Retrieve orders, inspect return policies, check eligibility and prepare return requests.

Consequential actions require user approval.

## Hackathon MVP scope
The initial prototype is intentionally limited to:
1. A curated product catalog with multiple sample retailer listings.
2. Personalized payment preferences and deterministic offer calculations.
3. A conversational interface and comparison dashboard.
4. A controlled demo store operated through Playwright.
5. A return-assistance workflow: order lookup → policy check → eligibility → form autofill → approval → submission verification.

**Scope and data transparency:** Sample prices and offers must be labelled as demo/curated data with source and timestamp. Do not claim a refund has been issued when only a request has been submitted.

## Architecture
```text
React + Vite
     |
     v
Java + Spring Boot ------ PostgreSQL
     |
     v
Python + FastAPI + LLM
     |
     v
Playwright
     |
     v
Controlled Demo Store
```

Spring Boot is the source of truth for application data, task state and approval checks. The Python service handles AI orchestration and browser execution.

## Technology stack
- Frontend: React, Vite, Tailwind CSS
- Backend: Java, Spring Boot
- Database: PostgreSQL
- AI orchestration: Python, FastAPI, LLM
- Browser automation: Playwright
- Optional: AWS S3 for invoice/document storage

## Repository structure
```text
frontend/       React application
backend/        Spring Boot REST API and business logic
ai-agent/       FastAPI, LLM orchestration and Playwright
demo-store/     Controlled shopping website for browser workflows
docs/           Architecture, API contracts and database notes
screenshots/    Prototype screenshots for documentation
```

## Safety boundaries
- Never store full card numbers, CVV, PINs or banking credentials.
- Do not automate payments, OTPs or CAPTCHA.
- Require explicit user approval before submitting returns or other consequential actions.
- Respect retailer website terms and access restrictions.
- Clearly distinguish form-filled, request-submitted, request-accepted and refund-issued states.

## Local development
Each service will have its own setup instructions in its folder README. Add environment variables to local `.env` files; never commit secrets.

## Team ZeroTouch
- Neel Upadhyaya
- Aman Singh Banafar
- Dhruv Sharma

Ramaiah Institute of Technology  
wHACKiest 2026 — Track 2: Beyond the Browser

## Project status
This repository is the shared project scaffold. Update this section as features become implemented and tested. Do not mark planned features as complete.
