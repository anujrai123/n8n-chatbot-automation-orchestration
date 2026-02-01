<p align="center">
  <img src="docs/logo.png" alt="Project Logo" width="160"/>
</p>

<h1 align="center">Chatbot-Driven Automation using n8n</h1>

<p align="center">
  Reliable workflow orchestration with retries, polling, and notifications
</p>




# Chatbot-Driven Automation using n8n

This repository demonstrates how **n8n can be used as an orchestration layer**
to handle chatbot-driven automation in a production-style environment.

The focus of this project is **workflow reliability, error handling, and clear
communication**, not just task automation.

---

## 🧠 Problem Statement

In many teams, backend jobs are triggered and monitored manually.
Engineers and operators repeatedly:

- Check system health
- Trigger jobs by hand
- Poll for status updates
- Retry failed executions
- Inform stakeholders manually

This leads to:
- Wasted engineering time
- Delayed responses
- Higher operational cost
- Increased risk of human error

---

## ✅ Solution Overview

This project replaces manual coordination with **automated orchestration**.

A chatbot submits requests to **n8n**, which then:

1. Accepts the request and returns a tracking ID
2. Validates backend system health
3. Triggers job execution asynchronously
4. Handles retries when the system is busy
5. Polls job status with safety limits
6. Sends clear notifications for success, timeout, or escalation

n8n acts as the **orchestration layer**, while execution remains external.

---

## 🏗 High-Level Architecture


---



[ Chatbot ]
     |
     v
[ n8n Webhook ]
     |
     v
[ Orchestration Logic ]
(Health Checks, Retries, Polling)
     |
     v
[ Backend APIs ]
(Execution & Status)




---

## 🔁 Workflow Highlights

- **Immediate request acknowledgement** (non-blocking)
- **Explicit execution context** (request_id, retry_count, poll_count)
- **System busy handling with retries**
- **Asynchronous polling for long-running jobs**
- **Polling limits to prevent infinite execution**
- **Human-friendly email notifications**

This mirrors real-world automation patterns used in production systems.

---


---

## 🔐 Security & Credentials

All credentials, OAuth tokens, and secrets have been **intentionally removed**
before publishing.

Email and external integrations are included only to demonstrate
**orchestration and escalation patterns**.

In real deployments, credentials are managed securely per environment.

---

## 🧪 Backend Implementation

The actual backend service (Flask) is not included.

This repository focuses on **automation and orchestration design**.
A mock API contract is provided to explain how the n8n workflow interacts
with backend systems in a real deployment.

---

## 🎯 Why This Project Matters

This workflow reduces:
- Manual monitoring effort
- Mean time to resolution (MTTR)
- Operational overhead

And improves:
- Reliability
- Scalability
- Clarity for non-technical users

It demonstrates how automation can save **time, cost, and engineering effort**
while improving system reliability.

---

## 👤 Author

**Anuj Rai**  
Automation Engineer | Workflow Orchestration | Observability  


