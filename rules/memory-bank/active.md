# Active Context: HSM

## Текущее состояние
- [x] Реализована поддержка Docker-контейнеров.
- [x] Внедрен механизм `implies` для зависимостей.
- [x] Переход на иерархическое хранение режимов в `hsm.yaml`.
- [x] Обновлена документация и CLI.

## Фокус
- [ ] Рефакторинг системы адаптеров (Абстракция над Python и Контейнерами).

## Активные задачи
1. **Рефакторинг адаптеров**:
   - План: [hsm/docs/plans/adapter_abstraction.md](../../../docs/plans/adapter_abstraction.md)
   - Контекст задачи: [hsm/docs/tasks/refactor_adapters.md](../../../docs/tasks/refactor_adapters.md)

## Открытые вопросы
- Реализация `hsm check` для валидации без изменений.