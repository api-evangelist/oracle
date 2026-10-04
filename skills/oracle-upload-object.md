---
name: oracle-upload-object
description: Upload an object to a bucket in Oracle Object Storage.
api: openapi/oracle-object-storage-api-openapi.yml
operations:
- GetNamespace
- ListBuckets
- CreateBucket
- PutObject
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/oracle-object-storage-api-openapi.yml ; every operationId checked against the contract
---

# oracle-upload-object

Upload an object to a bucket in Oracle Object Storage.

## Steps

1. 1. `GetNamespace` – requires `Authorization` header (ApiKey).
2. 2. `ListBuckets` – requires `Authorization` header and query parameter `namespaceName`.
3. 3. `CreateBucket` – requires `Authorization` header, body fields `namespaceName`, `name` (bucket name).
4. 4. `PutObject` – requires `Authorization` header, path parameters `namespaceName`, `bucketName`, `objectName`, and request body with the object data.

## Rules

- Auth: Include an `Authorization` header with the ApiKey.
- Idempotency: `CreateBucket` and `PutObject` are not idempotent; repeat calls may create duplicate resources.
- Pagination: `ListBuckets` supports pagination via standard `limit` and `page` query parameters (if provided).
- Errors: API returns standard HTTP error codes; on rate‑limit exhaustion there is no specific limit response.
