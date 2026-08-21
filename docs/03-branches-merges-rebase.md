# Branches, Merge and Rebase / Ветки, merge и rebase

## English

A branch isolates a line of work. Create it from an up-to-date base and keep its purpose narrow.

```bash
git switch -c feat/export-report
git branch --show-current
git branch -vv
```

### Merge

Merge joins histories and may create a merge commit. It preserves the fact that development occurred in parallel.

```bash
git switch main
git merge feat/export-report
```

### Rebase

Rebase replays commits on a new base. It can produce a linear history, but it changes commit IDs.

```bash
git switch feat/export-report
git fetch origin
git rebase origin/main
```

Do not casually rebase commits that other people already use. If a rebased personal branch must be pushed, prefer:

```bash
git push --force-with-lease
```

`--force-with-lease` checks that the remote branch has not advanced unexpectedly. It reduces risk but does not make rewriting shared history harmless.

### Conflict workflow

```bash
git status
# edit conflicted files and remove conflict markers
git add path/to/resolved-file
git merge --continue   # during merge
git rebase --continue  # during rebase
```

Abort when the operation should not continue:

```bash
git merge --abort
git rebase --abort
```

## Русский

Ветка изолирует отдельное направление работы. Создавайте её от актуальной базовой ветки и ограничивайте одной понятной задачей.

### Merge

Merge объединяет истории и может создать merge commit. Он сохраняет факт параллельной разработки.

### Rebase

Rebase повторно применяет коммиты поверх новой базы. История становится линейнее, но идентификаторы коммитов меняются.

Не выполняйте rebase общей истории без согласования. Для публикации переписанной личной ветки используйте `git push --force-with-lease`, а не обычный `--force`. Проверка lease снижает риск перезаписать чужие изменения, но не превращает переписывание общей истории в безопасную операцию.

При конфликте сначала выполните `git status`, вручную исправьте файлы, добавьте их в индекс и продолжите операцию. Если продолжать нельзя, используйте `git merge --abort` или `git rebase --abort`.

Sources / Источники: [Basic branching and merging](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging), [Rebasing](https://git-scm.com/book/en/v2/Git-Branching-Rebasing), [git-rebase](https://git-scm.com/docs/git-rebase)

