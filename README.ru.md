[**Открыть опубликованный сайт →**](https://ekatmoz88-alt.github.io/technical-writing-portfolio/)

[English](README.md) | **Русский**

# Портфолио технического писателя

Портфолио по документированию REST API и OpenAPI.

**Фокус:** REST API · OpenAPI 3.1 · документация для разработчиков · Docs-as-Code · EN/RU

## Обзор

Демонстрационный проект по документированию вымышленного Orders API. Показывает, как я выстраиваю документацию для разработчиков и интеграторов: от OpenAPI-контракта до руководства по подключению и описания вебхуков.

## Что демонстрирует портфолио

- Проектирование API Reference и информационной архитектуры.
- Подготовку спецификации OpenAPI 3.1.
- Документирование REST-эндпоинтов, параметров, схем и ответов.
- Примеры запросов и ответов, описание обработки ошибок.
- Документирование событий вебхуков, payload, проверки подписи и повторных доставок.
- Руководства для разработчиков.
- Docs-as-Code: Markdown и Git.
- Чек-листы проверки точности и качества документации.
- Структуру документации на английском и русском языках.

## Избранные материалы

| Материал | Файл | Что демонстрирует |
|---|---|---|
| OpenAPI-контракт | [openapi/openapi.yaml](openapi/openapi.yaml) | Пути API, схемы, переиспользуемые компоненты и вебхуки |
| Справочник API | [docs/api-reference.md](docs/api-reference.md) | Описание эндпоинтов, параметров и ответов |
| Обработка ошибок | [docs/error-handling.md](docs/error-handling.md) | HTTP-ошибки и единые рекомендации по ответам |
| Вебхуки | [docs/webhooks.md](docs/webhooks.md) | События, payload, HMAC-подпись, повторы и дедупликация |
| Руководство разработчика | [docs/developer-guide.md](docs/developer-guide.md) | Авторизация, первый запрос, пагинация и вебхуки |
| Информационная архитектура | [docs/information-architecture.md](docs/information-architecture.md) | Уровни документации, навигация и локализация |
| Процесс Docs-as-Code | [docs/documentation-workflow.md](docs/documentation-workflow.md) | Ветки, ревью, проверки и публикация |
| Чек-лист качества | [docs/testing-api-documentation.md](docs/testing-api-documentation.md) | Точность, примеры, удобство и локализация |
| История изменений | [docs/changelog.md](docs/changelog.md) | История изменений документации |

## Инструменты

OpenAPI 3.1 · YAML · Markdown · Git · Postman/cURL · процессы документирования API

## Подход

- **Spec-first:** OpenAPI выступает структурированным контрактом для API Reference.
- **Developer-first:** руководства и примеры помогают интеграторам решать практические задачи.
- **Docs-as-Code:** исходники документации хранятся в Git и подготовлены для ревью.
- **Единообразие:** повторно используемые структуры и терминология упрощают поддержку.
- **Два языка:** материалы портфолио представлены на английском и русском.

## Контекст проекта

Orders API — демонстрационный, вымышленный API. Проект показывает структуру и артефакты документации и не является действующим production-сервисом.

## Автор

**Kate Motsar** — Technical Writer | API Documentation | Developer Docs


## Теги

`api-documentation` · `openapi-3-1` · `webhooks` · `developer-docs` · `docs-as-code` · `en-ru`


## Связь с API Documentation Portfolio V2

Этот репозиторий — отдельный демонстрационный пример документации вымышленного Orders API. Это не тот же сервис, что Supabase Edge Function в [API Documentation Portfolio V2](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2). В V2 размещены развёрнутый демонстрационный API и дополнительные кейсы legacy SOAP/WSDL.


## Дополнительные архитектурные кейсы

- [SOIS — концепция и архитектура служб бортовых интерфейсов](case-studies/sois/README.ru.md) — уровни архитектуры, службы Application Support и Subnetwork, классы QoS, CDAS и TAS. Концептуальный анализ стандарта, не описание реализованной бортовой системы.


## Enterprise / Backend / Integration-heavy documentation

Сводная карта подтверждённых материалов по архитектуре систем, backend и data-моделям, API-контрактам, интеграциям и техническим диаграммам:

- [Enterprise Documentation — обзор портфолио](./docs/enterprise-documentation/README.ru.md)
- [Интерактивная страница](./site/enterprise-documentation/index.html)
- [Модуль C4 / UML Sequence / BPMN 2.0](./site/enterprise-documentation/diagrams/index.html)
- [Исходники диаграмм](./docs/enterprise-documentation/diagrams/README.md)

Карта объединяет ссылки на отдельные репозитории; она не смешивает их системы и не выдаёт демонстрационные модели за production-архитектуру.
