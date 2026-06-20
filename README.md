# Preset (preset)

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
