# Lesson 02 — Installing Git + First-Time Setup

Before we start tracking code, we need to install Git (the engine) and tell it who you are.
Every commit you make will be stamped with your identity (name and email).

## Learning Goals
By the end of this lesson, you will be able to:
- Install Git on Windows and Linux (Arch, Fedora)
- Verify Git is installed (`git --version`)
- Configure your name and email globally
- Set a default branch name (`main`)
- Set your default editor (VS Code example)
- Verify everything is saved correctly

## 1) Install Git

### Windows (Git for Windows)
1. Download Git for Windows from the official page: [git install link](https://git-scm.com/install/windows)
2. Run the installer and keep the default options (recommended).
3. After installation, open your terminal.
4. Verify:

```bash
git --version
```

You are done when you see a Git version printed.

---

### Linux (Arch Linux)
1. Update system packages:

```bash
sudo pacman -Syu
```

2. Install Git:

```bash
sudo pacman -S git
```

3. Verify:

```bash
git --version
```

---

### Linux (Fedora)
1. Optional but recommended: refresh packages:

```bash
sudo dnf upgrade --refresh
```

2. Install Git:

```bash
sudo dnf install git-all
```

3. Verify:

```bash
git --version
```

## 2) First-Time Identity Setup

Git needs to know who is making changes so commits are attributed correctly.

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

Tip: use the same email you use on GitHub (or a verified email).

## 3) Set Default Branch Name

Make new repositories use `main` by default:

```bash
git config --global init.defaultBranch main
```

## 4) Choose Your Default Editor

When Git needs a message (merge commits, rebases), it opens an editor.
If you do not set this, Git may open Vim.

### VS Code (recommended)

```bash
git config --global core.editor "code --wait"
```

If `code` does not work, enable it in VS Code:
Command Palette -> `Shell Command: Install 'code' command in PATH`

## 5) Verify Your Settings

```bash
git config --global --list
```

You should see:
- `user.name=...`
- `user.email=...`
- `init.defaultBranch=main`
- `core.editor=code --wait` (if set)

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 02 Task](../../excersises/setup/task.md)

## Navigation

- Previous: [Lesson 01 — Welcome](../welcome/README.md)
- Next: [Lesson 03 — Your First Repo](../first-repo/README.md)
