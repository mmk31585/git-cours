# Lesson 09 — Handling Merge Conflicts (and Not Panicking)

Conflicts happen when Git cannot auto-merge two changes in the same area of a file.
This lesson shows a calm, repeatable process to resolve them safely.

## Learning Goals
By the end of this lesson, you will be able to:
- Explain what a merge conflict is
- Identify conflict markers in files
- Resolve conflicts and finish a merge
- Use `git status` to track conflict progress
- Avoid common conflict mistakes

## Simple Explanation
A conflict usually happens when:
- two branches changed the same lines
- one branch deleted a file the other edited

Git marks conflicts in files with:
- `<<<<<<<`
- `=======`
- `>>>>>>>`

Your job is to keep the correct final content, remove markers, then commit.

## Conflict Resolution Workflow
1. Start merge and detect conflict:
```bash
git switch main
git merge <branch>
```

2. Check conflicted files:
```bash
git status
```

3. Open each conflicted file and resolve markers manually.

4. Mark as resolved:
```bash
git add <resolved-file>
```

5. Finish merge:
```bash
git commit -m "fix: resolve merge conflict in <file>"
```

## Key Commands
```bash
git status
git merge <branch>
git add <file>
git commit
git merge --abort
```

Use `git merge --abort` if you want to cancel and return to pre-merge state.

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 09 Task](../../excersises/merge-conflicts/task.md)

## Suggested Commit Messages
- `fix: resolve merge conflict in README.md`
- `fix: resolve conflict in feature notes`
- `docs: explain merge conflict workflow`

## Common Beginner Mistakes
- Deleting the wrong lines while removing markers
- Forgetting to remove conflict markers before `git add`
- Resolving one file but forgetting others
- Panicking and force-resetting history

## Navigation
- Previous: [Lesson 08 — Merging Branches](../merging/README.md)
- Next: [Lesson 10 — GitHub Basics](../github-basics/README.md)
