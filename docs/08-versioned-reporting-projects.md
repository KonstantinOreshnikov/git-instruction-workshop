# Git for Versioned Analytics, Automation and QA Projects

Git is not just a backup or a way to upload files. It records **why a code, report definition, test or documentation change occurred**, lets reviewers compare revisions, and protects a working baseline.

## A generic project tree

```text
fictional-reporting-project/
├── README.md
├── data/demo_events.csv       # invented records only
├── src/validate.py            # example logic
├── tests/test_validate.py
├── docs/metric-contract.md
└── .gitignore
```

Exclude real extracts, credentials, caches, virtual environments and generated confidential reports using an appropriate `.gitignore`. **A .gitignore is not a substitute for reviewing staged files and history.**

## A safe branch workflow

```bash
git switch main
git pull --ff-only
git switch -c docs/explain-reconciliation
git status --short
git diff
git add README.md docs/metric-contract.md
git diff --cached
git commit -m "docs: explain synthetic reconciliation contract"
git push -u origin docs/explain-reconciliation
```

Open a pull request, record the expected behavior and actual QA evidence, request review and merge **only when authorized**. A commit does not automatically establish runtime correctness. A PR is a review boundary, not proof of deployment.

## What to version

| Artifact | Version in Git? | Rule |
|---|---|---|
| Synthetic exercises, reusable Python, shell scripts | Yes | Check code ownership and side effects |
| Documentation, test cases, metric contracts | Yes | Preserve effective periods and revisions |
| Empty schemas and mock data | Usually yes | Synthetic and non-reconstructive |
| Real extracts, client records, credentials | **No** | Keep in controlled systems, never public |
| Excel/PPTX templates | Only if rights allow | Binary diff and review limitations |
| Generated reports | Depends on disclosure and size | Avoid sensitive artifacts; consider release storage |

## Change example

Imagine the fictional completion-rate denominator incorrectly includes test events. The proper change is **not** to edit a percentage in a slide. Instead: document the corrected eligibility rule; update the calculation; add a failing regression test; regenerate the synthetic output; reconcile numerator and denominator; and document the difference in the PR.

## Review checklist

- Does the change preserve unrelated calculations and project files?
- Are all tracked files safe to publish, including images, logs and Git history?
- Does the PR explain its input contract and observed QA status?
- Are the link targets and any Mermaid diagrams valid?
- Does a failed runtime gate remain visibly FAILED or BLOCKED?

## Related learning

[Cross-track engineering map](https://github.com/KonstantinOreshnikov/git-markdown-practice) · [Python Learning Lab](https://github.com/KonstantinOreshnikov/python-lessons-geekbrains) · [Linux Automation Lab](https://github.com/KonstantinOreshnikov/linux-testing-python) · [Quality Engineering](https://github.com/KonstantinOreshnikov/web-testing-page-object).

**RU:** Git помогает управлять изменениями Python, SQL, методологии, QA и отчётности. Version control фиксирует исходную версию, diff, reviewer и доказательства тестов, но не заменяет сам тест.

Sources: [Pro Git](https://git-scm.com/book/en/v2), [GitHub Flow](https://docs.github.com/en/get-started/using-github/github-flow).
