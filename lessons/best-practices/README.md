# Lesson 20 — Best Practices + Common Pitfalls (Real-World Checklist)

This lesson consolidates practical habits that keep repositories healthy over time.

## Learning Goals
By the end of this lesson, you will be able to:
- Apply a reliable daily Git workflow
- Write clear commit messages
- Avoid high-risk mistakes on shared branches
- Build habits that improve review quality

## Practical Best Practices
- Commit often with focused scope
- Pull before you push
- Keep branches short-lived
- Prefer PR review for shared code
- Use meaningful commit messages
- Avoid committing secrets or generated noise

## Pre-Push Checklist
Before pushing:
- run `git status`
- inspect `git diff --staged`
- verify target branch
- ensure commit messages are clear

## Key Commands
```bash
git status
git diff
git diff --staged
git log --oneline -n 10
git pull --rebase
git push
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 20 Task](../../exercises/best-practices/task.md)

## Suggested Commit Messages
- `docs: add git best-practices checklist`
- `docs: add pre-push review steps`
- `chore: clean commit history`

## Common Pitfalls
- Vague commits (`update`, `fix stuff`)
- Very large PRs with mixed concerns
- Force-pushing shared branches without coordination
- Merging without understanding change impact

## Navigation
- Previous: [Lesson 19 — GitHub Collaboration Tools](../collaboration-tools/README.md)
- Next: [Lesson 21 — Mini Project Workflow](../mini-project/README.md)
