# System Patterns: HSM

## Архитектурные принципы
- **Declarative Intent**: `hsm.yaml` — единственный источник правды.
- **Adapter Pattern**: Ядро (`HSMCore`) не зависит от конкретных пакетных менеджеров. Вся специфика (`uv`, `docker`) вынесена в адаптеры.
- **Registry-First**: Все компоненты должны быть описаны в реестре перед использованием.

## Ключевые компоненты
- **Manifest Engine**: Парсинг и сохранение YAML с комментариями (`ruamel.yaml`).
- **Registry Manager**: Поиск и валидация компонентов в `hsm-registry/`.
- **Dependency Resolver**: Механизм `implies` для разрешения созависимостей.
- **CLI**: Интерфейс на базе `typer` с поддержкой автодополнения и интерактивного режима.

## Структура данных
- **PackageManifest**: Описание Python-пакета.
- **ContainerManifest**: Описание Docker-контейнера.
- **RegistryGroup**: Описание группы выбора (1-of-N / M-of-N).