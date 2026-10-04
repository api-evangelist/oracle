---
name: oracle-data-integration-create-and-start-workspace
description: Create a new Data Integration workspace and start it.
api: openapi/oracle-data-integration-api-openapi.yml
operations:
- CreateWorkspace
- StartWorkspace
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/oracle-data-integration-api-openapi.yml ; every operationId checked against the contract
---

# oracle-data-integration-create-and-start-workspace

Create a new Data Integration workspace and start it.

## Steps

1. 1. Call `CreateWorkspace` with the required request body (JSON) and include the `Authorization` header as defined by the ApiKey scheme.
2. 2. Call `StartWorkspace` with path parameter `workspaceId` returned from the previous step and include the `Authorization` header.

## Rules

- Auth: Provide an API key in the `Authorization` header (ApiKey scheme).
- Idempotency: Not applicable; the operations are not defined as idempotent.
