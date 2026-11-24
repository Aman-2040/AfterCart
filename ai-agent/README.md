# AI Agent

Python + FastAPI service for intent understanding, task planning, structured extraction and Playwright browser automation.

MVP workflow:
1. Receive a task from Spring Boot.
2. Classify intent and produce a structured plan.
3. Select an allowed tool.
4. Use Playwright against the controlled demo store.
5. Return structured execution status and evidence to Spring Boot.

The backend must validate authorization before consequential actions. Do not automate payment, OTP or CAPTCHA.
