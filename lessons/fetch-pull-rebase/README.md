# Lesson 14 — Keeping Up to Date: `fetch`, `pull`, and Rebase Basics

Teams move fast. This lesson teaches how to sync safely with remote changes.

## Learning Goals
By the end of this lesson, you will be able to:
- Explain `fetch` vs `pull`
- Use `pull --rebase` for cleaner local history
- Update your feature branch before opening PR
- Resolve basic rebase interruptions safely

## Simple Explanation
`git fetch`:
- downloads remote updates
- does not change your working branch

`git pull`:
- fetch + integrate in one step

`git pull --rebase`:
- replays your local commits on top of updated remote base
- often keeps history cleaner than merge-based pull

## Key Commands
```bash
git fetch origin
git pull
git pull --rebase
git rebase --continue
git rebase --abort
```

Useful checks:
```bash
git status
git log --oneline --graph --decorate --all
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 14 Task](../../exercises/fetch-pull-rebase/task.md)

## Suggested Commit Messages
- `docs: explain fetch vs pull`
- `docs: add pull --rebase workflow`
- `fix: resolve rebase interruption`

## Common Beginner Mistakes
- Pulling without checking uncommitted local changes
- Rebasing public/shared branches
- Forgetting to run tests after integrating upstream updates

## Navigation
- Previous: [Lesson 13 — Team Workflow](../team-workflow/README.md)
- Next: [Lesson 15 — Rebase vs Merge](../rebase-vs-merge/README.md)
