# Lesson 07 — Branching Fundamentals: Creating and Switching Branches

Branches are one of Git's most useful features. They let you work on features, fixes, and experiments without changing the stable `main` branch.

## Learning Goals
By the end of this lesson, you will be able to:
- Explain what a branch is and why teams use branches
- Create a new branch
- Switch between branches
- Make commits on a branch
- Understand what `HEAD` points to
- Follow a simple feature-branch workflow

## Simple Explanation
A branch is a separate timeline of your project.  
You create a branch to work safely, then merge it back into `main` later.

Why branches matter:
- Build features without breaking `main`
- Test and experiment safely
- Collaborate through pull requests

What is `HEAD`?
- `HEAD` points to the branch/commit you are currently on.
- When you switch branches, `HEAD` moves.

## Key Commands
```bash
git branch                 # list branches
git switch -c <branch>     # create + switch (recommended)
git switch <branch>        # switch branches

# older (still common)
git checkout -b <branch>   # create + switch
git checkout <branch>      # switch
```

Check your current branch:
```bash
git status
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 07 Task](../../excersises/branching/task.md)

## Best Practice: Branch naming
Good branch names:
- `feature/dark-mode`
- `fix/login-bug`
- `docs/readme-improvements`

Avoid vague names:
- `test`
- `new`
- `branch1`

## Suggested Commit Messages
- `feat: add dark mode draft`
- `docs: add branching lesson notes`
- `chore: add features folder`

## Common Beginner Mistakes
- Doing all work on `main`
- Forgetting to switch branches before committing
- Using unclear branch names
- Putting unrelated work in one branch

## Navigation
- Previous: [Lesson 06 — Undo Basics](../undo-safely/README.md)
- Next: [Lesson 08 — Merging Branches](../merging/README.md)
