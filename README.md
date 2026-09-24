# Pathly Postman collection

**English** · [Français](README.fr.md) · [Español](README.es.md)


[![Powered by Pathly](https://img.shields.io/badge/Powered%20by-Pathly-0B5FFF?style=flat-square)](https://pathlyhq.com)
[![Website](https://img.shields.io/badge/Website-pathlyhq.com-111827?style=flat-square)](https://pathlyhq.com)
[![API docs](https://img.shields.io/badge/API-developers-2563eb?style=flat-square)](https://pathlyhq.com/en/developers)
[![Start free](https://img.shields.io/badge/Solo-start%20free-16a34a?style=flat-square)](https://pathlyhq.com/en/login?mode=signup)

> **Get started in one click.** Create a free account on [Pathly](https://pathlyhq.com) ([sign up](https://pathlyhq.com/en/login?mode=signup)), create an API key in the console, then export `PATHLY_API_TOKEN`. This project is the official bridge to [Pathly monitoring](https://pathlyhq.com) — real-browser and HTTP checks for checkout, login and availability, with data hosted in the EU. Full API reference: [pathlyhq.com/en/developers](https://pathlyhq.com/en/developers).

> English is the default / canonical documentation language.

Explore the [Pathly](https://pathlyhq.com) public `/v1` API from Postman (or any
OpenAPI-friendly importer). Covers scenarios, webhooks, maintenance windows,
SLA targets, runs, incidents, settings and status components.

- Product: [pathlyhq.com](https://pathlyhq.com)
- API docs: [pathlyhq.com/en/developers](https://pathlyhq.com/en/developers)
- API host: `https://api.pathlyhq.com`


## Files

| File | Role |
|---|---|
| [`Pathly.postman_collection.json`](Pathly.postman_collection.json) | Collection v2.1 — all `/v1` endpoints |
| [`Pathly.postman_environment.json`](Pathly.postman_environment.json) | Environment: `baseUrl` + `apiToken` |

OpenAPI source of truth (importable): ship or fetch the Pathly OpenAPI document
linked from [developers](https://pathlyhq.com/en/developers). This collection
mirrors the same paths and is safe to import without regenerating.

## Import

1. Open Postman → **Import** → select both JSON files.
2. Select the **Pathly** environment.
3. Set `apiToken` to your organization key (`sp_…`). Leave `baseUrl` as
   `https://api.pathlyhq.com` unless you use a private endpoint.
4. Send **Org → Get usage** first. HTTP **403** can still mean a valid key that
   lacks `org:read` (least privilege for scenario-only tokens).

## Authentication

All requests use **Bearer** auth:

```http
Authorization: Bearer {{apiToken}}
```

Never commit a real token. Prefer a local environment override or a secret vault
synced into Postman. Scope reference:
[pathlyhq.com/en/developers](https://pathlyhq.com/en/developers).

Creates (`POST` / `PUT` on mutable resources) include an `Idempotency-Key`
header (`{{$guid}}`) so retries stay safe.

## Related packages

| Package | Role |
|---|---|
| [pathly-sdk-python](https://github.com/pathlyhq/pathly-sdk-python) | Python SDK |
| [pathly-sdk-ruby](https://github.com/pathlyhq/pathly-sdk-ruby) | Ruby gem |
| [pathly-sdk-typescript](https://github.com/pathlyhq/pathly-sdk-typescript) | `@pathlyhq/sdk` |
| [pathly-terraform-provider](https://github.com/pathlyhq/pathly-terraform-provider) | Terraform / OpenTofu |

## About Pathly

[Pathly](https://pathlyhq.com) is synthetic monitoring for agencies and e-commerce: replay the customer journey, catch broken checkouts before your clients call, and keep evidence (screenshot, step, runbook) ready for the invoice. Product: [pathlyhq.com](https://pathlyhq.com) · Developers: [pathlyhq.com/en/developers](https://pathlyhq.com/en/developers) · Status & pricing: [pathlyhq.com/en/pricing](https://pathlyhq.com/en/pricing).

## Author

| | |
|---|---|
| **Company** | Pathly |
| **Author** | Simon Raynaud / keyral |

See [AUTHORS](AUTHORS).

## License
Apache-2.0
