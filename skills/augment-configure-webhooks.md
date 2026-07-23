---
name: Configure webhook endpoints and subscriptions
description: Register an HTTPS webhook endpoint on the Augment API, subscribe it to event types, and send a test delivery.
api: openapi/augment-openapi-original.json
operations:
  - createWebhookEndpoint
  - listWebhookEndpoints
  - listWebhookEventTypes
  - createWebhookSubscription
  - testWebhookSubscription
---

# Configure webhook endpoints and subscriptions

Set up Augment to push events (tracking, stop updates, carrier issues, load drafts, bids) to your system.

## Auth
- Base URL: `https://api.prod.goaugment.com`
- HTTP Basic auth: empty username + API key as password.

## Steps
1. **Register the destination.** Call `createWebhookEndpoint` (`POST /v2/webhook-endpoints`) with your HTTPS URL. Use `listWebhookEndpoints` (`GET /v2/webhook-endpoints`) to review existing ones.
2. **Discover event types.** Call `listWebhookEventTypes` (`GET /v2/webhook-event-types`). Available types include `TRACKING_UPDATE`, `STOP_UPDATE`, `LOAD_CARRIER_UPDATE`, `SEND_TMS_COMMENT`, `SCHEDULED_CARRIER_OUTREACH`, `UPLOAD_FILES`, `PUSH_BID_TO_TMS`, `PUSH_LOAD_DRAFT`, and `CARRIER_ISSUE_UPDATED`.
3. **Subscribe.** Call `createWebhookSubscription` (`POST /v2/webhook-subscriptions`) binding the endpoint to the event types you need.
4. **Test.** Call `testWebhookSubscription` (`POST /v2/webhook-subscriptions/{subscriptionId}/test`) to send a sample delivery and confirm your receiver.

## Rules
- Prefer webhook **v2** (shared envelope). v1 flat payloads are legacy — see `asyncapi/augment-webhooks.yml`.
- Endpoints must be HTTPS. Public signature-verification details are not documented; validate deliveries defensively.
- Errors: `ApiErrorBody` JSON envelope — see `errors/augment-problem-types.yml`.
