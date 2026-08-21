# Remotes, Forks and Pull Requests / Remotes, forks и pull requests

## English

### Remote basics

```bash
git remote -v
git remote add origin https://github.com/USER/REPOSITORY.git
git fetch origin
git push -u origin main
```

`git fetch` downloads remote references without integrating them into the current branch. `git pull` fetches and then integrates changes using the configured strategy.

### Direct collaboration

When you have write access:

1. create a branch;
2. commit and push the branch;
3. open a pull request;
4. address review comments and checks;
5. merge after approval.

### Fork workflow

When you do not have write access:

1. fork the upstream repository;
2. clone your fork;
3. add the original repository as `upstream`;
4. create a branch and push it to your fork;
5. open a pull request from the fork to upstream.

```bash
git clone https://github.com/YOUR-USER/PROJECT.git
cd PROJECT
git remote add upstream https://github.com/ORIGINAL-OWNER/PROJECT.git
git fetch upstream
```

### Pull-request checklist

- descriptive title;
- problem and scope;
- concise change summary;
- validation performed;
- screenshots only when they materially help;
- linked issue when applicable;
- no secrets or unrelated changes.

## Русский

### Основы удалённых репозиториев

`git fetch` загружает удалённые ссылки, но не объединяет их с текущей веткой. `git pull` выполняет fetch, а затем интегрирует изменения в соответствии с настроенной стратегией.

### Совместная работа с правом записи

1. создайте ветку;
2. зафиксируйте и отправьте изменения;
3. откройте pull request;
4. исправьте замечания и пройдите проверки;
5. выполните merge после одобрения.

### Работа через fork

Если права записи отсутствуют, создайте fork, клонируйте свою копию, добавьте исходный репозиторий как `upstream`, работайте в отдельной ветке и откройте PR из fork в upstream.

Pull request должен иметь понятный заголовок, описание задачи и scope, список проверок и только относящиеся к задаче изменения. Secrets и случайные файлы в PR недопустимы.

Sources / Источники: [GitHub pull requests](https://docs.github.com/en/pull-requests), [GitHub Flow](https://docs.github.com/en/get-started/using-github/github-flow)

