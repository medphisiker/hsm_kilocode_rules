# Active Context: HSM

## Текущее состояние
- [x] Реализована поддержка Docker-контейнеров.
- [x] Внедрен механизм `implies` для зависимостей.
- [x] Переход на иерархическое хранение режимов в `hsm.yaml`.
- [x] Реализована поддержка `HSM_REGISTRY_PATH` и команда `package init`.
- [x] Реализован механизм Implication Merging.
- [x] Реализована команда `hsm check`.
- [x] Реализован Environment Inspector и верификация синхронизации.
- [x] Спроектирована архитектура Service Runtimes (ADR-002).
- [x] Сформирован бэклог задач для реализации VES.

## Фокус
- [ ] Реализация Service Runtimes (VES) для полной изоляции и гибкости.
- [ ] Исправление и миграция тестов на новую архитектуру.

## Активные задачи
1. **Реализация Service Runtimes (ADR-002)**:
   - План: [tasks_descriptions/plans/service_runtimes_ves.md](../../../tasks_descriptions/plans/service_runtimes_ves.md)
   - Задача 1 (Models): [tasks_descriptions/tasks/refactor_models_and_registry.md](../../../tasks_descriptions/tasks/refactor_models_and_registry.md)
   - Задача 2 (UV Adapter): [tasks_descriptions/tasks/implement_uv_runtime_adapter.md](../../../tasks_descriptions/tasks/implement_uv_runtime_adapter.md)
   - Задача 3 (Sync Engine): [tasks_descriptions/tasks/update_sync_engine_for_ves.md](../../../tasks_descriptions/tasks/update_sync_engine_for_ves.md)
2. **Тестирование и Валидация**:
   - Задача (Tests Migration): [tasks_descriptions/tasks/migrate_tests_to_ves.md](../../../tasks_descriptions/tasks/migrate_tests_to_ves.md)
3. **Документация**:
   - Задача (Website): [tasks_descriptions/tasks/update_website_documentation.md](../../../tasks_descriptions/tasks/update_website_documentation.md)

## Next Up (Level 3)
- Нет.

## Открытые вопросы
- Нет.