# Recovery and Safety / Восстановление и безопасность

## English

Before undoing anything, inspect the state:

```bash
git status
git diff
git diff --staged
git log --oneline --decorate --graph -10
```

### Restore an unstaged file

```bash
git restore path/to/file
```

This discards uncommitted changes in that file. Review the diff first.

### Unstage without discarding the edit

```bash
git restore --staged path/to/file
```

### Revert a published commit

```bash
git revert COMMIT_SHA
```

`revert` creates a new commit that applies the inverse change. It is generally safer for shared history than resetting and force-pushing.

### Find lost work

```bash
git reflog
git switch -c recovery/branch COMMIT_SHA
```

### Secrets

Removing a secret in a later commit does not remove it from Git history. Revoke or rotate the credential first, then use an approved history-cleaning process. Prevention is better: use environment variables, ignored local files and secret scanning.

## Русский

Перед отменой изменений проверьте `status`, оба вида `diff` и последние коммиты.

`git restore path/to/file` удаляет незакоммиченные изменения файла — сначала обязательно посмотрите diff. `git restore --staged` убирает файл из индекса, но сохраняет редактирование.

Для отмены опубликованного коммита обычно безопаснее `git revert`: команда создаёт новый обратный коммит и не переписывает общую историю.

`git reflog` помогает найти ранее доступные коммиты и восстановить потерянную ветку.

Удаление пароля или токена последующим коммитом не удаляет секрет из истории Git. Сначала отзовите или замените credential, затем примените согласованную процедуру очистки истории. Для профилактики используйте переменные окружения, локальные ignored-файлы и secret scanning.

Sources / Источники: [Git documentation](https://git-scm.com/docs), [Viewing history](https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History)

