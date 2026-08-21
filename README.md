# Git Collaboration Guide / Руководство по Git

A bilingual, practice-oriented guide to Git, GitHub and collaborative development.

Двуязычное практическое руководство по Git, GitHub и совместной разработке.

## English

This repository turns several early learning exercises into one structured path: from the mental model of Git to branches, remote repositories, pull requests, conflict resolution and safe recovery.

The guide is based on original learning notes and exercises, rewritten and updated using current official Git and GitHub documentation.

## Русский

Этот репозиторий объединяет несколько ранних учебных проектов в один последовательный маршрут: от модели Git до веток, удалённых репозиториев, pull request, разрешения конфликтов и безопасного восстановления.

Материал основан на собственных учебных заметках и заданиях, переработанных и обновлённых по актуальной официальной документации Git и GitHub.

## Learning path / Учебный маршрут

1. [How Git works / Как работает Git](docs/01-how-git-works.md)
2. [Daily workflow / Ежедневный workflow](docs/02-daily-workflow.md)
3. [Branches, merges and rebase / Ветки, merge и rebase](docs/03-branches-merges-rebase.md)
4. [Remotes, forks and pull requests / Remotes, forks и pull requests](docs/04-remotes-forks-pull-requests.md)
5. [Recovery and safety / Восстановление и безопасность](docs/05-recovery-and-safety.md)
6. [Markdown for repositories / Markdown для репозиториев](docs/06-markdown-for-repositories.md)
7. [Command reference / Справочник команд](docs/07-command-reference.md)
8. [Branching and conflict lab / Практикум по веткам и конфликтам](exercises/branching-conflict-lab.md)

## Recommended workflow / Рекомендуемый workflow

```text
Update main → create a focused branch → make small commits → push → open a draft PR
→ review and checks → address feedback → merge → delete the merged branch

Обновить main → создать тематическую ветку → делать небольшие коммиты → push
→ открыть draft PR → review и проверки → исправить замечания → merge → удалить слитую ветку
```

## Current best practice / Актуальная практика

- Use short-lived branches for focused changes.
- Prefer `git switch` for branches and `git restore` for working-tree recovery.
- Review the diff before every commit.
- Never commit secrets.
- Do not rewrite shared history without coordination.
- Prefer `--force-with-lease` over `--force` when a force push is genuinely required.
- Use pull requests and checks before changing the default branch.

---

- Используйте короткоживущие ветки для конкретных изменений.
- Для переключения веток предпочитайте `git switch`, а для восстановления файлов — `git restore`.
- Проверяйте diff перед каждым коммитом.
- Никогда не добавляйте secrets в Git.
- Не переписывайте общую историю без согласования.
- Если force push действительно необходим, предпочитайте `--force-with-lease`, а не `--force`.
- Изменяйте default branch через pull request и проверки.

## Sources / Источники

The main references are the [Pro Git book](https://git-scm.com/book/en/v2), [Git documentation](https://git-scm.com/docs) and [GitHub Flow](https://docs.github.com/en/get-started/using-github/github-flow).

Основные источники: [книга Pro Git](https://git-scm.com/book/en/v2), [документация Git](https://git-scm.com/docs) и [GitHub Flow](https://docs.github.com/en/get-started/using-github/github-flow).

## Legacy materials / Исторические материалы

Earlier course notes and exercises remain in the repository during migration. They are preserved for traceability and are not treated as the current guide. Moving them into a dedicated legacy area will be a separate, reviewed change.

Ранние учебные конспекты и задания сохраняются в репозитории на время миграции. Они оставлены для прослеживаемости и не считаются актуальной версией руководства. Перенос в отдельный исторический раздел будет выполнен отдельным проверяемым изменением.

## License

MIT. See [LICENSE](LICENSE).
