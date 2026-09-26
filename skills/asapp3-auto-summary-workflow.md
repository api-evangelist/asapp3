---
name: asapp3-auto-summary-workflow
description: Retrieve a free‑text summary, get the conversation intent, fetch the stored summary and optionally submit feedback for a given conversation.
api: openapi/asapp3-openapi.yaml
operations:
- retrieveFreeTextSummary
- getIntent
- getFreeTextSummary
- createFeedbackEvent
generated: '2026-09-26'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/asapp3-openapi.yaml ; every operationId checked against the contract
---

# asapp3-auto-summary-workflow

Retrieve a free‑text summary, get the conversation intent, fetch the stored summary and optionally submit feedback for a given conversation.

## Steps

1. 1. Call `retrieveFreeTextSummary` with the required request body and header `asapp-api-id` / `asapp-api-secret` to generate a free‑text summary for a conversation.
2. 2. Call `getIntent` with path parameter `conversationId` and headers `asapp-api-id` / `asapp-api-secret` to obtain the inferred intent.
3. 3. Call `getFreeTextSummary` with path parameter `conversationId` and headers `asapp-api-id` / `asapp-api-secret` to fetch the stored free‑text summary.
4. 4. (Optional) Call `createFeedbackEvent` with path parameter `conversationId`, request body containing feedback, and headers `asapp-api-id` / `asapp-api-secret` to submit user feedback.

## Rules

- Include both `asapp-api-id` and `asapp-api-secret` headers for authentication on every request.
- Rate limit is 100 requests per second; exceeding returns HTTP 429.
