---
name: oracle-create-and-retrieve-api
description: Create a new API in Oracle API Gateway and then retrieve its details.
api: openapi/oracle-apigateway-api-openapi.yml
operations:
- CreateApi
- GetApi
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/oracle-apigateway-api-openapi.yml ; every operationId checked against the contract
---

# oracle-create-and-retrieve-api

Create a new API in Oracle API Gateway and then retrieve its details.

## Steps

1. 1. Call `CreateApi` with the required request body fields for the new API and include the `Authorization` header (ApiKey).
2. 2. Call `GetApi` using the `apiId` returned from `CreateApi` and include the `Authorization` header (ApiKey).

## Rules

- Authentication: Provide an API key in the `Authorization` header as defined by the ApiKey scheme.
- Idempotency: Not applicable for these operations.
