# Lesson 21 — Mini Project: Full Workflow Simulation

This mini project combines everything from branching to PR review and merge.
Treat it like a small real-world team sprint.

## Learning Goals
By the end of this lesson, you will be able to:
- Run an end-to-end branch and PR workflow
- Coordinate issue tracking with implementation
- Handle review feedback and merge cleanly
- Document outcomes in commit history

## Project Scenario
You have one small feature request tracked by an issue.
One person implements on a branch, another reviews and merges.

## Workflow Steps
1. Create an issue
2. Create feature branch
3. Implement and commit in small steps
4. Push branch
5. Open PR linked to issue
6. Review and request updates if needed
7. Merge and delete branch
8. Pull latest `main`

## Key Commands
```bash
git switch main
git pull
git switch -c feature/mini-project
git add .
git commit -m "feat: implement mini project task"
git push -u origin feature/mini-project
```

After merge:
```bash
git switch main
git pull
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 21 Task](../../exercises/mini-project/task.md)

## Suggested Commit Messages
- `feat: add mini project feature`
- `fix: apply review feedback`
- `docs: update mini project notes`

## Common Beginner Mistakes
- Trying to complete everything in one huge commit
- Opening PR without context or issue reference
- Forgetting post-merge sync

## Navigation
- Previous: [Lesson 20 — Best Practices](../best-practices/README.md)
- Next: [Lesson 22 — Wrap-Up + Next Steps](../wrap-up/README.md)
