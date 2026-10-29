# Augment

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Augment (Augie) is an AI productivity platform for the freight and logistics industry, automating complex supply-chain workflows for brokerages, carriers, and distributors — quoting, booking, load building, capacity sourcing, track & trace, carrier support, and order-to-cash — while integrating with existing TMS, ERP, email, and messaging systems. Its public REST API (api.prod.goaugment.com) lets partner systems manage loads and route stops, upsert and archive carriers, post tracking events, report carrier issues, and configure webhook endpoints and event subscriptions across nine event types. Authentication is HTTP Basic with an API key; the company is SOC 2 Type II certified. Augment is backed by 8VC, Lightspeed Venture Partners, and Redpoint Ventures.

**Areas:** Company · Logistics · Freight · Supply Chain · Transportation · Webhook · Artificial Intelligence · Automation

## Augment on APIs.io

Everything profiled for Augment is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/augment/](https://apis.io/providers/augment/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [Augment API Key API](https://apis.io/apis/augment/augment-api-key-api/) — API key based authorization. Please refer to the [authorization documentation](docs/authorization.md) for details.
- [Augment Carrier Management API](https://apis.io/apis/augment/augment-carrier-management-api/) — API endpoints for managing carriers, carrier contacts, and carrier-manager relationships.
- [Augment Carrier Support API](https://apis.io/apis/augment/augment-carrier-support-api/) — Public API endpoints for correlating carrier issues (detention, lumper, TONU, etc.) with the matching incidents in your TMS. Access is gated by brokerage;…
- [Augment Load Management API](https://apis.io/apis/augment/augment-load-management-api/) — API endpoints for creating, updating, and retrieving loads.
- [Augment Webhook Endpoints API](https://apis.io/apis/augment/augment-webhook-endpoints-api/) — Public API endpoints for approved brokerages to create, update, list, and delete webhook endpoints. Self-service endpoints send version 2 webhook payloads…
- [Augment Webhook Event Subscriptions API](https://apis.io/apis/augment/augment-webhook-event-subscriptions-api/) — Public API endpoints for approved brokerages to list supported webhook event types, subscribe endpoints to event types, and send test deliveries.…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Augment Webhooks](https://apis.io/asyncapis/augment/augment-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [augment](https://apis.io/servers/augment/augment/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Augment Agentic Access](https://apis.io/agentic-access/augment/augment-agentic-access/)

#### Collections (6)

Postman and Open Collection request collections.

- [Augment API Key API](https://apis.io/collections/augment/open-augment-api-key-api/)
- [Augment API Key Carrier Management API](https://apis.io/collections/augment/open-augment-carrier-management-api/)
- [Augment API Key Carrier Support API](https://apis.io/collections/augment/open-augment-carrier-support-api/)
- [Augment API Key Load Management API](https://apis.io/collections/augment/open-augment-load-management-api/)
- [Augment API Key Webhook Endpoints API](https://apis.io/collections/augment/open-augment-webhook-endpoints-api/)
- [Augment API Key Webhook Event Subscriptions API](https://apis.io/collections/augment/open-augment-webhook-event-subscriptions-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Augment Openapi Overlay](https://apis.io/overlays/augment/augment-openapi-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Augment Authentication](https://apis.io/security/augment/augment-authentication/)
- [Augment Domain Security](https://apis.io/security/augment/augment-domain-security/)
- [Augment Trust Center](https://apis.io/security/augment/augment-trust-center/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Augment Plans Pricing](https://apis.io/plans/augment/augment-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Augment Rate Limits](https://apis.io/rate-limits/augment/augment-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://goaugment.com)
- [Documentation](https://apidocs.goaugment.com/)
- [Getting started](https://apidocs.goaugment.com/guide/start-developing/authorization/)
- [API reference](https://apidocs.goaugment.com/reference)
- [Pricing](https://www.goaugment.com/pricing)
- [Sign up](https://www.goaugment.com/get-a-demo)
- [Blog](https://www.goaugment.com/blog)
- [Compliance](https://trust.goaugment.com/)
- [Terms of service](https://www.goaugment.com/terms-of-use)
- [Privacy policy](https://www.goaugment.com/privacy)
- [GitHub](https://github.com/goaugment)

## API Evangelist rating

**Kin Score 59.1** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 61.3 |
| Contract governance | 18.2 |
| Operational transparency | 31.6 |
| Developer ergonomics | 54.2 |
| Access clarity | 60.5 |

**Agent readiness 35.9** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 27.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/augment/](https://apis.io/providers/augment/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Augment: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/augment/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
