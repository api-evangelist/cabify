# Cabify

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

Cabify is a Spanish multi-mobility company founded in 2011 and headquartered in Madrid, operating ride-hailing, corporate mobility, and last-mile logistics across Spain and Latin America (6+ countries and 40+ cities). Its public developer platform exposes two authenticated REST APIs: a Ride-Hailing API (v4) for price estimation, journey booking, real-time state tracking, rider and label management, and sales reporting; and a Logistics API (v1) for creating, shipping, tracking, and configuring proof of delivery for parcels, including ecommerce integrations with Shopify, Tiendanube, and VTEX. Both APIs authenticate with OAuth2 client-credentials access tokens (Bearer), publish independent sandbox environments, and deliver asynchronous updates via webhooks.

**Areas:** Company · Transportation · Ride Hailing · Mobility · Logistics · Delivery · Last Mile Delivery · Webhook · Authentication

## Cabify on APIs.io

Everything profiled for Cabify is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/cabify/](https://apis.io/providers/cabify/)** — or go straight to one of the APIs or properties below.

### APIs (13)

- [Cabify Delivery API](https://apis.io/apis/cabify/cabify-delivery-api/) — Operations for managing the delivery lifecycle. Use these endpoints to trigger a shipment, cancel an active delivery, or check whether a pickup location…
- [Cabify Estimates API](https://apis.io/apis/cabify/cabify-estimates-api/) — This method returns prices, Id's and all the information for products that are available at the origin point. Before requesting a journey as a first step it…
- [Cabify Hubs API](https://apis.io/apis/cabify/cabify-hubs-api/) — A hub is a physical location (such as a warehouse or store) where parcels are stored until they are ready to be picked up by a driver. You can reference a…
- [Cabify Journeys API](https://apis.io/apis/cabify/cabify-journeys-api/) — This section covers the mobility solution for all companies looking to transport their employees in a simple, safe and comfortable way. We offer different…
- [Cabify Label API](https://apis.io/apis/cabify/cabify-label-api/) — The label API from Cabify — 1 operation(s) for label.
- [Cabify Labels API](https://apis.io/apis/cabify/cabify-labels-api/) — Cabify offers to its clients a feature where the client’s employees have to input a journey motive or a project or a dynamic cost center associated with the…
- [Cabify Parcels API](https://apis.io/apis/cabify/cabify-parcels-api/) — A parcel is the package you need to ship. Each parcel is identified by a unique ID and contains a pickup point (where the driver collects the package) and a…
- [Cabify Sales API](https://apis.io/apis/cabify/cabify-sales-api/) — Sales objects are created once a journey transitions into the terminated state and they are associated with the user who requested the journey (which not…
- [Cabify Shipment API](https://apis.io/apis/cabify/cabify-shipment-api/) — The shipment API from Cabify — 2 operation(s) for shipment.
- [Cabify Shipping Types API](https://apis.io/apis/cabify/cabify-shipping-types-api/) — The shipping_types API from Cabify — 1 operation(s) for shipping_types.
- [Cabify Status API](https://apis.io/apis/cabify/cabify-status-api/) — Track the real-time status and location of your parcels at any point during their delivery.
- [Cabify Users API](https://apis.io/apis/cabify/cabify-users-api/) — The users API from Cabify — 4 operation(s) for users.
- [Cabify Webhooks API](https://apis.io/apis/cabify/cabify-webhooks-api/) — Subscribe to event-driven notifications to receive live updates about parcel status changes, location updates, and proof of delivery codes.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Cabify Webhooks](https://apis.io/asyncapis/cabify/cabify-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [cabify](https://apis.io/servers/cabify/cabify/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Cabify Agentic Access](https://apis.io/agentic-access/cabify/cabify-agentic-access/)

#### Collections (13)

Postman and Open Collection request collections.

- [Cabify Logistics delivery API](https://apis.io/collections/cabify/open-cabify-delivery-api/)
- [Cabify Logistics delivery Estimates API](https://apis.io/collections/cabify/open-cabify-estimates-api/)
- [Cabify Logistics delivery hubs API](https://apis.io/collections/cabify/open-cabify-hubs-api/)
- [Cabify Logistics delivery Journeys API](https://apis.io/collections/cabify/open-cabify-journeys-api/)
- [Cabify Logistics delivery label API](https://apis.io/collections/cabify/open-cabify-label-api/)
- [Cabify Logistics delivery Labels API](https://apis.io/collections/cabify/open-cabify-labels-api/)
- [Cabify Logistics delivery parcels API](https://apis.io/collections/cabify/open-cabify-parcels-api/)
- [Cabify Logistics delivery Sales API](https://apis.io/collections/cabify/open-cabify-sales-api/)
- [Cabify Logistics delivery shipment API](https://apis.io/collections/cabify/open-cabify-shipment-api/)
- [Cabify Logistics delivery shipping_types API](https://apis.io/collections/cabify/open-cabify-shipping-types-api/)
- [Cabify Logistics delivery status API](https://apis.io/collections/cabify/open-cabify-status-api/)
- [Cabify Logistics delivery users API](https://apis.io/collections/cabify/open-cabify-users-api/)
- [Cabify Logistics delivery webhooks API](https://apis.io/collections/cabify/open-cabify-webhooks-api/)

#### Overlays (2)

OpenAPI overlays, including conversational phrasing for each operation.

- [Cabify Logistics Overlay](https://apis.io/overlays/cabify/cabify-logistics-overlay/)
- [Cabify Ride Hailing Overlay](https://apis.io/overlays/cabify/cabify-ride-hailing-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Cabify Authentication](https://apis.io/security/cabify/cabify-authentication/)
- [Cabify Domain Security](https://apis.io/security/cabify/cabify-domain-security/)
- [Cabify Vulnerability Disclosure](https://apis.io/security/cabify/cabify-vulnerability-disclosure/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://cabify.com)
- [Documentation](https://developers.cabify.com/docs/getting-started)
- [Getting started](https://developers.cabify.com/docs/quickstart)
- [API reference](https://developers.cabify.com/reference/createjourney)
- [Sign up](https://cabify.com/app)
- [Support](https://developers.cabify.com/page/cabify-api-support)
- [Blog](https://cabify.com/es/empresas/blog)
- [Security](https://cabify.com/.well-known/security.txt)
- [Terms of service](https://cabify.com/en/legal)
- [Privacy policy](https://cabify.com/en/legal/privacy)
- [GitHub](https://github.com/cabify)
- [Status](https://cabify.statuspage.io)

## API Evangelist rating

**Kin Score 53.9** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 59.1 |
| Contract governance | 4.5 |
| Operational transparency | 52.6 |
| Developer ergonomics | 66.1 |
| Access clarity | 34.2 |

**Agent readiness 36.9** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | verified |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | — |
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
| Pagination Ratio | partial |
| Operation Distinctiveness | distinct |

**Regulatory alignment 30.4** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/cabify/](https://apis.io/providers/cabify/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Cabify: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/cabify/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
