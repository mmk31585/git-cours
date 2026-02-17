# Lesson 18 — `.gitignore` + Repo Hygiene: What Not to Commit

Clean repositories are easier to review, build, and secure.
This lesson focuses on ignoring generated files and secrets.

## Learning Goals
By the end of this lesson, you will be able to:
- Explain what `.gitignore` does
- Add common ignore patterns
- Stop tracking files that should not be versioned
- Protect secrets from accidental commits

## Simple Explanation
`.gitignore` tells Git which files/folders to ignore.

Common examples:
- dependency folders (`node_modules/`)
- build outputs (`dist/`, `bin/`)
- local secrets (`.env`)
- editor/system files

Important:
- `.gitignore` does not remove files already tracked

## Key Commands
```bash
echo "node_modules/" >> .gitignore
echo ".env" >> .gitignore
git add .gitignore
git commit -m "chore: add .gitignore"
```

Stop tracking file already committed:
```bash
git rm --cached <file>
git commit -m "chore: stop tracking <file>"
```

## Practice Exercise
Complete the lesson practice in:

- [Exercise: Lesson 18 Task](../../excersises/gitignore-hygiene/task.md)

## Suggested Commit Messages
- `chore: add .gitignore`
- `security: remove tracked env file`
- `chore: clean generated files from repo`

## Common Beginner Mistakes
- Committing `.env` files
- Assuming `.gitignore` removes tracked files automatically
- Ignoring too broadly and hiding important source files

## Navigation
- Previous: [Lesson 17 — Tagging + Releases](../tagging-releases/README.md)
- Next: [Lesson 19 — GitHub Collaboration Tools](../collaboration-tools/README.md)
