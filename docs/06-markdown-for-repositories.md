# Markdown for Repositories / Markdown для репозиториев

## English

Repository documentation should help a new reader answer five questions:

1. What is this project?
2. Why does it exist?
3. How do I run or use it?
4. What is included?
5. What are the limitations and license?

### Common syntax

```markdown
# Main heading
## Section

**Bold text** and *italic text*

- unordered item
1. ordered item

[Descriptive link](https://example.com)
![Useful alternative text](path/to/image.png)

> A short quotation or important note.

| Column A | Column B |
|---|---|
| Value 1 | Value 2 |

`inline code`
```

Use fenced code blocks with a language identifier:

````markdown
```bash
git status
```
````

Prefer descriptive link text over “click here.” Add meaningful alternative text to images. Keep heading levels hierarchical and preview the rendered document before publishing.

## Русский

Документация репозитория должна отвечать новому читателю на пять вопросов:

1. Что это за проект?
2. Зачем он создан?
3. Как его запустить или использовать?
4. Что входит в состав?
5. Какие есть ограничения и лицензия?

Используйте понятные названия ссылок вместо «нажмите здесь», добавляйте содержательный альтернативный текст к изображениям, соблюдайте иерархию заголовков и проверяйте rendered preview перед публикацией.

Для блоков кода указывайте язык — например, `bash`, `python` или `sql`. Это улучшает читаемость и подсветку синтаксиса.

Source / Источник: [GitHub basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
