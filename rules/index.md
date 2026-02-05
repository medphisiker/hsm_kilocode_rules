# HSM: Навигатор проекта

Этот файл является точкой входа для AI-агента при работе над инструментом **Hyper Stack Manager (HSM)**.

Отвечай на русском языке при диалоге с пользователем.

## 🗺️ Карта знаний (Entry Points)

### 🛠️ Правила и Стандарты (Автозагрузка)
- [Инструментальные правила](./tooling.md) — Переносимые стандарты (ADR, Git, поведение, отладка).
- [Проектные правила](./project.md) — Специфика HSM (стек, структура).

### 🧠 Память проекта HSM (Ленивая загрузка)
- `.kilocode/rules/memory-bank/product.md` — Цели HSM и концепция Meta-Orchestrator.
- `.kilocode/rules/memory-bank/active.md` — Текущее состояние и задачи HSM.
- `.kilocode/rules/memory-bank/progress.md` — История изменений HSM.
- `.kilocode/rules/memory-bank/systemPatterns.md` — Архитектура (Core, Adapters, Registry).
- `.kilocode/rules/memory-bank/techContext.md` — Технологический стек (Python, Typer, Docker).

### 📜 Навыки (Lazy-loaded Skills)
- `.kilocode/skills/documentation-writer/SKILL.md`
- `.kilocode/skills/researcher/SKILL.md`
- `.kilocode/skills/maintenance/SKILL.md`

## 🚀 Как работать с HSM
1. При получении задачи по HSM проверь `active.md` в этой папке.
2. Следуй архитектурным паттернам из `systemPatterns.md`.