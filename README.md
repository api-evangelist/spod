# SPOD (spod)

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
