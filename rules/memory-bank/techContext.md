# Technical Context: HSM

## Технологический стек
- **Язык**: Python 3.13+
- **CLI Framework**: `typer`
- **YAML Engine**: `ruamel.yaml` (для сохранения комментариев)
- **UI/Logging**: `rich`
- **Package Manager**: `uv` (основной адаптер)
- **Orchestration**: `docker compose`

## Среда разработки
- **IDE**: VS Code / Kilo Code
- **Установка**: Рекомендуется устанавливать HSM в режиме редактирования как инструмент `uv`: `uv tool install -e ./hsm` (из корня репозитория). 
Это позволяет использовать команду `hsm` глобально, при этом изменения в коде подпроекта `hsm/` подхватываются автоматически.
- **Testing**: `pytest` (планируется)