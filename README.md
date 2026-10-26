# SPOD (spod)

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

SPOD (Spreadshirt Print-On-Demand), now branded **Spreadconnect**, is the print-on-demand and dropshipping fulfillment service from Spreadshirt (sprd.net AG). Its REST API - base `https://rest.spod.com` - lets any shop system create customizable articles from designs, place and manage orders, choose shipping types and track shipments, browse a catalog of 250+ product types, check stock, and subscribe to webhook notifications for article, order, and shipment events. SPOD prints and ships from US and EU facilities, typically producing 95% of orders within 48 hours.

**Access model:** The API is public and free to use with a per-account **API access token** generated in the SPOD/Spreadconnect web application and sent in the `X-SPOD-ACCESS-TOKEN` header on every request. There is **no subscription, setup, or monthly platform fee** - sellers are invoiced only per fulfilled order (base product price + print cost + shipping + tax), and that invoice is independent of the retail price the seller charges their own customers. This is an honest, verify-before-production reference: the endpoint list is grounded in SPOD's published OpenAPI (`github.com/SP0D/rest-api`) and developer docs (`rest.spod.com/docs`), while request/response schemas should be confirmed against the live documentation. A staging environment is available at `https://rest.spreadconnect-staging.app`.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/spod/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/spod/refs/heads/main/apis.yml)

## Tags

- Print on Demand
- POD
- Dropshipping
- Fulfillment
- E-commerce
- Merchandise
- Spreadshirt
- Spreadconnect

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### SPOD Articles API

Create, list, retrieve, and delete customizable articles - the sellable products built by placing a design onto a product type and view. Each article carries its variants (SKUs), print configurations, and point-of-sale metadata.

- **Human URL:** [https://rest.spod.com/docs/](https://rest.spod.com/docs/)
- **Base URL:** `https://rest.spod.com`

#### Tags

- Articles
- Products
- Designs

#### Properties

- [Documentation](https://rest.spod.com/docs/)
- [API Reference](https://rest.spod.com/docs/)
- [OpenAPI](openapi/spod-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/spod.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/spod.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SPOD Orders API

Place and manage print-on-demand orders. Create an order (simple single-request flow or a controlled create/update/confirm flow), retrieve or update order details, confirm an order for production, and attempt cancellation while it is still cancelable.

- **Human URL:** [https://rest.spod.com/docs/](https://rest.spod.com/docs/)
- **Base URL:** `https://rest.spod.com`

#### Tags

- Orders
- Fulfillment
- Checkout

#### Properties

- [Documentation](https://rest.spod.com/docs/)
- [API Reference](https://rest.spod.com/docs/)
- [OpenAPI](openapi/spod-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/spod.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/spod.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SPOD Shipping API

List the available shipping types for an order with their prices and delivery estimates, set the preferred shipping type on an order, and retrieve shipment records with tracking information once an order is dispatched from a US or EU facility.

- **Human URL:** [https://rest.spod.com/docs/](https://rest.spod.com/docs/)
- **Base URL:** `https://rest.spod.com`

#### Tags

- Shipping
- Shipments
- Tracking

#### Properties

- [Documentation](https://rest.spod.com/docs/)
- [API Reference](https://rest.spod.com/docs/)
- [OpenAPI](openapi/spod-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/spod.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/spod.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SPOD Product Types API

Browse the SPOD catalog of 250+ product types (article types) - blank products such as T-shirts, hoodies, and accessories. Retrieve a product type's sizes, colors, views, printable areas, and the configuration needed to build an article.

- **Human URL:** [https://rest.spod.com/docs/](https://rest.spod.com/docs/)
- **Base URL:** `https://rest.spod.com`

#### Tags

- Product Types
- Article Types
- Catalog

#### Properties

- [Documentation](https://rest.spod.com/docs/)
- [API Reference](https://rest.spod.com/docs/)
- [OpenAPI](openapi/spod-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/spod.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/spod.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SPOD Stock API

Check inventory availability across product variants. Retrieve stock for all variants or for a specific SKU so you can surface availability in your shop before an article is ordered.

- **Human URL:** [https://rest.spod.com/docs/](https://rest.spod.com/docs/)
- **Base URL:** `https://rest.spod.com`

#### Tags

- Stock
- Inventory
- Availability

#### Properties

- [Documentation](https://rest.spod.com/docs/)
- [API Reference](https://rest.spod.com/docs/)
- [OpenAPI](openapi/spod-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/spod.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/spod.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SPOD Subscriptions and Webhooks API

Register webhook subscriptions to be notified via POST about Article, Order, and Shipment state changes. List and delete subscriptions, verify authenticity with the `X-SPRD-SIGNATURE` SHA256 HMAC header, and use simulate endpoints to trigger test events. Notifications follow an at-least-once delivery model and must be acknowledged with a 202 status, a response within 8 seconds, and the payload `[accepted]`.

- **Human URL:** [https://rest.spod.com/docs/](https://rest.spod.com/docs/)
- **Base URL:** `https://rest.spod.com`

#### Tags

- Subscriptions
- Webhooks
- Events

#### Properties

- [Documentation](https://rest.spod.com/docs/)
- [API Reference](https://rest.spod.com/docs/)
- [OpenAPI](openapi/spod-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/spod.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/spod.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/SP0D)
- [LinkedIn](https://www.linkedin.com/company/spod-spreadshirt-print-on-demand)
- [Website](https://www.spod.com)
- [Documentation](https://rest.spod.com/docs/)
- [Plans](plans/spod-plans-pricing.yml)
- [Rate Limits](rate-limits/spod-rate-limits.yml)
- [Fin Ops](finops/spod-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
