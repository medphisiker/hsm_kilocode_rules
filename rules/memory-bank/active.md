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
- [x] Добавить поддержку `env_file` для сервисов HSM ([`add_env_file_support_for_hsm_services.md`](tasks_descriptions/tasks/add_env_file_support_for_hsm_services.md))
- [x] Добавить `--git-init` при инициализации компонентов ([`add_git_init_to_component_init.md`](tasks_descriptions/tasks/add_git_init_to_component_init.md))
- [x] Реализовать тесты по плану Hybrid TDD ([`hsm_active_tasks_test_design.md`](tasks_descriptions/plans/hsm_active_tasks_test_design.md))

## Next Up (Level 3)
- [ ] Реализовать Environment Inspector ([`implement_environment_inspector.md`](tasks_descriptions/tasks/implement_environment_inspector.md))
- [ ] Реализовать Pixi адаптер ([`implement_pixi_adapter.md`](tasks_descriptions/tasks/implement_pixi_adapter.md))

## Открытые вопросы
- Нет.
