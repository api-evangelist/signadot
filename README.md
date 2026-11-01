# Signadot

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

Signadot is a Kubernetes-native platform for validating microservices and AI-generated code changes against real dependencies before merge. Its core is environment virtualization: large numbers of lightweight ephemeral "sandboxes" spin up in seconds by routing request-level traffic to only the changed services on a shared cluster, without duplicating the whole stack. Testing capabilities — Jobs (Playwright/Cypress/k6 runners), Smart Tests (AI regression detection), and Plans (reusable validation workflows) — layer on top, and a bundled MCP server plus installable Agent Skills let coding agents (Cursor, Claude Code, Codex) provision environments and validate their own work. Signadot installs as a Kubernetes operator, integrates with service meshes and CI/CD, and exposes a REST control-plane API, a CLI, and a Go SDK.

**Areas:** Company · Developer Tools · Kubernetes · Testing · Ephemeral Environments · Microservices · Preview Environments · Agentic Development · Continuous Integration · Developer Experience

## Signadot on APIs.io

Everything profiled for Signadot is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/signadot/](https://apis.io/providers/signadot/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [Signadot Cluster API](https://apis.io/apis/signadot/signadot-cluster-api/) — The Cluster API from Signadot — 5 operation(s) for cluster.
- [Signadot Orgs API](https://apis.io/apis/signadot/signadot-orgs-api/) — The Orgs API from Signadot — 1 operation(s) for orgs.
- [Signadot ResourcePlugins API](https://apis.io/apis/signadot/signadot-resourceplugins-api/) — The ResourcePlugins API from Signadot — 2 operation(s) for resourceplugins.
- [Signadot RouteGroups API](https://apis.io/apis/signadot/signadot-routegroups-api/) — The RouteGroups API from Signadot — 2 operation(s) for routegroups.
- [Signadot Sandboxes API](https://apis.io/apis/signadot/signadot-sandboxes-api/) — The Sandboxes API from Signadot — 2 operation(s) for sandboxes.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (1)

Multi-step workflows that chain operations into a business task.

- [Create and inspect a Signadot sandbox](https://apis.io/arazzos/signadot/signadot-create-and-inspect-sandbox/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [signadot](https://apis.io/servers/signadot/signadot/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Signadot Agentic Access](https://apis.io/agentic-access/signadot/signadot-agentic-access/)

#### Collections (5)

Postman and Open Collection request collections.

- [Signadot Cluster API](https://apis.io/collections/signadot/open-signadot-cluster-api/)
- [Signadot Cluster Orgs API](https://apis.io/collections/signadot/open-signadot-orgs-api/)
- [Signadot Cluster ResourcePlugins API](https://apis.io/collections/signadot/open-signadot-resourceplugins-api/)
- [Signadot Cluster RouteGroups API](https://apis.io/collections/signadot/open-signadot-routegroups-api/)
- [Signadot Cluster Sandboxes API](https://apis.io/collections/signadot/open-signadot-sandboxes-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Signadot Openapi Overlay](https://apis.io/overlays/signadot/signadot-openapi-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Signadot Authentication](https://apis.io/security/signadot/signadot-authentication/)
- [Signadot Domain Security](https://apis.io/security/signadot/signadot-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://signadot.com/)
- [Documentation](https://www.signadot.com/docs/overview)
- [Getting started](https://www.signadot.com/docs/getting-started/installation)
- [API reference](https://www.signadot.com/docs/api)
- [Pricing](https://www.signadot.com/pricing/)
- [Sign up](https://www.signadot.com/signup/)
- [Support](https://signadotcommunity.slack.com)
- [Blog](https://www.signadot.com/blog/)
- [Terms of service](https://www.signadot.com/terms-of-service)
- [Privacy policy](https://www.signadot.com/privacy-policy)
- [GitHub](https://github.com/signadot)
- [Status](https://status.signadot.com/)

## API Evangelist rating

**Kin Score 55.6** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 50.8 |
| Contract governance | 18.2 |
| Operational transparency | 34.2 |
| Developer ergonomics | 73.2 |
| Access clarity | 52.6 |

**Agent readiness 27.9** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | — |
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

**Regulatory alignment 29.4** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/signadot/](https://apis.io/providers/signadot/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Signadot: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/signadot/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
