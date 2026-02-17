# Lesson 15 — Rebase vs Merge: When to Use Which

Both rebase and merge integrate changes, but they create different history shapes.
This lesson helps you choose the right tool for the right context.

## Learning Goals
By the end of this lesson, you will be able to:
- Explain difference between merge and rebase
- Choose merge or rebase for common scenarios
- Rebase a local branch safely
- Avoid rewriting shared public history

## Simple Explanation
Merge:
- combines histories with a merge commit
- preserves exact branch topology

Rebase:
- rewrites commit base for linear history
- cleaner log, but changes commit IDs

## When to Use
Use merge when:
- branch is shared
- you want explicit integration points
- preserving historical shape matters

Use rebase when:
- branch is local/private
- you want a clean linear sequence before PR

## Key Commands
```bash
git merge main
git rebase main
git rebase --continue
git rebase --abort
```

Visualize result:
```bash
git log --oneline --graph --decorate --all
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 15 Task](../../excersises/rebase-vs-merge/task.md)

## Suggested Commit Messages
- `docs: compare rebase and merge`
- `docs: add integration strategy notes`
- `fix: resolve rebase conflict`

## Common Beginner Mistakes
- Rebasing commits already pushed to shared branch
- Force-pushing rewritten history without coordination
- Assuming linear history is always better than explicit merges

## Navigation
- Previous: [Lesson 14 — Keeping Up to Date](../fetch-pull-rebase/README.md)
- Next: [Lesson 16 — Stash for Context Switching](../stash/README.md)
