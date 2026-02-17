# Exercise — Lesson 02: Installing Git + Setup

Practice goal: confirm Git is installed and your global identity/config are saved correctly.

---

## Task 1: Verify installation
```bash
git --version
```

## Task 2: Check your global identity
```bash
git config --global --get user.name
git config --global --get user.email
```

If missing, set them:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## Task 3: Check branch and editor defaults
```bash
git config --global --get init.defaultBranch
git config --global --get core.editor
```

If missing, set them:
```bash
git config --global init.defaultBranch main
git config --global core.editor "code --wait"
```

## Task 4: Save setup notes
```bash
mkdir -p notes
cat > notes/lesson-02.md << 'EOF'
## Lesson 02 Notes
- Git version:
- user.name:
- user.email:
- default branch:
- editor:
EOF
```

Fill values using:
```bash
git --version
git config --global --get user.name
git config --global --get user.email
git config --global --get init.defaultBranch
git config --global --get core.editor
```

---

## Expected Result
- Git is installed
- Global identity is configured
- `main` and editor defaults are configured
- `notes/lesson-02.md` is filled with your values

## Self-Check
- [ ] `git --version` works
- [ ] `user.name` and `user.email` are set
- [ ] `init.defaultBranch` is `main`
- [ ] I recorded setup details in `notes/lesson-02.md`
