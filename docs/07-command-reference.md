# Command Reference / Справочник команд

## English / Русский

The table below is intentionally bilingual: each command has an English explanation followed by its Russian equivalent.

Таблица ниже намеренно двуязычная: у каждой команды есть пояснение на английском и русский эквивалент.

| Command | English | Русский |
|---|---|---|
| `git init` | Initialize a repository | Инициализировать репозиторий |
| `git clone URL` | Clone a repository | Клонировать репозиторий |
| `git status` | Show working-tree state | Показать состояние рабочей директории |
| `git diff` | Show unstaged changes | Показать изменения вне индекса |
| `git diff --staged` | Show staged changes | Показать подготовленный коммит |
| `git add PATH` | Stage a path | Добавить путь в индекс |
| `git commit -m "..."` | Create a commit | Создать коммит |
| `git log --oneline --graph` | Show compact history | Показать компактную историю |
| `git switch BRANCH` | Switch branches | Переключить ветку |
| `git switch -c BRANCH` | Create and switch | Создать ветку и переключиться |
| `git branch -vv` | Show branches and upstreams | Показать ветки и upstream |
| `git fetch REMOTE` | Download remote references | Загрузить удалённые ссылки |
| `git pull --ff-only` | Fast-forward-only pull | Обновить без неожиданного merge commit |
| `git push -u origin BRANCH` | Push and set upstream | Отправить ветку и настроить upstream |
| `git merge BRANCH` | Merge a branch | Объединить ветку |
| `git rebase BASE` | Replay commits on a base | Перенести коммиты на новую базу |
| `git restore PATH` | Discard unstaged file changes | Отменить изменения файла вне индекса |
| `git restore --staged PATH` | Unstage a path | Убрать путь из индекса |
| `git revert SHA` | Revert with a new commit | Отменить коммит новым коммитом |
| `git reflog` | Show reference movement history | Показать историю перемещения ссылок |

Before running a destructive-looking command, read its official help:

Перед потенциально опасной командой прочитайте официальную справку:

```bash
git help COMMAND
git COMMAND --help
```
