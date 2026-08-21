# How Git Works / Как работает Git

## English

Git is a distributed version-control system. A local repository contains the project files and enough history to work without a permanent connection to a central server.

The practical model has four areas:

1. **Working tree** — files currently visible and editable.
2. **Staging area** — the exact snapshot prepared for the next commit.
3. **Local repository** — committed snapshots and references such as branches and tags.
4. **Remote repository** — another copy used for collaboration and backup.

A commit is not simply “saving a file.” It records a project snapshot with metadata and a link to its parent commit. A branch is a movable name pointing to a commit. `HEAD` identifies the currently checked-out branch or commit.

```text
Working tree --git add--> Staging area --git commit--> Local repository
Local repository --git push--> Remote repository
Remote repository --git fetch--> Local repository
```

### Why the staging area matters

The staging area lets you build a coherent commit even when the working tree contains unrelated edits. Use `git diff` for unstaged changes and `git diff --staged` for the snapshot that will be committed.

## Русский

Git — распределённая система контроля версий. Локальный репозиторий содержит файлы проекта и историю, достаточную для работы без постоянного подключения к центральному серверу.

Практическая модель состоит из четырёх областей:

1. **Рабочая директория** — видимые и редактируемые файлы.
2. **Индекс (staging area)** — точный снимок, подготовленный для следующего коммита.
3. **Локальный репозиторий** — зафиксированные снимки и ссылки: ветки и теги.
4. **Удалённый репозиторий** — другая копия для совместной работы и резервирования.

Коммит — не просто «сохранение файла». Он фиксирует снимок проекта с метаданными и ссылкой на родительский коммит. Ветка — перемещаемое имя, указывающее на коммит. `HEAD` указывает на текущую ветку или коммит.

### Зачем нужен индекс

Индекс позволяет собрать логичный коммит, даже если в рабочей директории есть несвязанные изменения. `git diff` показывает изменения вне индекса, а `git diff --staged` — снимок, который попадёт в следующий коммит.

## Practice / Практика

```bash
git init
git status
git add README.md
git diff --staged
git commit -m "docs: add project overview"
git log --oneline --decorate --graph
```

Source / Источник: [Pro Git — What is Git?](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F)

