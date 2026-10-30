# Infor

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

Infor provides industry-specific cloud ERP platforms including CloudSuite Industrial (M3), CloudSuite Financials, and Infor LN. The Infor ION API Gateway enables OAuth 2.0-based integration across Infor applications and third-party systems. SDKs are available via the infor-cloud GitHub organization for Java, .NET, Go, and HTML5 development.

**Areas:** ERP · Manufacturing · Supply Chain · Cloud · Integration

## Infor on APIs.io

Everything profiled for Infor is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/infor/](https://apis.io/providers/infor/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [Infor M3 / LN CloudSuite Industrial API](https://apis.io/apis/infor/infor-m3-api/) — The Infor M3 (CloudSuite Industrial) APIs provide access to production orders, inventory management, supply chain planning, and financial data for discrete…
- [Infor XtendM3 API](https://apis.io/apis/infor/infor-xtendm3-api/) — Infor XtendM3 provides a Java SDK for extending and customizing Infor M3 (CloudSuite Industrial) business logic without modifying core code. Extensions are…
- [Infor CloudSuite Financials API](https://apis.io/apis/infor/infor-cloudsuite-financials-api/) — Infor CloudSuite Financials APIs provide integration with general ledger, accounts payable, accounts receivable, cash management, and financial reporting…
- [Infor ION Documents API](https://apis.io/apis/infor/infor-ion-documents-api/) — ION document routing and processing
- [Infor M3 API](https://apis.io/apis/infor/infor-m3-api-api/) — Infor M3 business API programs
- [Infor Document Management (IDM) API](https://apis.io/apis/infor/infor-idm-api/) — The Infor Document Management REST API, published on the Infor Developer Portal at developer.infor.com/api and served through the ION API Gateway under the…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Infor ION Events](https://apis.io/asyncapis/infor/infor-ion-events-asyncapi/)

#### Event channels (5)

Individual events and webhooks the provider emits.

- [customer/deleted](https://apis.io/channels/infor/customer-deleted/)
- [customer/synced](https://apis.io/channels/infor/customer-synced/)
- [inventory/synced](https://apis.io/channels/infor/inventory-synced/)
- [invoice/synced](https://apis.io/channels/infor/invoice-synced/)
- [order/synced](https://apis.io/channels/infor/order-synced/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [infor-mcp.yml](https://apis.io/servers/infor/infor-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Infor Agentic Access](https://apis.io/agentic-access/infor/infor-agentic-access/)

#### JSON Schema (1)

The data models the API reads and writes.

- [Infor M3 Customer](https://apis.io/schemas/infor/infor-m3-customer/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Infor Context](https://apis.io/jsonld/infor/infor-context/)

#### Collections (3)

Postman and Open Collection request collections.

- [Infor ION API Gateway](https://apis.io/collections/infor/open-infor-ion-api-gateway/)
- [Infor ION API Gateway ION Documents API](https://apis.io/collections/infor/open-infor-ion-documents-api/)
- [Infor ION API Gateway ION Documents M3 API API](https://apis.io/collections/infor/open-infor-m3-api-api/)

#### Overlays (4)

OpenAPI overlays, including conversational phrasing for each operation.

- [Infor Ion Documents Api Overlay](https://apis.io/overlays/infor/infor-ion-documents-api-overlay/)
- [Infor Ion Documents Api Phrasing Overlay](https://apis.io/overlays/infor/infor-ion-documents-api-phrasing-overlay/)
- [Infor M3 Api Api Overlay](https://apis.io/overlays/infor/infor-m3-api-api-overlay/)
- [Infor M3 Api Api Phrasing Overlay](https://apis.io/overlays/infor/infor-m3-api-api-phrasing-overlay/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Infor — asyncapi rules](https://apis.io/rules/infor/infor-asyncapi-spectral-rules/)
- [Infor — jsonschema rules](https://apis.io/rules/infor/infor-jsonschema-spectral-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Infor Authentication](https://apis.io/security/infor/infor-authentication/)
- [Infor Domain Security](https://apis.io/security/infor/infor-domain-security/)
- [Infor Trust Center](https://apis.io/security/infor/infor-trust-center/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Infor Scopes](https://apis.io/scopes/infor/infor-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Infor Plans Pricing](https://apis.io/plans/infor/infor-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Infor Rate Limits](https://apis.io/rate-limits/infor/infor-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Infor Finops](https://apis.io/finops/infor/infor-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.infor.com/)
- [Documentation](https://docs.infor.com/)
- [Getting started](https://developer.infor.com/tutorials)
- [API reference](https://developer.infor.com/api)
- [Pricing](https://www.infor.com/products)
- [Support](https://www.infor.com/customer-success/support)
- [Blog](https://www.infor.com/blog)
- [Trust centre](https://trust.infor.com/)
- [Terms of service](https://www.infor.com/en/about/legal)
- [Privacy policy](https://www.infor.com/en/about/privacy)
- [GitHub](https://github.com/infor-cloud)

## API Evangelist rating

**Kin Score 68.3** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 58.0 |
| Contract governance | 31.8 |
| Operational transparency | 63.2 |
| Developer ergonomics | 82.7 |
| Access clarity | 75.0 |

**Agent readiness 33.2** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | yes |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 39.2** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/infor/](https://apis.io/providers/infor/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Infor: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/infor/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
