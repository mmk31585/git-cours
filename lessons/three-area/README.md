# Lesson 04 — Understanding the Three Areas: Working Tree, Staging, Repository

In this lesson, you will learn the core mental model that makes Git easier: changes move through three areas, and you control each step.

## Learning Goals
By the end of this lesson, you will be able to:
- Explain the difference between Working Tree, Staging Area, and Repository
- Use `git status` to see where your changes are
- Stage only what you want with `git add`
- Unstage safely with `git restore --staged`
- Create clean commits (for example, bug fixes separate from features)

## Simple Explanation (The 3 Areas)

### 1) Working Tree
This is your project folder right now, where you edit files.

Changes here are not saved in Git history yet.

Example: you open `app.js` and change code. That change is in the Working Tree.

---

### 2) Staging Area (Index)
This is Git's preview box for the next commit.
You choose exactly which changes should go into the next checkpoint.

Move changes here with:

```bash
git add <file>
```

---

### 3) Repository (History)
This is the permanent commit history stored in `.git/`.

Save staged changes here with:

```bash
git commit -m "message"
```

## Workflow (Always)

Edit -> Stage -> Commit

- Edit files in the Working Tree
- Stage selected changes in the Staging Area
- Commit staged changes to the Repository

## Key Commands

```bash
git status                  # shows where changes are
git add <file>              # working tree -> staging
git add .                   # stage everything in current folder
git restore --staged <file> # staging -> working tree (unstage)
git commit -m "message"     # staging -> repository
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 04 Task](../../excersises/three-area/task.md)

## Suggested Commit Messages
- `docs: explain git three areas`
- `docs: add demo file`
- `fix: add bugfix note`
- `feat: add feature draft`

## Common Beginner Mistakes
- Running `git add .` without checking what gets included
- Mixing unrelated changes into one commit
- Forgetting that staging is a filter before commit

## Navigation
- Previous: [Lesson 03 — Your First Repo](../first-repo/README.md)
- Next: [Lesson 05 — Reading History Like a Pro](../history-tools/README.md)
