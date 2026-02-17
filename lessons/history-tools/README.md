# Lesson 05 — Reading History Like a Pro: `log`, `diff`, `show`

In this lesson, you will learn how to inspect Git history like a developer: see what happened, what changed, and exactly what is inside a commit.

## Learning Goals
By the end of this lesson, you will be able to:
- Use `git log` to navigate commit history
- Use `git diff` to review changes before committing
- Use `git show` to inspect a specific commit
- Compare staged vs unstaged changes
- Debug faster by finding what changed and when

## Simple Explanation
Git gives you three core history tools:

### 1) `git log` -> "What happened?"
Shows the timeline of commits.

### 2) `git diff` -> "What changed?"
Shows line-by-line differences between versions.

### 3) `git show` -> "What is inside this commit?"
Shows one commit's details, including message and diff.

## Key Commands

### `git log` (history)
```bash
git log
git log --oneline
git log --oneline --graph --decorate --all
```

Pro tips:
- `--oneline` gives a compact view
- `--graph` visualizes branch structure
- `--decorate` shows branch and tag names

### `git diff` (changes)
```bash
git diff           # unstaged changes
git diff --staged  # staged changes (ready to commit)
```

### `git show` (inspect a commit)
```bash
git show          # latest commit
git show HEAD     # explicit latest commit
git show <hash>   # specific commit
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 05 Task](../../exercises/history-tools/task.md)

## Suggested Commit Messages
- `docs: add history file`
- `docs: add second line to history file`
- `docs: add lesson 05 notes (log/diff/show)`

## Common Beginner Mistakes
- Forgetting `git diff --staged` (staged and unstaged changes are different)
- Using only `git log` and never inspecting actual diffs
- Skipping diff review before commit, which leads to messy commits

## Navigation
- Previous: [Lesson 04 — The Three Areas](../three-area/README.md)
- Next: [Lesson 06 — Undo Basics (Safely)](../undo-safely/README.md)
