[**Открыть опубликованный сайт →**](https://ekatmoz88-alt.github.io/technical-writing-portfolio/)

[English](README.md) | **Русский**

# Портфолио технического писателя

**Enterprise API & Software Architecture Documentation · OpenAPI 3.1 · Docs-as-Code · EN/RU**

## Обзор

Портфолио демонстрирует компетенции Senior Technical Writer в проектировании API-документации, информационной архитектуре, Developer Experience, контроле качества документации и документировании enterprise-систем.

Комплект Orders API в этом репозитории построен вокруг самостоятельного демонстрационного API-контракта. Он показывает полный процесс проектирования и сопровождения документации: от OpenAPI 3.1 и API Reference до руководства разработчика, обработки ошибок и сценариев Webhooks. Это не документация развёрнутого Supabase Orders API из отдельного репозитория [API Documentation Portfolio V2](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2).

## Что демонстрирует портфолио

- Проектирование API Reference и информационной архитектуры.
- Подготовку спецификаций OpenAPI 3.1 и согласование контракта с документацией.
- Документирование REST-эндпоинтов, параметров, схем и ответов.
- Примеры запросов и ответов, описание обработки ошибок.
- Модели событий Webhooks, payload, проверку подписи, повторные доставки и дедупликацию.
- Руководства для разработчиков и интеграционные сценарии.
- Docs-as-Code: Markdown, Git, ревью и публикацию.
- Процессы проверки, валидации и QA-чек-листы.
- Англоязычную и русскоязычную структуру материалов портфолио.
- Архитектурные кейсы enterprise-систем и материалы C4 / UML / BPMN с явным обозначением границ подтверждённых сведений.

## Избранные материалы

| Материал | Файл | Что демонстрирует |
|---|---|---|
| Демонстрационный OpenAPI-контракт | [openapi/openapi.yaml](openapi/openapi.yaml) | Пути API, схемы, компоненты, security и примеры Webhooks |
| API Reference | [docs/api-reference.md](docs/api-reference.md) | Описание эндпоинтов, параметров, ответов и иллюстративных примеров |
| Обработка ошибок | [docs/error-handling.md](docs/error-handling.md) | HTTP-ошибки и единый формат рекомендаций по обработке ответов |
| Webhooks | [docs/webhooks.md](docs/webhooks.md) | Примеры событий, payload, HMAC-подпись, повторы и дедупликация |
| Руководство разработчика | [docs/developer-guide.md](docs/developer-guide.md) | Демонстрационные сценарии авторизации, первого запроса, пагинации и Webhooks |
| Информационная архитектура | [docs/information-architecture.md](docs/information-architecture.md) | Уровни документации, навигация и локализация |
| Процесс Docs-as-Code | [docs/documentation-workflow.md](docs/documentation-workflow.md) | Ветки, ревью, проверки и публикация |
| QA checklist | [docs/testing-api-documentation.md](docs/testing-api-documentation.md) | Проверка точности, примеров, удобства и локализации |
| История изменений | [docs/changelog.md](docs/changelog.md) | История изменений документации |

## Инструменты и процесс

OpenAPI 3.1 · YAML · Markdown · Git · Postman/cURL · процессы документирования API

- **Spec-first:** OpenAPI — структурированный источник для API Reference и связанных артефактов демонстрационного контракта.
- **Developer-first:** руководства и примеры показывают, как интегратор может решать типовые задачи.
- **Docs-as-Code:** исходники документации хранятся в Git и подготовлены для ревью.
- **Единообразие:** повторно используемые структуры и терминология упрощают сопровождение.
- **Двуязычное портфолио:** материалы верхнего уровня представлены на английском и русском языках.

## Контекст и границы достоверности

Orders API в этом репозитории — спроектированный демонстрационный пример для показа методов документирования API. Адреса `api.example.com` и `api.sandbox.example.com` являются placeholder-адресами. Эндпоинты, OAuth flow, scopes, пагинация, события Webhooks, формат подписи, политика повторных доставок и примеры относятся к демонстрационному контракту. Их нельзя трактовать как возможности действующего сервиса или инструкции для production-интеграции.

Развёрнутый Supabase Orders API — отдельная реализация, документированная в [API Documentation Portfolio V2](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2). Репозитории показывают разные стороны API-документирования и реализации; их контракты и возможности не взаимозаменяемы.

## Автор

**Kate Motsar** — Senior Technical Writer | API & Enterprise Documentation | Docs-as-Code

[GitHub profile](https://github.com/ekatmoz88-alt) · [LinkedIn](https://www.linkedin.com/in/ekatmoz88/)

## Теги

`api-documentation` · `openapi-3-1` · `developer-docs` · `webhooks` · `docs-as-code` · `enterprise-architecture` · `en-ru`

## Связь с API Documentation Portfolio V2

[API Documentation Portfolio V2](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2) — отдельный проект. В нём находятся развёрнутая Supabase Edge Function, реализация на PostgreSQL и соответствующая документация API с Quickstart.

Текущий репозиторий не является расширением этого развёрнутого API и не описывает тот же API-контракт. Здесь размещён самостоятельный пример Orders API и более широкий документационный кейс: проектирование API Reference, руководство разработчика, обработка ошибок, сценарии Webhooks, QA документации и Docs-as-Code.

## Дополнительный архитектурный кейс

Отдельный архитектурный кейс описывает Enterprise Insurance System с C4-inspired container view и ERD сущностей CDB/APPLN.

- [Enterprise Insurance System — Architecture Case Study](case-studies/enterprise-insurance-system/README.md)

В кейсе явно обозначены неподтверждённые предположения о технологиях и связях. Он не представлен как обратная реконструкция production-системы.

## Дополнительные архитектурные кейсы

- [SOIS — Spacecraft Onboard Interface Services](case-studies/sois/README.ru.md) — архитектурные уровни, onboard interface services, subnetwork services, классы QoS, CDAS и TAS. Анализ реальной архитектуры SOIS по стандартам CCSDS; это не реконструкция конкретной бортовой инсталляции.

## Enterprise / Backend / Integration-heavy documentation

Сводная карта материалов портфолио по архитектуре систем, backend и data-моделям, API-контрактам, интеграциям и техническим диаграммам:

- [Enterprise Documentation — обзор портфолио](./docs/enterprise-documentation/README.ru.md)
- [Интерактивная страница](./site/enterprise-documentation/index.html)
- [Модуль C4 / UML Sequence / BPMN 2.0](./site/enterprise-documentation/diagrams/index.html)
- [Исходники диаграмм](./docs/enterprise-documentation/diagrams/README.md)

Карта объединяет материалы отдельных реальных проектов; она сохраняет границы систем и отдельно обозначает проектные модели и фактические компоненты.
