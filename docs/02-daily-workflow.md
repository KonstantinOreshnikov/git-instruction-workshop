# Daily Workflow / Ежедневный workflow

## English

### Start work

```bash
git switch main
git pull --ff-only
git switch -c feat/short-description
```

`git pull --ff-only` refuses to create an unexpected merge commit. Teams may choose another pull strategy, but it should be explicit and consistent.

### Make a focused commit

```bash
git status
git diff
git add path/to/file
git diff --staged
git commit -m "feat: describe the user-visible change"
```

Stage confirmed paths instead of blindly staging the entire working tree. A useful commit represents one logical change and can be reviewed or reverted independently.

### Publish the branch

```bash
git push -u origin feat/short-description
```

Open a draft pull request when early feedback is useful. The PR description should explain the problem, the change, validation and known limitations.

## Русский

### Начало работы

```bash
git switch main
git pull --ff-only
git switch -c feat/short-description
```

`git pull --ff-only` не позволит незаметно создать неожиданный merge commit. Команда может отличаться в конкретной команде, но стратегия должна быть явной и одинаковой для всех.

### Логичный коммит

```bash
git status
git diff
git add path/to/file
git diff --staged
git commit -m "feat: describe the user-visible change"
```

Добавляйте в индекс конкретные проверенные файлы, а не всё содержимое рабочей директории вслепую. Хороший коммит содержит одно логическое изменение и может быть независимо проверен или отменён.

### Публикация ветки

```bash
git push -u origin feat/short-description
```

Открывайте draft pull request, если нужна ранняя обратная связь. В описании PR укажите проблему, изменение, проведённые проверки и известные ограничения.

Source / Источник: [GitHub Flow](https://docs.github.com/en/get-started/using-github/github-flow)

