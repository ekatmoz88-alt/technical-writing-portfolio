# Разработка, проверки и публикация

## Быстрые ссылки

- [Опубликованный сайт](https://ekatmoz88-alt.github.io/technical-writing-portfolio/)
- [Репозиторий](https://github.com/ekatmoz88-alt/technical-writing-portfolio)
- [GitHub Actions — все запуски](https://github.com/ekatmoz88-alt/technical-writing-portfolio/actions)
- [GitHub Actions workflow](https://github.com/ekatmoz88-alt/technical-writing-portfolio/blob/main/.github/workflows/pages.yml)
- [Документация проекта](README.md)

## Локальная работа

Откройте репозиторий и следуйте инструкциям в README и workflow. Проверяйте относительные ссылки, корректность путей и согласованность примеров с исходными спецификациями.

## Что проверить перед публикацией

Проверьте YAML и согласованность endpoint/schema/example в OpenAPI и справочнике. Убедитесь, что webhook-раздел описывает подпись, retries и дедупликацию. Сверьте EN/RU материалы.

## Release checklist

- [ ] Изменения соответствуют структуре и назначению проекта.
- [ ] Внутренние и внешние ссылки проверены.
- [ ] Примеры и спецификации согласованы.
- [ ] Нет секретов, токенов или реальных персональных данных.
- [ ] [GitHub Actions workflow](https://github.com/ekatmoz88-alt/technical-writing-portfolio/blob/main/.github/workflows/pages.yml) завершился успешно.
- [ ] [Опубликованный сайт](https://ekatmoz88-alt.github.io/technical-writing-portfolio/) открывается и показывает ожидаемую версию.

## Диагностика

1. Откройте [GitHub Actions](https://github.com/ekatmoz88-alt/technical-writing-portfolio/actions) и выберите последний запуск.
2. Найдите первый упавший step и прочитайте его лог.
3. Проверьте trigger, branch и path-фильтры в workflow.
4. Исправьте первопричину, повторите проверку и убедитесь, что Pages deployment завершился успешно.

Не считайте публикацию успешной только по факту успешной сборки: проверьте deployment и сам сайт.
