# Branching and Conflict Lab / Практикум по веткам и конфликтам

## Goal / Цель

Practice four branches, an intentional conflict, conflict resolution and a pull-request-ready history.

Отработать четыре ветки, намеренный конфликт, его разрешение и подготовку истории к pull request.

## English

1. Create a new repository with `README.md`.
2. Create branches `feat/alpha`, `feat/beta`, `docs/guide` and `fix/typo`.
3. Make one focused commit in every branch.
4. In `feat/alpha` and `feat/beta`, edit the same line of the same file differently.
5. Merge one branch into `main`.
6. Merge the other branch and resolve the intentional conflict.
7. Review the history with:

```bash
git log --oneline --graph --decorate --all
```

8. Push the final feature branch and open a draft pull request.
9. In the PR description, document the conflict and how it was resolved.

## Русский

1. Создайте новый репозиторий с `README.md`.
2. Создайте ветки `feat/alpha`, `feat/beta`, `docs/guide` и `fix/typo`.
3. Сделайте по одному логичному коммиту в каждой ветке.
4. В `feat/alpha` и `feat/beta` по-разному измените одну строку одного файла.
5. Слейте первую ветку в `main`.
6. Слейте вторую ветку и разрешите намеренный конфликт.
7. Проверьте граф истории.
8. Отправьте итоговую feature-ветку и откройте draft pull request.
9. В PR опишите конфликт и способ его разрешения.

## Acceptance criteria / Критерии приёмки

- four named branches exist in history or reflog;
- commits are focused and clearly named;
- conflict markers are removed;
- the final working tree is clean;
- the PR explains the change and validation.

---

- в истории или reflog видны четыре ветки;
- коммиты логичны и понятно названы;
- маркеры конфликта удалены;
- итоговая рабочая директория чистая;
- PR объясняет изменение и проведённую проверку.

