# Preset (preset)

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

Preset is a managed cloud BI and analytics platform powered by Apache Superset. Its REST API combines a Preset Manager surface (authentication, teams, workspaces, users, guest tokens) at https://api.app.preset.io with a per-workspace proxy to the underlying Superset REST API for charts, dashboards, datasets, databases, and SQL Lab.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/preset/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/preset/refs/heads/main/apis.yml)

## Tags

- BI
- Analytics
- Superset
- Dashboards
- Data Visualization

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Preset Auth API

Exchanges an API token name and secret for a short-lived JWT access token via POST /v1/auth/. The returned bearer token authenticates all subsequent Preset Manager and Superset proxy requests.

- **Human URL:** [https://api-docs.preset.io/](https://api-docs.preset.io/)
- **Base URL:** `https://api.app.preset.io/v1`

#### Tags

- Authentication
- JWT
- API Token

#### Properties

- [Documentation](https://docs.preset.io/docs/using-the-api)
- [API Reference](https://api-docs.preset.io/)
- [OpenAPI](openapi/preset-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/preset.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/preset.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Preset Teams and Workspaces API

Preset Manager endpoints for listing teams, listing and creating workspaces within a team, managing team membership, and minting guest tokens for embedded dashboards via POST /v1/teams/{team}/workspaces/{workspace}/guest-token/.

- **Human URL:** [https://api-docs.preset.io/](https://api-docs.preset.io/)
- **Base URL:** `https://api.app.preset.io/v1`

#### Tags

- Teams
- Workspaces
- Users
- Guest Tokens

#### Properties

- [Documentation](https://docs.preset.io/docs/using-the-api)
- [API Reference](https://api-docs.preset.io/)
- [OpenAPI](openapi/preset-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/preset.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/preset.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Preset Superset Dashboards API

Per-workspace proxy to the Apache Superset Dashboard REST API (/api/v1/dashboard/) for listing, creating, reading, updating, deleting, and exporting dashboards as code. Reached at the workspace hostname pattern {workspace-slug}.{region}.app.preset.io.

- **Human URL:** [https://superset.apache.org/docs/api](https://superset.apache.org/docs/api)
- **Base URL:** `https://{workspace-slug}.{region}.app.preset.io/api/v1`

#### Tags

- Superset Proxy
- Dashboards
- BI

#### Properties

- [Documentation](https://docs.preset.io/docs/using-the-api)
- [API Reference](https://superset.apache.org/docs/api)
- [OpenAPI](openapi/preset-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/preset.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/preset.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Preset Superset Charts API

Per-workspace proxy to the Apache Superset Chart REST API (/api/v1/chart/) for CRUD on charts, chart data queries, and import/export of charts as code within a Preset workspace.

- **Human URL:** [https://superset.apache.org/docs/api](https://superset.apache.org/docs/api)
- **Base URL:** `https://{workspace-slug}.{region}.app.preset.io/api/v1`

#### Tags

- Superset Proxy
- Charts
- Visualization

#### Properties

- [Documentation](https://docs.preset.io/docs/using-the-api)
- [API Reference](https://superset.apache.org/docs/api)
- [OpenAPI](openapi/preset-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/preset.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/preset.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Preset Superset Datasets API

Per-workspace proxy to the Apache Superset Dataset REST API (/api/v1/dataset/) for managing physical and virtual datasets, columns, metrics, and the semantic layer.

- **Human URL:** [https://superset.apache.org/docs/api](https://superset.apache.org/docs/api)
- **Base URL:** `https://{workspace-slug}.{region}.app.preset.io/api/v1`

#### Tags

- Superset Proxy
- Datasets
- Semantic Layer

#### Properties

- [Documentation](https://docs.preset.io/docs/using-the-api)
- [API Reference](https://superset.apache.org/docs/api)
- [OpenAPI](openapi/preset-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/preset.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/preset.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Preset Superset Databases API

Per-workspace proxy to the Apache Superset Database REST API (/api/v1/database/) for managing data source connections, testing connectivity, and listing schemas and tables.

- **Human URL:** [https://superset.apache.org/docs/api](https://superset.apache.org/docs/api)
- **Base URL:** `https://{workspace-slug}.{region}.app.preset.io/api/v1`

#### Tags

- Superset Proxy
- Databases
- Connections

#### Properties

- [Documentation](https://docs.preset.io/docs/using-the-api)
- [API Reference](https://superset.apache.org/docs/api)
- [OpenAPI](openapi/preset-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/preset.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/preset.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Preset Superset SQL Lab API

Per-workspace proxy to the Apache Superset SQL Lab REST API (/api/v1/sqllab/execute/) for executing ad hoc SQL against connected databases and retrieving query results.

- **Human URL:** [https://superset.apache.org/docs/api](https://superset.apache.org/docs/api)
- **Base URL:** `https://{workspace-slug}.{region}.app.preset.io/api/v1`

#### Tags

- Superset Proxy
- SQL Lab
- Query

#### Properties

- [Documentation](https://docs.preset.io/docs/using-the-api)
- [API Reference](https://superset.apache.org/docs/api)
- [OpenAPI](openapi/preset-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/preset.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/preset.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/preset-io)
- [LinkedIn](https://www.linkedin.com/company/preset-data)
- [Website](https://www.preset.io)
- [Documentation](https://docs.preset.io)
- [Plans](plans/preset-plans-pricing.yml)
- [Rate Limits](rate-limits/preset-rate-limits.yml)
- [Fin Ops](finops/preset-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
