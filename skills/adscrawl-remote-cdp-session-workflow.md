---
name: adscrawl-remote-cdp-session-workflow
description: Create a temporary CDP session, retrieve its discovery data, issue a live‑control token, and finally terminate the session.
api: openapi/adscrawl-openapi.yaml
operations:
- createCdpSession
- getCdpDiscovery
- createLiveControlToken
- deleteCdpSession
generated: '2026-10-02'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/adscrawl-openapi.yaml ; every operationId checked against the contract
---

# adscrawl-remote-cdp-session-workflow

Create a temporary CDP session, retrieve its discovery data, issue a live‑control token, and finally terminate the session.

## Steps

1. 1. Call `createCdpSession` – requires header `x-api-key` with your API key.
2. 2. Call `getCdpDiscovery` – requires header `x-api-key` and path parameter `sessionId` returned from step 1.
3. 3. Call `createLiveControlToken` – requires header `x-api-key` and body containing the `sessionId` from step 1.
4. 4. Call `deleteCdpSession` – requires header `x-api-key` and path parameter `sessionId` from step 1.

## Rules

- Auth: Include the `x-api-key` header for all requests (ApiKey scheme).
- Idempotency: `createCdpSession` and `createLiveControlToken` are not idempotent; avoid retrying without a new session.
- Errors: The API returns standard HTTP error codes (e.g., 400 for bad request, 401 for unauthorized, 404 for unknown session).
