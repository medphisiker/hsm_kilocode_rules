# Active Context: HSM

## Текущее состояние
- [x] Реализована поддержка Docker-контейнеров.
- [x] Внедрен механизм `implies` для зависимостей.
- [x] Переход на иерархическое хранение режимов в `hsm.yaml`.
- [x] Обновлена документация и CLI.

## Фокус
- [ ] Реализация инфраструктуры для Self-Bootstrapping тестирования (`HSM_REGISTRY_PATH`, `package init`).
- [ ] Реализация механизма Implication Merging (слияние зависимостей).
- [ ] Покрытие проекта функциональными тестами (Level 1.1 - 1.3).

## Активные задачи
1. **Инфраструктура тестирования**:
   - Поддержка `HSM_REGISTRY_PATH`: [hsm/docs/tasks/support_hsm_registry_path.md](../../../docs/tasks/support_hsm_registry_path.md)
   - Команда `hsm package init`: [hsm/docs/tasks/implement_package_init.md](../../../docs/tasks/implement_package_init.md)
2. **Слияние зависимостей (Merging)**:
   - План: [hsm/docs/plans/implication_merging.md](../../../docs/plans/implication_merging.md)
   - Задача: [hsm/docs/tasks/implement_implication_merging.md](../../../docs/tasks/implement_implication_merging.md)
3. **Функциональное тестирование**:
   - Задача: [hsm/docs/tasks/implement_functional_tests.md](../../../docs/tasks/implement_functional_tests.md)
4. **Валидация (Dry-run)**:
   - Задача: [hsm/docs/tasks/implement_hsm_check.md](../../../docs/tasks/implement_hsm_check.md)

## Открытые вопросы
- Реализация `hsm check` для валидации без изменений.