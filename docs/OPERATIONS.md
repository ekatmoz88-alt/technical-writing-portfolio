# Разработка и публикация

## Полезные ссылки
- [Сайт портфолио](https://ekatmoz88-alt.github.io/technical-writing-portfolio/)
- [Репозиторий](https://github.com/ekatmoz88-alt/technical-writing-portfolio)
- [Запуски GitHub Actions](https://github.com/ekatmoz88-alt/technical-writing-portfolio/actions)
- [Pages workflow](../.github/workflows/pages.yml)

## Проверки перед публикацией
- Проверьте YAML и OpenAPI contract.
- Сверьте endpoints, параметры, схемы и примеры со справочником.
- Проверьте webhook signature, retries и deduplication.
- Проверьте внутренние ссылки и EN/RU материалы.
- Убедитесь, что Pages deployment завершился успешно и сайт открывается.

## Диагностика
В Actions откройте последний запуск и найдите первый упавший step. Проверьте trigger/path filters и повторите ошибочную команду локально. Не добавляйте токены или реальные персональные данные.
