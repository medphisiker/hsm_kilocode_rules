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

### 2026-02-08
- **Refactoring**: Выполнен масштабный рефакторинг моделей и реестра (ADR-002).
- **Architecture**: Переход от технологического разделения (пакеты/контейнеры) к функциональному (библиотеки/сервисы).
- **Architecture**: Внедрена поддержка рантаймов (`RuntimeType`) в профилях развертывания сервисов.
- **Architecture**: Реализована поддержка Virtual Environment Services (VES) через рантайм `uv`.
- **Features**: Добавлена команда `hsm service init` для создания изолированных сервисов.
- **Features**: Реализована полная изоляция VES через `--no-workspace` и `UV_NO_WORKSPACE=1`.
- **Testing**: Внедрена система версионированных песочниц в `debug_tests/` с поддержкой `LATEST.txt`.
- **Testing**: Добавлена поддержка `.env` файлов для локальной настройки отладки.
- **Documentation**: Создан Technical Design по управлению конфигурацией и обновлена стратегия тестирования.
- **CLI**: Команды `package` и `container` заменены на `library` и `service`.
- **CLI**: Команда `hsm list` теперь отображает рантаймы сервисов.
- **Features**: Реализована полная поддержка Virtual Environment Services (VES) в `SyncEngine`.
- **Features**: Добавлена материализация сервисов из Git-репозиториев в режиме `prod`.
- **Features**: Реализован резолвинг зависимостей для изолированных сервисов через реестр HSM.
- **Features**: Интегрирован проброс ENV через Implication Merging для VES.
- **CLI**: Команда `hsm registry service add` расширена опциями `--runtime` и `--dependency`.
- **Testing**: Добились 100% прохождения High-Fidelity тестов (`isolation`, `git`, `env`, `sandbox`).
- **Features**: Реализован CLI для управления импликациями (`hsm registry ... implies add/remove`).
- **Architecture**: Упрощена логика режимов (modes) — теперь это атомарные намерения на уровне компонентов.
- **Documentation**: Создан полный обзор системы тестирования `tests/TESTS_OVERVIEW.md`.
- **Documentation**: Обновлены технические дизайны по High-Fidelity тестированию и стратегии.

### 2026-02-22
- **Features**: Реализована поддержка `env_file` для сервисов на уровне моделей (`ServiceManifest`/`Source`), CLI реестра и SyncEngine.
- **Features**: Добавлена материализация `.env.<service>` и проброс `env_file` в ветки `docker`/`uv` с единой логикой резолвинга.
- **Features**: Включен fail-fast контроль конфликтов ENV-источников (`env_file`, `manifest.env`, `source.env`, `implies params`) с диагностикой источников.
- **CLI**: Команда `hsm registry service add` расширена опциями `--env-file`, `--prod-env-file`, `--dev-env-file`.
- **CLI**: Для `hsm library init` и `hsm service init` реализован флаг `--git-init`.
- **Core**: Добавлен `HSMCore._init_git(...)` с fail-fast обработкой ошибок (`git` binary missing / `git init` failed).
- **Testing**: Реализованы сценарии `ENV-FAIL-001..006`, `ENV-HF-001..004`, `ENV-CLI-001`, `GIT-CLI-001`, `GIT-HF-*`, `GIT-FAIL-*`.
- **Testing**: Добавлен файл `tests/test_project_init_git.py` и набор env-ассетов в `tests/assets/env_files/`.
- **Testing**: Обновлен `tests/TESTS_OVERVIEW.md` по новым сценариям active-задач.
- **Quality**: Подтверждено полное прохождение тестов: `uv run pytest tests -q` → `46 passed`.
