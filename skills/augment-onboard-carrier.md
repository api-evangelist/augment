---
name: Onboard and manage carriers
description: Create, look up, bulk-upsert, and archive carriers on the Augment API.
api: openapi/augment-openapi-original.json
operations:
  - createOrUpdateCarrier
  - bulkUpsertCarriers
  - getCarrierByIdentifier
  - getCarrierById
  - archiveCarrier
---

# Onboard and manage carriers

Manage the carrier roster that Augment assigns to loads.

## Auth
- Base URL: `https://api.prod.goaugment.com`
- HTTP Basic auth: empty username + API key as password.

## Steps
1. **Create or update a single carrier.** Call `createOrUpdateCarrier` (`POST /v1/carriers`). Upsert keyed on your TMS identifier, so replays are safe.
2. **Bulk import.** For onboarding many carriers at once, call `bulkUpsertCarriers` (`POST /v1/carriers/bulk`).
3. **Look up.** Use `getCarrierByIdentifier` (`GET /v1/carriers`) to find a carrier by your identifier, or `getCarrierById` (`GET /v1/carriers/{carrierId}`) by Augment's id.
4. **Archive.** Call `archiveCarrier` (`DELETE /v1/carriers/{carrierId}`) to soft-delete a carrier that should no longer be assigned.

## Rules
- Carrier Management is on the `/v1` path (loads and webhooks are on `/v2`). See `lifecycle/augment-lifecycle.yml`.
- Rate limit: 10 rps / 600 rpm per customer; retry only `5xx`/network with backoff.
- Errors: `ApiErrorBody` JSON envelope — see `errors/augment-problem-types.yml`.
