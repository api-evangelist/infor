---
name: infor-read-ion-documents
description: >-
  List and retrieve Infor ION documents — the OAGIS-derived Business Object
  Documents that ION routes between Infor CloudSuite applications — through the
  ION API Gateway. Read-only flow; safe for an agent to run unsupervised.
api: Infor ION Documents API
operations:
  - listIonDocuments
  - getIonDocument
generated: '2026-09-13'
method: generated
source: >-
  openapi/_original/infor-ion-api-gateway-openapi.yml (operationIds verified
  against the spec), conventions/infor-conventions.yml,
  data-model/infor-data-model.yml, asyncapi/infor-ion-events-asyncapi.yml
---

# Read Infor ION documents

## What these documents are

ION documents are the REST projection of Infor's **Business Object Documents**
(OAGIS-derived), the message format ION uses to move business events between
CloudSuite applications — M3, LN, SunSystems and third-party endpoints. The same
document model appears on the event side in
`asyncapi/infor-ion-events-asyncapi.yml`.

## Authenticate

Same gateway, same OAuth 2.0 as every other ION API call: a bearer token from
the tenant's Infor OS authorization server, using the credentials in the
tenant's `.ionapi` file. Base URL is
`https://mingle-ionapi.inforcloudsuite.com/{tenant}/IONSERVICES` (or the
regional gateway named in that file). The caller needs **IONAPI-User**.

## 1. List — `listIonDocuments`

`GET /ion-api/documents`

Returns a `DocumentList` containing `documents[]` of `Document`.

**Know the limit before you rely on this.** The contract declares no pagination
parameters and Infor publishes no gateway-wide paging convention, so you cannot
tell from the response whether the collection is complete. Do not treat the
returned set as exhaustive; if completeness matters, reconcile against the ION
event stream instead.

The operation declares only a `200`. No 4xx, no 429, no 5xx is described.

## 2. Retrieve one — `getIonDocument`

`GET /ion-api/documents/{documentId}`

`documentId` is the document's identifier, taken from a `Document` in the list
response. Declares `200` and `404`.

A `404` means the document does not exist **or** is not exposed to this
authorized app on this tenant — the contract does not distinguish them, so do
not infer deletion from a 404.

## 3. Crossing into M3

There is none, in the contract. The ION document cluster and the M3 business-API
cluster share no field (`data-model/infor-data-model.yml`). To connect an M3
transaction to the ION document it produced, you need program-specific knowledge
from the M3 API program reference — this API will not tell you.

## Safety

Both operations are reads. Nothing in this skill mutates tenant state.

## Related

- `data-model/infor-data-model.yml` — entity graph
- `asyncapi/infor-ion-events-asyncapi.yml` — the event side of the same model
- `conventions/infor-conventions.yml` — cross-cutting semantics
