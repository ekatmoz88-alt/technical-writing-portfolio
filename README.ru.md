[**Открыть опубликованный сайт →**](https://ekatmoz88-alt.github.io/technical-writing-portfolio/)

[English](README.md) | **Русский**

# Портфолио технического писателя

Портфолио по документированию REST API и OpenAPI.

**Фокус:** REST API · OpenAPI 3.1 · документация для разработчиков · Docs-as-Code · EN/RU

## Обзор

Документация реального проекта Orders API. Описывает OpenAPI-контракт, подключение разработчиков и интеграторов, API Reference, обработку ошибок и сценарии вебхуков.

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

Orders API — реальный развёрнутый сервис. Репозиторий содержит документацию его контракта и интеграционных сценариев. В публичных примерах используются контролируемые тестовые данные; закрытые учётные данные и клиентская информация не публикуются.

## Автор

**Kate Motsar** — Technical Writer | API Documentation | Developer Docs


## Теги

`api-documentation` · `openapi-3-1` · `webhooks` · `developer-docs` · `docs-as-code` · `en-ru`


## Связь с API Documentation Portfolio V2

Этот репозиторий содержит дополнительные материалы документации реального Orders API. Реализация и развёрнутая Supabase Edge Function находятся в [API Documentation Portfolio V2](https://github.com/ekatmoz88-alt/api-docs-portfolio-v2).


## Дополнительные архитектурные кейсы

- [SOIS — концепция и архитектура служб бортовых интерфейсов](case-studies/sois/README.ru.md) — уровни архитектуры, службы Application Support и Subnetwork, классы QoS, CDAS и TAS. Концептуальный анализ стандарта, не описание реализованной бортовой системы.


## Enterprise / Backend / Integration-heavy documentation

Сводная карта подтверждённых материалов по архитектуре систем, backend и data-моделям, API-контрактам, интеграциям и техническим диаграммам:

- [Enterprise Documentation — обзор портфолио](./docs/enterprise-documentation/README.ru.md)
- [Интерактивная страница](./site/enterprise-documentation/index.html)
- [Модуль C4 / UML Sequence / BPMN 2.0](./site/enterprise-documentation/diagrams/index.html)
- [Исходники диаграмм](./docs/enterprise-documentation/diagrams/README.md)

Карта объединяет материалы отдельных реальных проектов; она сохраняет границы систем и отдельно обозначает проектные модели и фактические компоненты.
