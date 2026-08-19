# Quarantined scaffold — not published by Oracle

The OpenAPI documents in this directory were **written by API Evangelist**, modelled from
Oracle's public OCI Compute documentation. Oracle never published them. They must not be
presented as Oracle artifacts, cited as evidence of what Oracle ships, or credited in a
Kin Score.

They were moved here on **2026-08-04**.

## What superseded them

Oracle publishes a first-party contract for **every** OCI service, indexed at:

> https://docs.oracle.com/en-us/iaas/api/specs/index.json

161 Swagger 2.0 documents covering 7,918 operations across 158 services are now
harvested into `openapi/`, stamped `method: harvested` / `first_party: true` with the
source URL on each one. The six documents here described 15 operations of one
service, modelled rather than served.

The index was reachable the whole time. It is served by the same documentation SPA whose
HTML shell returns 200 for any path — which is why probing pages found nothing and reading
the app bundle found everything. When a portal renders client-side, the spec list is in
its JavaScript, not in its markup.
