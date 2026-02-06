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
1. **Расширение адаптеров**:
   - План: [hsm/docs/plans/expanding_adapters.md](../../../docs/plans/expanding_adapters.md)
   - Задача (Pixi): [hsm/docs/tasks/implement_pixi_adapter.md](../../../docs/tasks/implement_pixi_adapter.md)
   - Задача (Podman): [hsm/docs/tasks/implement_podman_adapter.md](../../../docs/tasks/implement_podman_adapter.md)
2. **Параллельная синхронизация**:
   - План: [hsm/docs/plans/parallel_sync.md](../../../docs/plans/parallel_sync.md)

## Открытые вопросы
- Нет.