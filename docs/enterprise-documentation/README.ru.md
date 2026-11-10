# Enterprise Documentation — карта подтверждённых артефактов

[Открыть интерактивный обзор](https://ekatmoz88-alt.github.io/technical-writing-portfolio/enterprise-documentation/) · [Модуль диаграмм](https://ekatmoz88-alt.github.io/technical-writing-portfolio/enterprise-documentation/diagrams/) · [English](./README.md)

## Цель

Собрать в одном месте реальные публичные материалы портфолио, которые демонстрируют документирование сложных enterprise-, backend- и integration-heavy систем. Это не заявление о том, что каждый проект содержит полный комплект документации: карта показывает конкретные подтверждённые артефакты и пробелы.

## Результат аудита репозиториев

| Направление | Подтверждённые материалы | Репозитории / доказательства | Оценка |
|---|---|---|---|
| Enterprise/system architecture | Логические границы систем, deployment views, component maps, trust boundaries, evidence notes | [Architecture catalogue](https://github.com/ekatmoz88-alt/territory-descriptor-unified), [PPO Territory archive](https://github.com/ekatmoz88-alt/ppo-territory-archive), [ARM Descriptor](https://github.com/ekatmoz88-alt/descriptor-arm-spec) | Сильная сторона |
| Integrations and interfaces | Семь направлений внешнего обмена, SOAP/WSDL client case, JSON operations, XML/file exchange, API-to-database mapping | [PPO integrations](https://github.com/ekatmoz88-alt/ppo-territory-archive/blob/main/docs/04-external-integrations.md), [UMMS SOAP](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2/blob/main/umms-enterprise-soap-client.html), [Territory API](https://github.com/ekatmoz88-alt/territory-docs/blob/main/api/index.md) | Сильная сторона |
| API contracts | OpenAPI 3.1, REST paths, schemas, security schemes, examples, error responses, automated linting | [API Documentation V2](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2) | Сильная сторона |
| Data architecture | Oracle inventory and ER views, 401-table inventory, JSON-to-Oracle mappings, SQLite data-access review | [Territory docs](https://github.com/ekatmoz88-alt/territory-docs), [Deshifrator docs](https://github.com/ekatmoz88-alt/deshifrator-docs) | Сильная сторона |
| UML sequence | A sequence-style interaction model can be derived from the documented Orders API authentication and request flow; existing sequence examples also occur in the MIB3 portfolio material | [Orders API contract](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2/blob/main/openapi/openapi.yaml) | Добавлен демонстрационный артефакт; требует сверки с runtime-кодом |
| C4 | Existing architecture catalogue contains system landscape and logical architecture views, but the reviewed sources do not establish a complete, consistently maintained native C4 model across all systems | [Architecture catalogue](https://github.com/ekatmoz88-alt/territory-descriptor-unified) | Требовалась стандартизация; добавлен C4 view для Orders API demo |
| BPMN | Business processes and KYC/operator journeys are documented; reviewed repositories did not show a verified BPMN 2.0 model | [Fintech workflow](https://github.com/ekatmoz88-alt/fintech-docs-demo), [AS FB and DROND source basis](https://github.com/ekatmoz88-alt/technical-writing-portfolio/tree/main/docs/enterprise-documentation) | Добавлена BPMN 2.0 реконструкция по ДОА 2011; не является исходной схемой |
| Operational documentation | Developer guides, quickstarts, operational workflows, lifecycle testing, platform requirements | [API docs](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2), [PPO archive](https://github.com/ekatmoz88-alt/ppo-territory-archive) | Есть, но неодинаково глубоко по проектам |

## Рекомендуемые кейсы для работодателя

1. **PPO Territory / unified architecture catalogue** — лучший пример системной и enterprise-архитектурной документации: системные границы, deployment alternatives, интеграционный ландшафт, component maps, data architecture и evidence boundaries.
2. **API Documentation Portfolio V2** — лучший пример API contracts и integration documentation: OpenAPI 3.1, REST, SOAP/WSDL, XML/XSD, request/response models, auth and validation.
3. **Territory Docs** — лучший пример backend/data documentation: Oracle data model, ER views, API operations, JSON-to-table mappings, validation and rollback notes.
4. **Deshifrator / ARM Descriptor** — примеры legacy application architecture, source-based component analysis, file exchange, workstation boundaries and technical requirements.
5. **АС ФБ и ДРОНД** — отдельный бизнес-процессный кейс на основе ДОА 2011 года: бюджетное планирование, импорты/экспорты, согласования, РРО и ОБАС.

## Кейс АС ФБ и ДРОНД

[Бизнес-процессный кейс](./case-studies/as-fb-drond.md) — отдельное описание предметной области, источников, последовательности предложений / РРО / ОБАС и границ доказательности.

## Диаграммный модуль

[Открыть интерактивный модуль](../../site/enterprise-documentation/diagrams/index.html).

В нём собраны:
- C4 Context для интеграционного ландшафта ППО «Территория».
- C4 Container view для демонстрационного Orders API.
- UML Sequence Diagram для аутентифицированного API-вызова.
- BPMN 2.0 process model для процесса формирования бюджета по ДОА АС ФБ и ДРОНД.
- Mermaid source для воспроизводимого редактирования.
- Ссылки на существующие архитектурные каталоги и ER-диаграммы.

## Границы достоверности

- Демонстрационный Orders API не следует выдавать за production enterprise-сервис.
- C4 и UML Sequence для Orders API — документированные демонстрационные представления, но конкретные детали runtime должны сверяться с кодом и конфигурацией.
- BPMN для АС ФБ и ДРОНД реконструирована по тексту «Детального описания объекта автоматизации» 2011 года. В исходном фрагменте диаграммы отсутствовали; модель не выдаётся за оригинал или подтверждённый workflow внедрённой системы.
- Диаграммы PPO Territory / ARM Descriptor / Deshifrator различают подтверждённые сведения, логические представления и непроверенные зависимости. Не объединять системы в одну runtime-архитектуру.
- BPMN, UML и C4 — разные нотации. Mermaid flowchart не следует называть BPMN; для BPMN здесь хранится отдельный файл BPMN 2.0 XML.

## Позиционирование

Подтверждённая формулировка:

> Technical Writer focused on enterprise system documentation, backend and data architecture, API contracts, legacy integrations, and evidence-based technical diagrams. Experienced in turning source documents, API specifications, database structures and code excerpts into structured documentation, traceable models and maintainable Docs-as-Code deliverables.

Не заявлять, что все перечисленные проекты являются действующими production-системами или что для каждого создан полный комплект C4/BPMN/UML-артефактов.
