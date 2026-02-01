# Backend Contract

This folder defines the **API contract** used by the n8n orchestration workflow.

The actual backend implementation is intentionally excluded.  
Only interface definitions, sample requests, and sample responses are provided.

This approach keeps the repository secure while clearly explaining how the
automation workflow interacts with backend systems in a real deployment.

---

## Purpose

The backend contract exists to:

- Describe the **expected behavior** of backend APIs
- Define request and response formats used by the n8n workflow
- Document possible execution states and error scenarios
- Allow reviewers to understand orchestration logic without exposing code

This folder focuses on **interfaces, not implementation**.

---

## Included Files

### `api_contract.md`
Defines all backend endpoints used by the workflow, including:
- Health check endpoint
- Job execution endpoint
- Job status polling endpoint
- Possible success, failure, and busy states

---

### `sample_requests.json`
Provides example request payloads sent by n8n to the backend, such as:
- Job execution requests with metadata
- Priority and requester information

---

### `sample_responses.json`
Provides example responses returned by the backend, including:
- System health responses
- Job execution acknowledgements
- Job status states (RUNNING, SUCCESS, TIMED_OUT)
- Error responses (SYSTEM_BUSY)

---

## Design Principles

- **Security First**  
  No credentials, secrets, or internal logic are included.

- **Clear Boundaries**  
  n8n handles orchestration and reliability; the backend handles execution.

- **Production-Oriented**  
  Contracts are designed to reflect real-world automation and operational needs.

---

## Notes

This contract is provided for **demonstration and documentation purposes only**.

In a real production environment:
- Backend services would be deployed separately
- Credentials would be managed securely per environment
- Contracts would be versioned and governed as part of the delivery process
