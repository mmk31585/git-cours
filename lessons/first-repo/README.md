# Lesson 03 — Your First Repo

In this lesson, you will turn a normal folder into a Git repository and create your first commit (a checkpoint in history).

## Learning Goals
By the end of this lesson, you will be able to:
- Create a new Git repository with `git init`
- Understand what `git status` is showing
- Stage changes with `git add`
- Save checkpoints with `git commit`
- Use the core workflow: edit -> stage -> commit

## Simple Explanation
A Git repository (repo) is a project folder that Git tracks.

### The 4 commands you will use constantly
- `git init` -> start tracking a folder with Git
- `git status` -> see current changes and staging state
- `git add` -> choose what goes into the next commit
- `git commit` -> save a checkpoint with a message

Think of commits like save points in a game.

## Step-by-Step: Create Your First Repo

### 1) Make a new project folder
```bash
mkdir hello-git
cd hello-git
```

### 2) Initialize Git tracking
```bash
git init
```

### 3) Check repository status
```bash
git status
```

Expected result:
- You are on a branch (usually `main`)
- Git shows `No commits yet`
- Working tree is clean

## Create a File and Make Your First Commit

### 4) Create a README file
```bash
echo "# Hello Git" > README.md
```

### 5) Check status again
```bash
git status
```

Expected result:
- `README.md` appears as untracked

### 6) Stage the file
```bash
git add README.md
```

### 7) Commit staged changes
```bash
git commit -m "chore: initial commit"
```

### 8) Confirm everything is saved
```bash
git status
git log --oneline
```

Expected result:
- Working tree is clean
- One commit appears in history

---

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 03 Task](../../excersises/first-repo/task.md)

## Suggested Commit Messages
Good examples:
- `chore: initial commit`
- `docs: describe repository purpose`
- `docs: add notes file`
- `chore: add todo list`

Avoid vague messages like:
- `update`
- `final`
- `fix stuff`

## Common Beginner Mistakes
- Forgetting `git add` before `git commit`
- Using unclear commit messages
- Committing unrelated changes in one commit

## Navigation
- Previous: [Lesson 02 — Installing Git + Setup](../setup/README.md)
- Next: [Lesson 04 — The Three Areas](../three-area/README.md)
