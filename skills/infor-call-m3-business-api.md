---
name: infor-call-m3-business-api
description: >-
  Execute an Infor M3 (CloudSuite Industrial) business API program through the
  Infor ION API Gateway — acquire an OAuth 2.0 token from the tenant's Infor OS
  authorization server, call the program, and read the M3 response envelope.
  Use for any read or write against M3 from an agent.
api: Infor M3 API
operations:
  - callM3ApiGet
  - callM3ApiPost
generated: '2026-09-13'
method: generated
source: >-
  openapi/_original/infor-ion-api-gateway-openapi.yml (operationIds verified
  against the spec), conventions/infor-conventions.yml,
  errors/infor-problem-types.yml, authentication/infor-authentication.yml
---

# Call an Infor M3 business API program

## Before you start

You need the tenant's **`.ionapi` credentials file**, downloaded by an
IONAPI-Administrator from the Infor OS API Gateway admin UI. It carries the
tenant id, the gateway host, the client id/secret and the token endpoint. There
is no universal base URL: the gateway is
`https://mingle-ionapi.inforcloudsuite.com/{tenant}/M3` and regional tenants sit
on `mingle-ionapi.{region}.inforcloudsuite.com`. Read the host out of the
`.ionapi` file — do not hard-code one.

The calling identity needs the **IONAPI-User** role.

## 1. Get a token

Infor supports four OAuth 2.0 grants on this gateway: `client_credentials`,
`authorization_code`, `password`, and the SAML bearer grant used when the caller
already holds an Infor OS session. For an unattended agent, use
`client_credentials` with the client id/secret from the `.ionapi` file against
that file's token endpoint.

Present the token as `Authorization: Bearer <token>`.

## 2. Read from M3 — `callM3ApiGet`

`GET /api/{apiVersion}/{programId}`

- `apiVersion` — the M3 API version segment (v2 is the current default; the M3
  H5 SDK moved to v2 endpoints by default in 8.0.0, 2026-03-23).
- `programId` — the M3 business API program to execute.

Program-specific inputs are query parameters. **The contract does not describe
them** — each M3 program defines its own fields, and they are documented in the
M3 API program reference for the tenant's CloudSuite release, not in this
OpenAPI. Do not guess field names.

A `200` returns an `M3ApiResponse` carrying `results` (an array of `M3Record`)
or an `error` (`M3Error` with `messages` of `M3Message`).

## 3. Write to M3 — `callM3ApiPost`

`POST /api/{apiVersion}/{programId}` with an `M3ApiRequest` body.

**Stop and read this before calling it.**

- **There is no idempotency key.** Infor documents no replay protection on this
  gateway. If you retry after a timeout you may execute the transaction twice.
  Treat a timeout as *unknown*, not as *failed*, and verify with a read before
  retrying.
- **There is no reversal in this contract.** Where a reversal exists it is a
  different M3 program invoked through this same operation with a different
  `programId`, and Infor publishes no reversal window. Do not assume a write can
  be taken back.
- Escalate to a human before any write whose consequence you cannot verify with
  a preceding read.

## 4. Handle failures

| Status | Meaning | What to do |
|---|---|---|
| 400 | Unknown `programId`, missing required program field, unroutable request | Re-check `apiVersion`/`programId` and the program's own required fields |
| 401 | Missing/expired token, or a token for a different tenant | Re-acquire a token; confirm the IONAPI-User role |
| 404 | Program not found, or not published to this authorized app | Confirm the suite endpoint is published in the ION API Gateway admin UI |

Errors are **vendor-shaped**, not RFC 9457 problem+json. Read `error.messages[]`
from the `M3Error` object.

**The contract declares no 429 and no 5xx.** The gateway nonetheless enforces
per-endpoint Quota and Throttling policies configured by the tenant
administrator, and Infor does not publish the status code or the headers
returned on exhaustion. Back off exponentially on any unexpected non-2xx and
honour `Retry-After` if one appears.

## Related

- `conventions/infor-conventions.yml` — full cross-cutting semantics
- `errors/infor-problem-types.yml` — error envelope
- `rate-limits/infor-rate-limits.yml` — gateway policy model
