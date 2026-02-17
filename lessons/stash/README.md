# Lesson 16 — Stash for Context Switching

Sometimes you need to pause unfinished work and switch tasks quickly.
`git stash` lets you store work in progress without committing it.

## Learning Goals
By the end of this lesson, you will be able to:
- Explain what stash is used for
- Save work in progress with a stash
- List and inspect stashes
- Restore stashed work with `pop` or `apply`
- Decide when stash is better than a temporary commit

## Simple Explanation
A stash is a temporary shelf for uncommitted changes.

Use it when:
- urgent task appears
- your changes are not ready to commit
- you need a clean working tree to switch branches

## Key Commands
```bash
git stash
git stash push -m "wip: message"
git stash list
git stash show -p stash@{0}
git stash pop
git stash apply stash@{0}
git stash drop stash@{0}
```

Include untracked files:
```bash
git stash -u
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 16 Task](../../excersises/stash/task.md)

## Suggested Commit Messages
- `docs: add stash workflow notes`
- `chore: stash context-switch examples`

## Common Beginner Mistakes
- Forgetting what each stash contains
- Using stash as long-term storage
- Popping onto incompatible branch without checking

## Navigation
- Previous: [Lesson 15 — Rebase vs Merge](../rebase-vs-merge/README.md)
- Next: [Lesson 17 — Tagging + Releases](../tagging-releases/README.md)
