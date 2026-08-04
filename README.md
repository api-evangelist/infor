# Infor (infor)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Infor provides industry-specific cloud ERP platforms including CloudSuite Industrial (M3), CloudSuite Financials, and Infor LN. The Infor ION API Gateway enables OAuth 2.0-based integration across Infor applications and third-party systems. SDKs are available via the infor-cloud GitHub organization for Java, .NET, Go, and HTML5 development.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/infor/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/infor/refs/heads/main/apis.yml)

## Tags

- ERP
- Manufacturing
- Supply Chain
- Cloud
- Integration

## Timestamps

- **Modified:** 2026-04-28

## APIs

### Infor ION API Gateway

The Infor ION API Gateway provides a managed OAuth 2.0 API layer for integrating Infor CloudSuite applications with third-party systems. The gateway supports Authorization Code, Client Credentials, and SAML Bearer grant types with SDKs available for Java, .NET, and Go.

- **Human URL:** [https://www.infor.com/products/ion](https://www.infor.com/products/ion)
- **Base URL:** `https://mingledev01-ionapi.mingle.infor.com`

#### Tags

- Cloud
- ERP
- Integration
- Middleware
- OAuth2

#### Properties

- [Documentation](https://www.infor.com/products/ion)
- [S D Ks](https://github.com/infor-cloud/ion-api-sdk)
- [Getting Started](https://github.com/infor-cloud/ion-api-sdk)
- [Authentication](https://github.com/infor-cloud/ion-api-sdk)
- [OpenAPI](openapi/infor-ion-api-gateway-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/infor-ion-api-gateway.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/infor-ion-api-gateway.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](asyncapi/infor-ion-events-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)

### Infor M3 / LN CloudSuite Industrial API

The Infor M3 (CloudSuite Industrial) APIs provide access to production orders, inventory management, supply chain planning, and financial data for discrete and process manufacturing enterprises. The M3 H5 SDK enables HTML5-based application development on the M3 platform.

- **Human URL:** [https://www.infor.com/](https://www.infor.com/)
- **Base URL:** `https://api.infor.com`

#### Tags

- Cloud
- ERP
- M3
- Manufacturing
- Supply Chain

#### Properties

- [Documentation](https://www.infor.com/)
- [S D Ks](https://github.com/infor-cloud/m3-h5-sdk)
- [Postman Collection](collections/infor-ion-api-gateway.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/infor-ion-api-gateway.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Infor XtendM3 API

Infor XtendM3 provides a Java SDK for extending and customizing Infor M3 (CloudSuite Industrial) business logic without modifying core code. Extensions are deployed and executed within the M3 runtime environment.

- **Human URL:** [https://www.infor.com/](https://www.infor.com/)
- **Base URL:** `https://api.infor.com`

#### Tags

- ERP
- Extension
- Java
- M3
- Manufacturing

#### Properties

- [Documentation](https://www.infor.com/)
- [S D Ks](https://github.com/infor-cloud/xtendm3-sdk-java)
- [Getting Started](https://github.com/infor-cloud/xtendm3-extension-examples)
- [Postman Collection](collections/infor-ion-api-gateway.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/infor-ion-api-gateway.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Infor CloudSuite Financials API

Infor CloudSuite Financials APIs provide integration with general ledger, accounts payable, accounts receivable, cash management, and financial reporting for enterprise finance operations.

- **Human URL:** [https://www.infor.com/](https://www.infor.com/)
- **Base URL:** `https://api.infor.com`

#### Tags

- Accounting
- Cloud
- ERP
- Financials

#### Properties

- [Documentation](https://www.infor.com/)
- [Postman Collection](collections/infor-ion-api-gateway.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/infor-ion-api-gateway.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/infor)
