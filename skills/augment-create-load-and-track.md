---
name: Create a load and post tracking updates
description: Upsert a freight load with its route stops on the Augment API, then post tracking events against it.
api: openapi/augment-openapi-original.json
operations:
  - verifyApiKey
  - createOrUpdateLoad
  - getLoad
  - addTrackingEvent
---

# Create a load and post tracking updates

Use the Augment API to create/update a freight load and keep it updated with tracking events.

## Auth
- Base URL: `https://api.prod.goaugment.com`
- HTTP Basic auth: send an **empty username** and your **API key as the password** (equivalent to base64 of `:<API_KEY>`).
- Optionally confirm the key first with `verifyApiKey` (`POST /v2/auth-check`).

## Steps
1. **Verify the key (optional).** Call `verifyApiKey`. On failure the `AuthCheckError` body includes a `requestId` and `timestamp` for support.
2. **Create or update the load.** Call `createOrUpdateLoad` (`POST /v2/loads`). This is an upsert keyed on your external/group references (e.g. `groupExternalId`), so replaying the same load is safe. Include the route stops.
3. **Read it back (optional).** Call `getLoad` (`GET /v2/loads`) to confirm the stored state.
4. **Post tracking.** Call `addTrackingEvent` (`POST /v2/loads/tracking`) as the shipment progresses.

## Rules
- Rate limit: 10 requests/second (600/minute) per customer. Back off on `5xx`/network errors with capped exponential backoff + jitter; do **not** retry `4xx`.
- Errors return `application/json` with an `ApiErrorBody` (`message`, `errorCode`, `details`). See `errors/augment-problem-types.yml`.
- There is no `Idempotency-Key` header; rely on the upsert keys for safe replays. See `conventions/augment-conventions.yml`.
