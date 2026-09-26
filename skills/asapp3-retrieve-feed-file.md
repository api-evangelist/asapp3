---
name: asapp3-retrieve-feed-file
description: Retrieve a specific feed file from the File Exporter service.
api: openapi/asapp3-openapi.yaml
operations:
- listFeeds
- listFeedVersions
- listFeedFormats
- listFeedDates
- listFeedIntervals
- listFeedFiles
- listFeedFile
generated: '2026-09-26'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/asapp3-openapi.yaml ; every operationId checked against the contract
---

# asapp3-retrieve-feed-file

Retrieve a specific feed file from the File Exporter service.

## Steps

1. 1. Call `listFeeds` – no request fields are documented; include authentication headers `asapp-api-id` and `asapp-api-secret`.
2. 2. Call `listFeedVersions` – no request fields are documented; include authentication headers.
3. 3. Call `listFeedFormats` – no request fields are documented; include authentication headers.
4. 4. Call `listFeedDates` – no request fields are documented; include authentication headers.
5. 5. Call `listFeedIntervals` – no request fields are documented; include authentication headers.
6. 6. Call `listFeedFiles` – no request fields are documented; include authentication headers.
7. 7. Call `listFeedFile` – no request fields are documented; include authentication headers.

## Rules

- Authentication: provide `asapp-api-id` and `asapp-api-secret` headers.
- Rate limiting: 100 requests per second; HTTP 429 returned on exhaustion.
