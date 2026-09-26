---
name: asapp3-compose-message
description: Generate AutoCompose suggestions, correct spelling, and evaluate profanity for a conversation.
api: openapi/asapp3-openapi.yaml
operations:
- getSuggestions
- getSpellingCorrection
- getEvaluation
generated: '2026-09-26'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/asapp3-openapi.yaml ; every operationId checked against the contract
---

# asapp3-compose-message

Generate AutoCompose suggestions, correct spelling, and evaluate profanity for a conversation.

## Steps

1. 1. Call `getSuggestions` with path parameter `conversationId` and request body as defined in the contract.
2. 2. Call `getSpellingCorrection` with request body containing the text to correct.
3. 3. Call `getEvaluation` with request body containing the text to evaluate for profanity.

## Rules

- Include authentication headers `asapp-api-id` (API-ID) and `asapp-api-secret` (API-Secret) on every request.
- Rate limit is 100 requests per second; exceeding returns HTTP 429.
