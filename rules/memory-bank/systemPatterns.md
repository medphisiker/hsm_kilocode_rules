# System Patterns: HSM

## Архитектурные принципы
- **Declarative Intent**: `hsm.yaml` — единственный источник правды.
- **Adapter Pattern**: Ядро (`HSMCore`) не зависит от конкретных инструментов. Вся специфика (uv, docker, pixi) вынесена в специализированные адаптеры рантаймов.
- **Registry-First**: Все компоненты должны быть описаны в реестре перед использованием.
- **Physical Isolation (Sandbox)**: Сервисы в venv-рантаймах разворачиваются в изолированных директориях с использованием `--no-workspace`.

## Ключевые компоненты
- **Manifest Engine**: Парсинг и сохранение YAML с комментариями (`ruamel.yaml`).
- **Registry Manager**: Поиск и валидация компонентов в `hsm-registry/`.
- **Dependency Resolver**: Механизм `implies` для разрешения созависимостей.
- **CLI**: Интерфейс на базе `typer` с поддержкой автодополнения и интерактивного режима.

## Структура данных
- **LibraryManifest**: Описание Python-библиотеки (бывший `PackageManifest`).
- **ServiceManifest**: Описание автономного сервиса с поддержкой нескольких рантаймов (бывший `ContainerManifest`). Поддерживает `docker`, `uv`, `pixi` и др. через `DeploymentProfile`.
- **RegistryGroup**: Универсальное описание группы выбора (`library_group` или `service_group`).