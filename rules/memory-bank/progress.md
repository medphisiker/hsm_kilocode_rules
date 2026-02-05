# Progress: HSM

## История изменений

### 2026-02-04
- **Features**: Реализована поддержка Docker-контейнеров в CLI и Core.
- **Features**: Внедрен механизм `implies` для автоматического разрешения созависимостей.
- **Architecture**: Переход на иерархическое хранение режимов (`mode`) в `hsm.yaml`.
- **UX**: Добавлено динамическое автодополнение (shell completion) для команд.
- **Documentation**: Полное обновление технического дизайна и руководств пользователя.

### 2026-02-05
- **Refactoring**: Выполнен рефакторинг системы адаптеров. Логика вынесена в `hsm/src/hyper_stack_manager/adapters/`.
- **Architecture**: Реализована динамическая загрузка адаптеров через Python Entry Points (`hsm.package_managers`, `hsm.container_engines`).
- **Documentation**: Обновлен `techContext.md` с рекомендацией по установке в режиме редактирования (`uv tool install -e`).