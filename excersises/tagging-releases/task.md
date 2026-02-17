# Exercise — Lesson 17: Tagging and Releases

Practice goal: create and push annotated release tags.

## Part A: Create release commit
```bash
echo "release prep" > release-notes.md
git add release-notes.md
git commit -m "chore: prepare release notes"
```

## Part B: Create annotated tag
```bash
git tag -a v0.1.0 -m "Initial workshop release"
git tag
```

Inspect tag:
```bash
git show v0.1.0
```

## Part C: Push tag
```bash
git push origin v0.1.0
```

Optional push all tags:
```bash
git push origin --tags
```

## Self-Check
- [ ] I created annotated tag `v0.1.0`
- [ ] I inspected tag details
- [ ] I pushed the tag to remote
