---
name: oracle-compute-create-capacity-reservation
description: Create a new compute capacity reservation and verify its creation.
api: openapi/oracle-compute-api-openapi.yml
operations:
- CreateComputeCapacityReservation
- GetComputeCapacityReservation
- ListComputeCapacityReservations
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/oracle-compute-api-openapi.yml ; every operationId checked against the contract
---

# oracle-compute-create-capacity-reservation

Create a new compute capacity reservation and verify its creation.

## Steps

1. 1. Call `CreateComputeCapacityReservation` with the required request body fields as defined in the contract.
2. 2. Call `GetComputeCapacityReservation` using the `capacityReservationId` returned from step 1 to retrieve the reservation details.
3. 3. Call `ListComputeCapacityReservations` to list all reservations and confirm the new reservation appears.

## Rules

- Auth: Include an `Authorization` header with the API key as defined by the ApiKey scheme.
- Idempotency: POST operations (`CreateComputeCapacityReservation`) should be safe to retry; include an `Idempotency-Key` header if supported by the service.
