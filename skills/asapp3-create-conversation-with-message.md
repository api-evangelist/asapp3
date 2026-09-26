---
name: asapp3-create-conversation-with-message
description: Create a new conversation and add an initial message to it.
api: openapi/asapp3-openapi.yaml
operations:
- createOrUpdateConversation
- createMessage
generated: '2026-09-26'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/asapp3-openapi.yaml ; every operationId checked against the contract
---

# asapp3-create-conversation-with-message

Create a new conversation and add an initial message to it.

## Steps

1. 1. Call `createOrUpdateConversation` with the required conversation fields in the request body.
2. 2. Call `createMessage` with the `conversationId` returned from step 1 and the message fields in the request body.

## Rules

- Include both authentication headers: `asapp-api-id` (API-ID) and `asapp-api-secret` (API-Secret).
- Rate limit is 100 requests per second; exceeding returns HTTP 429.
