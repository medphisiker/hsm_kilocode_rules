# Active Context: HSM

## Текущее состояние
- [x] Реализована архитектура Service Runtimes (VES/ADR-002).
- [x] Внедрена полная изоляция сервисов через рантайм `uv`.
- [x] Реализован механизм Implication Merging для гибридных стеков.
- [x] Обеспечено 100% покрытие High-Fidelity тестами (isolation, git, env).
- [x] Публичная документация полностью обновлена и реорганизована.
- [x] Реализована поддержка `env_file` для сервисов (registry/model/sync, fail-fast merge).
- [x] Реализован флаг `--git-init` для `hsm library init` и `hsm service init`.
- [x] Закрыт цикл Hybrid TDD для активных задач (`env_file` + `--git-init`).

## Фокус
- Реализация следующего блока задач Level 3: Environment Inspector и Pixi адаптер.
- Опорный контекст: [`hsm_active_tasks_test_design.md`](tasks_descriptions/plans/hsm_active_tasks_test_design.md).

## Активные задачи
- [-] Реализовать Environment Inspector ([`implement_environment_inspector.md`](tasks_descriptions/tasks/implement_environment_inspector.md))
- [ ] Реализовать Pixi адаптер ([`implement_pixi_adapter.md`](tasks_descriptions/tasks/implement_pixi_adapter.md))

## Next Up (Level 3)
- [ ] Реализовать Environment Inspector ([`implement_environment_inspector.md`](tasks_descriptions/tasks/implement_environment_inspector.md))
- [ ] Реализовать Pixi адаптер ([`implement_pixi_adapter.md`](tasks_descriptions/tasks/implement_pixi_adapter.md))
- [ ] Автоматическое добавление локальных путей моделей в `.gitignore` при регистрации ([`auto_ignore_local_models.md`](tasks_descriptions/tasks/auto_ignore_local_models.md))

## Открытые вопросы
- Нет.
