# HSM: Навигатор подпроекта

> [!IMPORTANT]
> Директория `hsm/.kilocode` является **отдельным вложенным Git-репозиторием**.
> При внесении изменений в Memory Bank или правила проекта HSM, необходимо выполнять `git add`, `git commit` и `git push` **внутри** папки `hsm/.kilocode`.

Этот файл содержит ссылки на контекст Hyper Stack Manager.

> [!NOTE]
> HSM является автономным подпроектом. Общие правила наследуются из глобального хранилища.

## 🗺️ Карта знаний

### 🛠️ Правила
- [Project Rules](./project.md) — Специфика HSM (адаптеры, манифесты).

### 🧠 Memory Bank
- `.kilocode/rules/memory-bank/active.md` — Текущие задачи HSM.
- `.kilocode/rules/memory-bank/product.md` — Концепция HSM.
- `.kilocode/rules/memory-bank/systemPatterns.md` — Архитектура адаптеров.