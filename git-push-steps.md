# Git Push Guide

## When to Use This Guide

Use this guide when you have finished local changes and want to publish them to a remote repository safely.

## Basic Push Workflow

### 1. Check the working tree

Always review your current repository state before creating a commit:

```bash
git status
```

If you prefer compact output, use:

```bash
git status --short
```

### 2. Stage the files you want to commit

Stage specific files:

```bash
git add <file1> <file2>
```

Or stage everything in the current directory:

```bash
git add .
```

### 3. Confirm the staged result

Run `git status` again to make sure only the intended changes are staged:

```bash
git status
```

### 4. Create a local commit

Create a commit with a clear message:

```bash
git commit -m "docs: update git command guides"
```

If you omit `-m`, Git opens your configured editor so you can write a longer message.

### 5. Push to the remote repository

Push the current branch to a remote:

```bash
git push origin <branch>
```

Example:

```bash
git push origin main
```

If this is the first push for the branch and you want to set upstream tracking:

```bash
git push -u origin <branch>
```

## Helpful Checks

### Show the current branch

```bash
git branch --show-current
```

### Show configured remotes

```bash
git remote -v
```

## Notes

- Run `git status` before pushing so you do not accidentally include temporary files.
- In collaborative repositories, `git pull --rebase` before pushing can reduce unnecessary merge commits.
- If the remote rejects your push, fetch or pull the latest remote changes first and resolve any conflicts.
