# Crayon (crayon)

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

Crayon is a Boston-based competitive intelligence platform that automatically captures, analyzes and distributes competitor activity — website and pricing changes, product updates, social posts, news, reviews, job postings and review-site sentiment — and turns it into battlecards, competitor profiles, win/loss stories, objection handling and email digests for product marketing, sales enablement and go-to-market teams. On 2026-09-04 Crayon shipped what it describes as the first competitive-intelligence MCP server, a hosted OAuth-protected Model Context Protocol endpoint that exposes a customer's own curated Crayon content to Claude, ChatGPT, Glean, Microsoft Copilot, Google Gemini and internal Slack or Teams assistants.

> **Two different companies are named Crayon.** This profile is **Crayon, `crayon.co`** (competitive
> intelligence, Boston). It is **not** **Crayon Group ASA, `crayon.com`** (Microsoft CSP resale and
> software asset management, Oslo), whose API lives at `api.crayon.com` / `apidocs.crayon.com`.
> An earlier round of this profile conflated the two; the artifacts built from Crayon Group's
> platform have been quarantined in [`_wrong-company/`](_wrong-company/README.md) and are no longer
> referenced or scored.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/crayon/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/crayon/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Competitive Intelligence
- Market Intelligence
- Sales Enablement
- Battlecards
- Win-Loss Analysis
- Product Marketing
- AI
- MCP

## Timestamps

- **Created:** 2026-05-11
- **Modified:** 2026-08-14

## APIs

### Crayon Competitive Intelligence MCP Server

Hosted Model Context Protocol server exposing a customer's curated Crayon competitive intelligence
to MCP-capable assistants. JSON-RPC over Streamable HTTP, protected by OAuth 2.1 with dynamic
client registration and the single scope `mcp:read`.

- **Human URL:** [Crayon launches the first competitive intelligence MCP server](https://www.crayon.co/blog/crayon-launches-first-competitive-intelligence-mcp-server)
- **Base URL:** `https://mcp.crayon.co/mcp/`
- **Verified:** 2026-08-14 — anonymous `tools/list` POST returns HTTP 401 with an RFC 9728
  `resource_metadata` challenge naming `https://app.crayon.co/` as the authorization server.

#### Properties

- [MCP Server](mcp/crayon-mcp.yml)
- [Authentication](authentication/crayon-authentication.yml)
- [OAuth Scopes](scopes/crayon-scopes.yml)

### Crayon Content and Answers API

Marketed by Crayon, but no endpoint, base URL, authentication model or reference is published for
either API — access runs through a sales conversation. No base URL is recorded because Crayon
publishes none.

- **Human URL:** [Connecting competitive intel to enterprise AI with API and MCP](https://www.crayon.co/blog/connecting-competitive-intel-to-enterprise-ai-with-api-mcp)

## Artifacts

| Artifact | File | Method |
|---|---|---|
| MCP server | [mcp/crayon-mcp.yml](mcp/crayon-mcp.yml) | probed |
| Well-known index | [well-known/crayon-well-known.yml](well-known/crayon-well-known.yml) | probed |
| OAuth protected resource (RFC 9728) | [well-known/crayon-oauth-protected-resource.json](well-known/crayon-oauth-protected-resource.json) | verbatim |
| OAuth authorization server (RFC 8414) | [well-known/crayon-oauth-authorization-server.json](well-known/crayon-oauth-authorization-server.json) | verbatim |
| Authentication | [authentication/crayon-authentication.yml](authentication/crayon-authentication.yml) | probed |
| OAuth scopes | [scopes/crayon-scopes.yml](scopes/crayon-scopes.yml) | probed |
| Conventions | [conventions/crayon-conventions.yml](conventions/crayon-conventions.yml) | probed |
| Conformance | [conformance/crayon-conformance.yml](conformance/crayon-conformance.yml) | probed |
| Lifecycle | [lifecycle/crayon-lifecycle.yml](lifecycle/crayon-lifecycle.yml) | searched |
| Plans and pricing | [plans/crayon-plans-pricing.yml](plans/crayon-plans-pricing.yml) | searched |
| Rate limits | [rate-limits/crayon-rate-limits.yml](rate-limits/crayon-rate-limits.yml) | searched |
| Packages | [packages/crayon-packages.yml](packages/crayon-packages.yml) | searched |
| llms.txt | [llms/crayon-llms.txt](llms/crayon-llms.txt) | generated |
| Domain security | [security/crayon-domain-security.yml](security/crayon-domain-security.yml) | probed |

## Not published by Crayon

Recorded as measured absences, each with a probed URL and status in the artifact above:

- No OpenAPI, Swagger, GraphQL SDL, AsyncAPI or JSON Schema on any `crayon.co` host.
- No developer portal or API reference. `api.`, `docs.`, `developer.`, `developers.`, `status.`,
  `trust.`, `security.`, `knowledge.` and `academy.crayon.co` are wildcard DNS and return the
  byte-identical `www.crayon.co` marketing homepage with HTTP 200.
- No `llms.txt` (404), no `security.txt` (404), no A2A agent card (404 on both the canonical and
  legacy paths), no `api-catalog`, no `ai-plugin.json`.
- No status page — `crayon.statuspage.io` is unclaimed and redirects to `statuspage.io`.
- No published pricing, rate limits, changelog, release notes, roadmap, SLA or deprecation policy.
- No first-party SDK, CLI or client library in any public registry.
- No published compliance certifications (no SOC 2, ISO 27001, PCI DSS, HIPAA or FedRAMP claim).

## Common Properties

- [Website](https://www.crayon.co)
- [Blog](https://www.crayon.co/blog)
- [Pricing](https://www.crayon.co/pricing)
- [Login](https://app.crayon.co/login)
- [Terms of Service](https://www.crayon.co/terms)
- [Privacy Policy](https://www.crayon.co/privacy)
- [Integrations](https://www.crayon.co/integrations)
- [LinkedIn](https://www.linkedin.com/company/crayon-co)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
