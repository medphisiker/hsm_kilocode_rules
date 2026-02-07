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
- **Testing**: Проведено исследование лучших практик тестирования CLI на 2026 год.
- **Testing**: Создана стратегия тестирования ([`hsm/docs/technical_design/11_testing_strategy.md`](hsm/docs/technical_design/11_testing_strategy.md:1)).
- **Testing**: Реализован первый уровень автоматического тестирования (10 тестов на базе `CliRunner`).

### 2026-02-06
- **Features**: Реализована поддержка `HSM_REGISTRY_PATH` для изоляции реестра.
- **Features**: Добавлена команда `hsm package init` для быстрой инициализации пакетов.
- **Features**: Реализован механизм **Implication Merging** для слияния параметров зависимостей.
- **Features**: Реализована команда `hsm check` для dry-run валидации.
- **Architecture**: Проведен глубокий рефакторинг Core и CLI (2026 Edition) с использованием паттерна Facade и разделением на модули.
- **Research**: Проведено исследование трендов Python 3.13 и архитектурных паттернов 2026 года.
- **Testing**: Расширено тестовое покрытие до 19 функциональных тестов, включая полный цикл работы в sandbox.

### 2026-02-07
- **Documentation**: Полная реорганизация документации и создание сайта на базе Docusaurus.
- **Documentation**: Разделение контента на публичный (сайт) и внутренний (бэклог в `tasks_descriptions`).
- **Documentation**: Обновлен README.md с описанием концепции Intent vs Artifacts и примером Hybrid Stack.
- **Documentation**: Включена поддержка Mermaid диаграмм и исправлены ошибки MDX.
- **Architecture**: Структурирован раздел Архитектура (ADR, Технический дизайн, Исследования, Идеи).
- **Community**: Обновлен список авторов и социальные ссылки проекта.