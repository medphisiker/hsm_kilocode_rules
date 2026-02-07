# Active Context: HSM

## Текущее состояние
- [x] Реализована поддержка Docker-контейнеров.
- [x] Внедрен механизм `implies` для зависимостей.
- [x] Переход на иерархическое хранение режимов в `hsm.yaml`.
- [x] Обновлена документация и CLI.
- [x] Реализована поддержка `HSM_REGISTRY_PATH` и команда `package init`.
- [x] Реализован механизм Implication Merging.
- [x] Выполнен архитектурный рефакторинг Core и CLI (2026 Edition).
- [x] Реализована команда `hsm check`.
- [x] Покрыто функциональными тестами (19 тестов).

## Фокус
- [ ] Расширение экосистемы адаптеров (Pixi, Podman).
- [ ] Оптимизация производительности через параллельную синхронизацию.

## Активные задачи
1. **Валидация окружения и Тестирование**:
   - План (Validation): [hsm/tasks_descriptions/plans/environment_validation.md](../../../tasks_descriptions/plans/environment_validation.md)
   - План (Testing): [hsm/tasks_descriptions/plans/testing_strategy_implementation.md](../../../tasks_descriptions/plans/testing_strategy_implementation.md)
   - Задача (Inspector): [hsm/tasks_descriptions/tasks/implement_environment_inspector.md](../../../tasks_descriptions/tasks/implement_environment_inspector.md)
   - Задача (Tests): [hsm/tasks_descriptions/tasks/implement_environment_tests.md](../../../tasks_descriptions/tasks/implement_environment_tests.md)
2. **Расширение адаптеров**:
   - План: [hsm/tasks_descriptions/plans/expanding_adapters.md](../../../tasks_descriptions/plans/expanding_adapters.md)
   - Задача (Pixi): [hsm/tasks_descriptions/tasks/implement_pixi_adapter.md](../../../tasks_descriptions/tasks/implement_pixi_adapter.md)
3. **Параллельная синхронизация**:
   - План: [hsm/tasks_descriptions/plans/parallel_sync.md](../../../tasks_descriptions/plans/parallel_sync.md)

## Открытые вопросы
- Нет.