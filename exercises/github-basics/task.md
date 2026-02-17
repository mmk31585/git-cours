# Exercise — Lesson 10: GitHub Basics

Practice goal: create a clean GitHub repository with essential collaboration files.

## Part A: Create repository (GitHub UI)
1. Create a new GitHub repository.
2. Add a README during setup.
3. Choose a license (for example MIT).

## Part B: Add project planning basics
1. Create 3 Issues:
- one bug
- one feature
- one docs task

2. Add labels such as:
- `bug`
- `feature`
- `docs`

## Part C: Connect local repository
1. In your local project, verify branch and connect remote:
```bash
git branch
git remote add origin <repo-url>
git push -u origin main
```
If your branch is not `main`, replace `main` with your branch name.
If you see `remote origin already exists`, run:
```bash
git remote set-url origin <repo-url>
```

2. Verify remote and push result:
```bash
git remote -v
git log origin/main --oneline -n 3
```
Also verify in GitHub UI that your files are visible.

## Self-Check
- [ ] I created a GitHub repository
- [ ] Repository has README and LICENSE
- [ ] I created and labeled issues
- [ ] Local `main` is pushed to `origin`
- [ ] I can see my files on GitHub
