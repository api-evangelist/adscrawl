---
name: adscrawl-create-and-launch-cloud-browser
description: Create a cloud browser profile and immediately launch it.
api: openapi/adscrawl-openapi.yaml
operations:
- createCloudBrowser
- launchCloudBrowser
generated: '2026-10-02'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/adscrawl-openapi.yaml ; every operationId checked against the contract
---

# adscrawl-create-and-launch-cloud-browser

Create a cloud browser profile and immediately launch it.

## Steps

1. 1. Use `createCloudBrowser` with the request body fields required to define the profile (no specific fields listed in the documentation).
2. 2. Use `launchCloudBrowser` with the request body fields required to start the browser (no specific fields listed in the documentation).

## Rules

- Auth: include the API key in the `x-api-key` header.
- Pagination: the `listCloudBrowsers` operation supports pagination (details not provided).
