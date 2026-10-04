---
name: oracle-manage-application-vip
description: Create, retrieve, and delete an application virtual IP (VIP) address on a cloud VM cluster.
api: openapi/oracle-database-api-openapi.yml
operations:
- CreateApplicationVip
- GetApplicationVip
- DeleteApplicationVip
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/oracle-database-api-openapi.yml ; every operationId checked against the contract
---

# oracle-manage-application-vip

Create, retrieve, and delete an application virtual IP (VIP) address on a cloud VM cluster.

## Steps

1. 1. `CreateApplicationVip` – provide the required request body fields for the new VIP.
2. 2. `GetApplicationVip` – supply the `applicationVipId` returned from the create step to retrieve the VIP details.
3. 3. `DeleteApplicationVip` – supply the same `applicationVipId` to remove the VIP.

## Rules

- Auth: Include an API key in the `Authorization` header as defined by the ApiKey scheme.
- Idempotency: The `CreateApplicationVip` operation is not idempotent; repeat calls will create additional VIPs.
