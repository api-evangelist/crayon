# Quarantine — these artifacts describe a DIFFERENT company

**Quarantined 2026-08-14 by the API Evangelist enrichment pipeline (STEP 0c ownership check).**

Everything in this directory was harvested or derived in an earlier round under the assumption
that `apidocs.crayon.com` / `api.crayon.com` belonged to the company profiled by this repository.
**It does not.** There are two unrelated companies named "Crayon":

| | This repository (`aid: crayon`) | The company these files describe |
|---|---|---|
| Company | Crayon | Crayon Group ASA |
| Domain | `crayon.co` | `crayon.com` |
| Product | Competitive intelligence / battlecards / win-loss | Microsoft CSP resale, Cloud-iQ, software asset management |
| HQ | Boston, MA, USA | Oslo, Norway |
| API host | `mcp.crayon.co`, `app.crayon.co` | `api.crayon.com` |
| Docs | none public | `https://apidocs.crayon.com` ("CrayonApi documentation") |
| GitHub | `github.com/Crayon-Co` | `github.com/CrayonGroup` |
| LinkedIn | `linkedin.com/company/crayon-co` | `linkedin.com/company/crayon-group` |

## What the evidence said

The spec was judged by what it says about itself, not by where it was fetched:

- `servers[]` → `https://api.crayon.com/api/v1` — the **`.com`** host, not `crayon.co`.
- `info.contact.url` → `https://apidocs.crayon.com`.
- `info.description` → "Crayon's REST API for managing **CSP organizations, users, customer
  tenants, Microsoft subscriptions, Azure plans, agreements, invoices and billing statements**."
  That is Crayon Group's Cloud-iQ CSP platform. Crayon (`crayon.co`) sells competitive
  intelligence and ships no such resource model.
- `scopes/crayon-scopes.yml` recorded the scope `CustomerApi` sourced from
  `https://apidocs.crayon.com/getting-started/authentication.html` and named the product
  **"Cloud-iQ"** in its own note.
- `https://apidocs.crayon.com/` returns `<title>Crayon API Documentation — CrayonApi documentation</title>`
  and its SDK samples live at `github.com/CrayonGroup/crayon-api-sdk`.

## Second defect: the spec was never published

`openapi/_original/crayon-openapi.yml` says in its own `info.description`:

> "Endpoint inventory drawn from the public scenarios catalog at https://apidocs.crayon.com."

It is a hand-scaffolded inventory, not a spec Crayon Group published. `https://api.crayon.com/openapi.json`,
`/swagger.json` and `/api/v1/openapi.json` all return **404**. So even for Crayon Group this
would not be a harvested contract.

## Consequences

Everything derived from that spec inherited its provenance and is quarantined with it:
`openapi/` (8 refined + 1 original), `collections/` (Postman + Open Collection),
`agentic-access/`, `crayon-authentication.yml`, `crayon-scopes.yml`.

The corresponding `apis.yml` entries and `common[]` pointers were removed. Nothing here is
referenced by `apis.yml` any more, so nothing here is scored. Files are retained rather than
deleted so the mistake stays auditable.

## If you are Crayon Group ASA

These files are about your platform, not the company profiled here. If you would like a correct,
separate profile built from your own published surface — or these removed entirely — email
[info@apievangelist.com](mailto:info@apievangelist.com).
