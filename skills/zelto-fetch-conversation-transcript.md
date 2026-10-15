---
name: zelto-fetch-conversation-transcript
description: Retrieve a conversation transcript by first listing conversations and then fetching the transcript of a selected conversation.
api: openapi/zelto-openapi.json
operations:
- listConversations
- getConversation
- getTranscript
generated: '2026-10-15'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/zelto-openapi.json ; every operationId checked against the contract
---

# zelto-fetch-conversation-transcript

Retrieve a conversation transcript by first listing conversations and then fetching the transcript of a selected conversation.

## Steps

1. 1. Call `listConversations` – no request body; supports pagination via query parameters `page` and `pageSize`.
2. 2. Call `getConversation` – requires path parameter `id` of the desired conversation.
3. 3. Call `getTranscript` – requires path parameter `id` of the conversation to obtain its transcript.

## Rules

- All requests must include an `Authorization: Bearer <token>` header (bearerAuth).
- `listConversations` supports pagination; use `page` and `pageSize` query parameters to navigate results.
- Responses may include standard HTTP error codes: 401 for unauthorized, 404 for not found, and 5xx for server errors.
