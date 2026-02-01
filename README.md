# n8n-chatbot-automation-orchestration
Chatbot-driven automation using n8n as an orchestration layer. This project demonstrates production-style workflows with health checks, async execution, retries, polling limits, and user-friendly notifications. Designed to reduce manual operations, improve reliability, and save engineering time while keeping execution decoupled from orchestration.


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

