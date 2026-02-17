# Exercise — Lesson 18: `.gitignore` and Hygiene

Practice goal: create a practical `.gitignore` and clean tracked noise files.

## Part A: Add ignore patterns
1. Update `.gitignore`:
```bash
echo "node_modules/" >> .gitignore
echo ".env" >> .gitignore
echo "dist/" >> .gitignore
```

2. Commit:
```bash
git add .gitignore
git commit -m "chore: add repo hygiene ignore rules"
```

## Part B: Stop tracking a file
If a sensitive/generated file is already tracked:
```bash
git rm --cached <file>
git commit -m "security: stop tracking <file>"
```

## Part C: Verify ignore behavior
```bash
git status
```

Create ignored file and confirm it does not appear:
```bash
echo "SECRET=demo" > .env
git status
```

## Self-Check
- [ ] `.gitignore` contains key patterns
- [ ] I untracked a file with `git rm --cached`
- [ ] Ignored files no longer appear in normal status output
