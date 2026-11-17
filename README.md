[**Open the rendered portfolio website →**](https://ekatmoz88-alt.github.io/technical-writing-portfolio/)

[English](README.md) | [Русский](README.ru.md)

# Technical Writing Portfolio

**Enterprise API & Software Architecture Documentation · OpenAPI 3.1 · Docs-as-Code · EN/RU**

## Overview

A senior-level technical writing portfolio demonstrating API documentation architecture, developer experience, documentation quality practices, and enterprise software architecture case studies.

The Orders API documentation set in this repository is built around an independent sample API contract. It demonstrates how to design and maintain a coherent documentation set — from OpenAPI 3.1 and API reference to developer onboarding, error handling, and webhook workflows. It is not the documentation of the deployed Supabase Orders API in [API Documentation Portfolio V2](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2).

## What this project demonstrates

- API reference design and information architecture.
- OpenAPI 3.1 specification authoring and contract-to-documentation consistency.
- REST endpoint, parameter, schema, and response documentation.
- Request/response examples and error handling.
- Webhook event models, payloads, signature verification, retries, and deduplication.
- Developer onboarding guides and integration workflows.
- Docs-as-Code workflows using Markdown and Git.
- Documentation review, validation, and QA checklists.
- English/Russian portfolio navigation and content structure.
- Enterprise architecture case studies and C4 / UML / BPMN-related materials, with explicit evidence boundaries.

## Selected artifacts

| Artifact | File | What it demonstrates |
|---|---|---|
| OpenAPI sample contract | [openapi/openapi.yaml](openapi/openapi.yaml) | API paths, schemas, reusable components, security, and sample webhooks |
| API reference | [docs/api-reference.md](docs/api-reference.md) | Endpoint descriptions, parameters, responses, and illustrative examples |
| Error handling | [docs/error-handling.md](docs/error-handling.md) | HTTP errors and consistent error response guidance |
| Webhooks | [docs/webhooks.md](docs/webhooks.md) | Sample event payloads, HMAC verification, retries, and deduplication |
| Developer guide | [docs/developer-guide.md](docs/developer-guide.md) | Sample authentication, first request, pagination, and webhook workflows |
| Information architecture | [docs/information-architecture.md](docs/information-architecture.md) | Documentation layers, navigation, and localization |
| Docs workflow | [docs/documentation-workflow.md](docs/documentation-workflow.md) | Branching, review, validation, and publishing |
| QA checklist | [docs/testing-api-documentation.md](docs/testing-api-documentation.md) | Accuracy, examples, usability, and localization checks |
| Changelog | [docs/changelog.md](docs/changelog.md) | Documentation change history |

## Tools and workflow

OpenAPI 3.1 · YAML · Markdown · Git · Postman/cURL · API documentation workflows

- **Spec-first:** OpenAPI is the structured source for the sample API reference and related contract artifacts.
- **Developer-first:** guides and examples demonstrate how integrators can complete common API tasks.
- **Docs-as-Code:** sources are versioned in Git and organized for review.
- **Consistency:** reusable structures and terminology support maintainability.
- **Bilingual portfolio:** English and Russian portfolio-level materials.

## Project context and evidence boundaries

The Orders API contract in this repository is a designed sample used to demonstrate API documentation methods. Its `api.example.com` and `api.sandbox.example.com` server URLs are placeholders; the endpoints, OAuth flow, scopes, pagination, webhook events, signature format, retry policy, and examples are part of the sample contract. They must not be treated as live service capabilities or production integration instructions.

The deployed Supabase Orders API is a separate implementation documented in [API Documentation Portfolio V2](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2). The two repositories demonstrate different aspects of API documentation and implementation; their API contracts and capabilities are not interchangeable.

## Author

**Kate Motsar** — Senior Technical Writer | API & Enterprise Documentation | Docs-as-Code

[GitHub profile](https://github.com/ekatmoz88-alt) · [LinkedIn](https://www.linkedin.com/in/ekatmoz88/)

## Tags

`api-documentation` · `openapi-3-1` · `developer-docs` · `webhooks` · `docs-as-code` · `enterprise-architecture` · `en-ru`

## Relationship to API Documentation Portfolio V2

[API Documentation Portfolio V2](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2) is a separate project containing the deployed Supabase Edge Function, its PostgreSQL-backed implementation, and the corresponding OpenAPI documentation and Quickstart.

This repository is not an extension of that deployed API and does not describe the same API contract. It contains an independent sample Orders API specification and a broader documentation case study covering API reference design, developer guidance, error handling, webhook workflows, documentation QA, and Docs-as-Code practices.

## Additional architecture case study

A separate architecture case study covers an Enterprise Insurance System using a GitHub-renderable C4-inspired container view and an ERD of CDB/APPLN entities.

- [Enterprise Insurance System — Architecture Case Study](case-studies/enterprise-insurance-system/README.md)

The case study labels unverified technology and relationship assumptions explicitly; it is not presented as a production-system reverse engineering result.

## Additional architecture case studies

- [SOIS — Spacecraft Onboard Interface Services (RU)](case-studies/sois/README.ru.md) — architecture layers, onboard interface services, subnetwork services, QoS classes, CDAS and TAS. A standards-based analysis of the real CCSDS SOIS architecture; it is not a reconstruction of a specific spacecraft installation.

## Enterprise / Backend / Integration-heavy documentation

A consolidated map of the portfolio evidence for system architecture, backend and data models, API contracts, integrations and technical diagrams:

- [Enterprise Documentation — portfolio map](./docs/enterprise-documentation/README.md)
- [Interactive overview](./site/enterprise-documentation/index.html)
- [C4 / UML Sequence / BPMN 2.0 module](./site/enterprise-documentation/diagrams/index.html)
- [Diagram source index](./docs/enterprise-documentation/diagrams/README.md)

The map links separate real project repositories without merging their system boundaries or presenting draft architecture models as fully verified physical deployment topologies.
