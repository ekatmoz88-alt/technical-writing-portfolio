# Enterprise Documentation — evidence-based capability map

[Open interactive overview](../../site/enterprise-documentation/index.html) · [Diagram module](../../site/enterprise-documentation/diagrams/index.html) · [Русская версия](./README.ru.md)

## Purpose

This page consolidates public portfolio evidence for documenting complex enterprise, backend and integration-heavy systems. It does not claim that every project contains a complete documentation set. It identifies concrete artifacts and remaining gaps.

## Repository audit

| Area | Existing evidence | Repositories / source | Assessment |
|---|---|---|---|
| Enterprise/system architecture | System boundaries, deployment views, component maps, trust boundaries and evidence notes | [Architecture catalogue](https://github.com/ekatmoz88-alt/territory-descriptor-unified), [PPO Territory archive](https://github.com/ekatmoz88-alt/ppo-territory-archive), [ARM Descriptor](https://github.com/ekatmoz88-alt/descriptor-arm-spec) | Strong |
| Integrations and interfaces | Seven external exchange directions, SOAP/WSDL client case, JSON operations, XML/file exchange and API-to-database mapping | [PPO integrations](https://github.com/ekatmoz88-alt/ppo-territory-archive/blob/main/docs/04-external-integrations.md), [UMMS SOAP](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2/blob/main/umms-enterprise-soap-client.html), [Territory API](https://github.com/ekatmoz88-alt/territory-docs/blob/main/api/index.md) | Strong |
| API contracts | OpenAPI 3.1, REST paths, schemas, security schemes, examples, error responses and automated linting | [API Documentation V2](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2) | Strong |
| Data architecture | Oracle inventory and ER views, 401-table inventory, JSON-to-Oracle mappings and SQLite data-access review | [Territory docs](https://github.com/ekatmoz88-alt/territory-docs), [Deshifrator docs](https://github.com/ekatmoz88-alt/deshifrator-docs) | Strong |
| UML sequence | Sequence-style interactions can be derived from the documented Orders API authentication and request flow; sequence examples also exist in the MIB3 portfolio material | [Orders API contract](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2/blob/main/openapi/openapi.yaml) | Added demonstration artifact; runtime details require code verification |
| C4 | The architecture catalogue includes system-landscape and logical-architecture views, but the reviewed sources do not establish a complete, consistently maintained native C4 model across all systems | [Architecture catalogue](https://github.com/ekatmoz88-alt/territory-descriptor-unified) | Standardization gap; a C4 view is added for the Orders API demo |
| BPMN | Business processes and KYC/operator journeys exist; the reviewed repositories did not show a verified BPMN 2.0 model | [Fintech workflow](https://github.com/ekatmoz88-alt/fintech-docs-demo), [AS FB and DROND source basis](https://github.com/ekatmoz88-alt/technical-writing-portfolio/tree/main/docs/enterprise-documentation) | Added BPMN 2.0 reconstruction from the 2011 automation-object description; not an original source diagram |
| Operational documentation | Developer guides, quickstarts, operational workflows, lifecycle testing and platform requirements | [API docs](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2), [PPO archive](https://github.com/ekatmoz88-alt/ppo-territory-archive) | Present, with varying depth by project |

## Strongest case studies

1. **PPO Territory / unified architecture catalogue** — strongest system and enterprise architecture example: system boundaries, deployment alternatives, integration landscape, component maps, data architecture and evidence boundaries.
2. **API Documentation Portfolio V2** — strongest API-contract and integration example: OpenAPI 3.1, REST, SOAP/WSDL, XML/XSD, request/response models, authentication and validation.
3. **Territory Docs** — strongest backend/data example: Oracle data model, ER views, API operations, JSON-to-table mappings, validation and rollback notes.
4. **Deshifrator / ARM Descriptor** — legacy application architecture, source-based component analysis, file exchange, workstation boundaries and technical requirements.
5. **AS FB and DROND** — separate business-process case based on the 2011 automation-object description: budget planning, imports/exports, approvals, RRO and OBAS.

## Diagram module

[Open the interactive diagram module](../../site/enterprise-documentation/diagrams/index.html).

It includes:
- A C4 Container view for the Orders API portfolio demo.
- A UML Sequence Diagram for an authenticated API request.
- A BPMN 2.0 process model for budget planning based on the AS FB and DROND 2011 source.
- Editable Mermaid source files.
- Links to existing architecture catalogues and ER diagrams.

## Evidence boundaries

- The Orders API is a portfolio demo, not a production enterprise service.
- The C4 and UML Sequence views are documented demonstration models; runtime details must be checked against code and configuration.
- The AS FB and DROND BPMN model is reconstructed from the supplied 2011 *Detailed Description of the Automation Object*. The referenced original diagrams were not present in the supplied extract. This model is neither an original diagram nor proof of a deployed workflow.
- PPO Territory, ARM Descriptor and Deshifrator diagrams distinguish documented facts, logical views and unverified dependencies. Do not merge these systems into one runtime architecture.
- BPMN, UML and C4 are different notations. A Mermaid flowchart is not BPMN; this portfolio stores a separate BPMN 2.0 XML model.

## Positioning statement

> Technical Writer focused on enterprise system documentation, backend and data architecture, API contracts, legacy integrations, and evidence-based technical diagrams. Experienced in turning source documents, API specifications, database structures and code excerpts into structured documentation, traceable models and maintainable Docs-as-Code deliverables.

Do not claim that all listed projects are live production systems or that every project has a complete C4/BPMN/UML documentation set.
