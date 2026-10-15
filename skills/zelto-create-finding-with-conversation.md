---
name: zelto-create-finding-with-conversation
description: Create a new finding and attach a conversation to it.
api: openapi/zelto-openapi.json
operations:
- createFinding
- addConversationToFinding
- listFindingConversations
generated: '2026-10-15'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/zelto-openapi.json ; every operationId checked against the contract
---

# zelto-create-finding-with-conversation

Create a new finding and attach a conversation to it.

## Steps

1. 1. Call `createFinding` with the JSON body describing the finding (requires `Authorization: Bearer <token>` header).
2. 2. Call `addConversationToFinding` with the finding ID returned from step 1 and a JSON body describing the conversation (requires `Authorization: Bearer <token>` header).
3. 3. Optionally call `listFindingConversations` with the finding ID to verify the conversation was attached (requires `Authorization: Bearer <token>` header).

## Rules

- Include an `Authorization: Bearer <token>` header for all requests (bearerAuth).
- All POST requests must include a `Content-Type: application/json` header.
- Responses may include standard HTTP error codes: 400 for bad request, 401 for unauthorized, 404 for not found, and 500 for server errors.
