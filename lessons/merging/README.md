# Lesson 08 — Merging Branches: Fast-Forward vs Merge Commit

In this lesson, you will learn how to combine a feature branch back into `main` using merge.
You will also understand the two common merge outcomes:
- Fast-forward merge (no extra merge commit)
- Merge commit (a new commit that joins both histories)

## Learning Goals
By the end of this lesson, you will be able to:
- Explain what merging does
- Merge a feature branch into `main`
- Understand fast-forward vs merge commit
- Force a merge commit with `--no-ff`
- Read merge history with `git log --graph`

## Simple Explanation
Merging means combining changes from one branch into another.

Typical flow:
- source branch: `feature/dark-mode`
- target branch: `main`

## 1) Fast-Forward Merge
When it happens:
- `main` has not moved since the feature branch was created
- Git can move the `main` pointer forward directly

Visual:
```text
main:    A
feature: A -- B -- C
merge -> main now points to C
```

Command:
```bash
git switch main
git merge feature/dark-mode
```

Result:
- clean linear history

## 2) Merge Commit
When it happens:
- both branches have new commits (histories diverged)
- Git creates a new merge commit with two parents

Visual:
```text
main:    A -- D
feature: A -- B -- C
merge -> A -- D -- M
              \    /
               B--C
```

Command:
```bash
git switch main
git merge feature/dark-mode
```

Result:
- history shows an explicit merge point

## 3) Force a Merge Commit (`--no-ff`)
Some teams always keep merge commits so branch integration points stay explicit.

```bash
git switch main
git merge --no-ff feature/dark-mode
```

## Key Commands
```bash
git merge <branch>                             # merge branch into current branch
git merge --no-ff <branch>                     # force merge commit
git log --oneline --graph --decorate --all     # visualize commit graph
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 08 Task](../../excersises/merging/task.md)

## Suggested Commit Messages
- `feat: add merge demo file`
- `feat: add no-ff demo file`
- `docs: explain fast-forward vs merge commit`

## Common Beginner Mistakes
- Merging into the wrong branch (check `git status` first)
- Forgetting to sync `main` before merging in team projects
- Assuming no merge commit means failure (it may be fast-forward)

## Navigation
- Previous: [Lesson 07 — Branching Fundamentals](../branching/README.md)
- Next: [Lesson 09 — Handling Merge Conflicts](../merge-conflicts/README.md)
