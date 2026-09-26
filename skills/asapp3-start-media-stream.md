---
name: asapp3-start-media-stream
description: Start a media stream, retrieve the Twilio media stream URL, and then stop the stream.
api: openapi/asapp3-openapi.yaml
operations:
- startStreaming
- getTwilioMediaStreams
- stopStreaming
generated: '2026-09-26'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/asapp3-openapi.yaml ; every operationId checked against the contract
---

# asapp3-start-media-stream

Start a media stream, retrieve the Twilio media stream URL, and then stop the stream.

## Steps

1. 1. `startStreaming` – send a POST request with headers `asapp-api-id` and `asapp-api-secret`.
2. 2. `getTwilioMediaStreams` – send a GET request with headers `asapp-api-id` and `asapp-api-secret` to obtain the Twilio media stream URL.
3. 3. `stopStreaming` – send a POST request with headers `asapp-api-id` and `asapp-api-secret` to end the stream.

## Rules

- Include `asapp-api-id` and `asapp-api-secret` headers for authentication on every request.
- Rate limit is 100 requests per second; exceeding this returns HTTP 429.
- Use one of the provided servers (https://api.sandbox.asapp.com or https://api.test.asapp.com) as the base URL.
