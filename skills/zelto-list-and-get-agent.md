---
name: zelto-list-and-get-agent
description: Retrieve a list of agents and then fetch details for a selected agent.
api: openapi/zelto-openapi.json
operations:
- listAgents
- getAgent
generated: '2026-10-15'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/zelto-openapi.json ; every operationId checked against the contract
---

# zelto-list-and-get-agent

Retrieve a list of agents and then fetch details for a selected agent.

## Steps

1. 1. Call `listAgents` – no request body; include the `Authorization: Bearer <token>` header; supports pagination via `page` and `pageSize` query parameters.
2. 2. Call `getAgent` – path parameter `id` (the agent identifier from the list); include the `Authorization: Bearer <token>` header.

## Rules

- Auth header: All requests require an `Authorization: Bearer <token>` header (bearerAuth).
- Pagination: `listAgents` supports `page` and `pageSize` query parameters for paginated results.
