# Lesson 06 — Undo Basics (Safely): `restore`, `checkout`, `reset` vs `revert`

Mistakes happen, and Git gives you safe ways to undo work depending on where the mistake lives:
- in your files (working tree)
- in staging
- in commit history

This lesson covers the safest undo tools and when to use each one.

## Learning Goals
By the end of this lesson, you will be able to:
- Undo file changes safely with `git restore`
- Unstage files with `git restore --staged`
- Understand when `git reset` is safe (local only)
- Undo pushed commits safely with `git revert`
- Recover lost references using `git reflog`
- Explain rewriting history vs adding an undo commit

## Simple Mental Model
Undo depends on the level:

- Files not committed yet -> `git restore`
- Local commits not pushed -> `git reset`
- Pushed/shared commits -> `git revert`

Golden rule:
- If others may have pulled your commits, prefer `git revert` over `git reset`.

## 1) `git restore` — safe file-level undo

Discard unstaged changes:
```bash
git restore <file>
git restore .
```

Unstage a file but keep edits:
```bash
git restore --staged <file>
```

## 2) `git checkout` — older undo style
Older command:
```bash
git checkout -- <file>
```

Prefer modern commands:
- `git restore` for file undo
- `git switch` for branch switching

## 3) `git reset` — move branch pointer (can rewrite history)
Modes:
- `--soft`: keep changes staged
- `--mixed`: keep changes unstaged (default)
- `--hard`: discard changes completely (dangerous)

Undo last commit but keep staged changes:
```bash
git reset --soft HEAD~1
```

Undo last commit and keep edits unstaged:
```bash
git reset HEAD~1
```

Hard reset to current commit state:
```bash
git reset --hard HEAD
```

Use `reset` only for local commits that are not pushed.

## 4) `git revert` — safest undo for shared branches
`revert` creates a new commit that reverses an earlier commit:
```bash
git revert <commit-hash>
```

Best for:
- `main`
- pushed commits
- team collaboration

## Reset vs Revert (core difference)
- `reset` rewrites branch history
- `revert` preserves history and adds an explicit undo commit

## Recovery Tool: `git reflog`
If a commit seems lost, inspect previous HEAD positions:
```bash
git reflog
```

You can recover using a reflog reference:
```bash
git reset --hard <reflog-hash>
```

Use this carefully, but it is a key recovery tool.

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 06 Task](../../excersises/undo-safely/task.md)

## Suggested Commit Messages
- `docs: add undo basics notes`
- `fix: revert breaking change`
- `docs: clarify reset vs revert`

## Common Pitfalls
- Using `reset` after pushing shared commits
- Running `--hard` without understanding data loss risk
- Confusing staged vs unstaged undo paths

## Navigation
- Previous: [Lesson 05 — Reading History](../history-tools/README.md)
- Next: [Lesson 07 — Branching Fundamentals](../branching/README.md)
