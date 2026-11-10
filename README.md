[**Open the rendered portfolio website →**](https://ekatmoz88-alt.github.io/technical-writing-portfolio/)

[English](README.md) | [Русский](README.ru.md)

# Technical Writing Portfolio

**REST API · OpenAPI 3.1 · Developer Documentation · Docs-as-Code · EN/RU**

## Overview

A portfolio project documenting a fictional Orders API. It demonstrates how to design developer-focused API documentation, from the OpenAPI contract to onboarding guides, error references, and webhook instructions.

## What this project demonstrates

- API reference design and information architecture.
- OpenAPI 3.1 specification authoring.
- REST endpoint, parameter, schema, and response documentation.
- Request/response examples and error handling.
- Webhook events, payloads, signature verification, retries, and deduplication.
- Developer onboarding guides.
- Docs-as-Code workflows using Markdown and Git.
- Documentation review, validation, and QA checklists.
- English/Russian documentation structure.

## Selected artifacts

| Artifact | File | What it demonstrates |
|---|---|---|
| OpenAPI contract | [openapi/openapi.yaml](openapi/openapi.yaml) | API paths, schemas, reusable components, and webhooks |
| API reference | [docs/api-reference.md](docs/api-reference.md) | Endpoint descriptions, parameters, and responses |
| Error handling | [docs/error-handling.md](docs/error-handling.md) | HTTP errors and consistent error response guidance |
| Webhooks | [docs/webhooks.md](docs/webhooks.md) | Event payloads, HMAC verification, retries, and deduplication |
| Developer guide | [docs/developer-guide.md](docs/developer-guide.md) | Authentication, first request, pagination, and webhooks |
| Information architecture | [docs/information-architecture.md](docs/information-architecture.md) | Documentation layers, navigation, and localization |
| Docs workflow | [docs/documentation-workflow.md](docs/documentation-workflow.md) | Branching, review, validation, and publishing |
| QA checklist | [docs/testing-api-documentation.md](docs/testing-api-documentation.md) | Accuracy, examples, usability, and localization checks |
| Changelog | [docs/changelog.md](docs/changelog.md) | Documentation change history |

## Tools and workflow

OpenAPI 3.1 · YAML · Markdown · Git · Postman/cURL · API documentation workflows

- **Spec-first:** OpenAPI is the structured contract for the API reference.
- **Developer-first:** guides and examples help integrators complete common tasks.
- **Docs-as-Code:** sources are versioned in Git and organized for review.
- **Consistency:** reusable structures and terminology support maintainability.
- **Bilingual:** English and Russian portfolio materials.

## Project context

The Orders API is illustrative and simulated. It is a portfolio exercise demonstrating documentation structure and artifacts, not a live production service.

## Author

**Kate Motsar** — Technical Writer | API Documentation | Developer Docs

[GitHub profile](https://github.com/ekatmoz88-alt) · [LinkedIn](https://www.linkedin.com/in/ekatmoz88/)


## Tags

`api-documentation` · `openapi-3-1` · `webhooks` · `developer-docs` · `docs-as-code` · `en-ru`


## Relationship to the API Documentation Portfolio V2

This repository is a separate, simulated Orders API documentation exercise. It is not the same service as the Supabase Edge Function demo in [API Documentation Portfolio V2](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2). The V2 repository contains the deployed portfolio API and additional legacy SOAP/WSDL case studies.


## Additional architecture case study

A separate conceptual case study documents an Enterprise Insurance System using a GitHub-renderable C4-inspired container view and an ERD of CDB/APPLN entities.

- [Enterprise Insurance System — Architecture Case Study](case-studies/enterprise-insurance-system/README.md)

The case study labels unverified technology and relationship assumptions explicitly; it is not presented as a production-system reverse engineering result.


## Enterprise / Backend / Integration-heavy documentation

A consolidated map of the portfolio evidence for system architecture, backend and data models, API contracts, integrations and technical diagrams:

- [Enterprise Documentation — portfolio map](./docs/enterprise-documentation/README.md)
- [Interactive overview](./site/enterprise-documentation/index.html)
- [C4 / UML Sequence / BPMN 2.0 module](./site/enterprise-documentation/diagrams/index.html)
- [Diagram source index](./docs/enterprise-documentation/diagrams/README.md)

The map links separate project repositories without merging their system boundaries or presenting demo models as production architecture.
