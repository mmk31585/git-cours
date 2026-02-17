# Lesson 13 — Team Workflow: Feature Branches + Reviews

This lesson turns individual Git usage into a repeatable team workflow.
The goal is a stable `main` branch and predictable collaboration.

## Learning Goals
By the end of this lesson, you will be able to:
- Explain a standard feature-branch workflow
- Keep commits small and reviewable
- Use PRs as the integration gate
- Coordinate review and merge responsibilities
- Avoid direct commits to `main` in team projects

## Simple Explanation
Team rule:
- branch -> commit -> push -> PR -> review -> merge

Why this works:
- protects `main`
- improves code quality
- makes changes easier to audit

## Workflow Checklist
1. Start from updated `main`
2. Create focused feature branch
3. Commit in small steps
4. Push branch and open PR
5. Request and address review
6. Merge after checks pass
7. Delete branch and sync local

## Key Commands
```bash
git switch main
git pull
git switch -c feature/<name>
git add .
git commit -m "feat: <change>"
git push -u origin feature/<name>
```

After merge:
```bash
git switch main
git pull
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 13 Task](../../exercises/team-workflow/task.md)

## Suggested Commit Messages
- `feat: add feature branch workflow doc`
- `docs: add PR checklist`
- `fix: address review feedback`

## Common Beginner Mistakes
- Working directly on `main`
- Opening PR with too many unrelated commits
- Skipping review because change feels small
- Merging with failing checks

## Navigation
- Previous: [Lesson 12 — Pull Requests 101](../pull-requests/README.md)
- Next: [Lesson 14 — Keeping Up to Date](../fetch-pull-rebase/README.md)
