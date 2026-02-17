# Lesson 11 — Connecting Local to GitHub: `remote`, `push`, `pull`

In this lesson, you connect your local repository to GitHub and sync changes both directions.

## Learning Goals
By the end of this lesson, you will be able to:
- Explain what a remote is
- Add and verify `origin`
- Push local branches to GitHub
- Pull remote changes safely
- Understand upstream tracking (`-u`)

## Simple Explanation
A remote is an online copy of your repository.

Most projects use:
- `origin` as the primary GitHub remote

Direction of sync:
- `push`: local -> remote
- `pull`: remote -> local

## Key Commands
```bash
git remote -v
git remote add origin <repo-url>
git push -u origin main
git pull
git fetch origin
```

Useful checks:
```bash
git branch -vv
git status
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 11 Task](../../excersises/remote-push-pull/task.md)

## Suggested Commit Messages
- `docs: add remote setup notes`
- `chore: connect local repo to origin`
- `docs: add push and pull workflow`

## Common Beginner Mistakes
- Adding wrong remote URL
- Forgetting `-u` on first push
- Pulling without checking local uncommitted changes
- Pushing to wrong branch

## Navigation
- Previous: [Lesson 10 — GitHub Basics](../github-basics/README.md)
- Next: [Lesson 12 — Pull Requests 101](../pull-requests/README.md)
