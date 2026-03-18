# Git Status Guide

## When to Use This Guide

Use `git status` whenever you want to see which files changed, which changes are staged, and which branch you are currently on.

## Basic Commands

### Show the full repository status

```bash
git status
```

This command shows:

- the current branch
- modified files that are not staged yet
- staged files that are ready to commit
- untracked files

### Show a compact status view

```bash
git status --short
```

Common status markers include:

- `M`: modified file
- `A`: added to the staging area
- `D`: deleted file
- `??`: untracked file

### Show branch and short status together

```bash
git status -sb
```

This is useful for quick daily checks because it shows both the branch name and a compact list of file changes.

## Common Scenarios

### Review changes before committing

```bash
git status
```

This helps confirm that you are committing only the files you intended.

### Confirm staged files after `git add`

```bash
git status
```

Use this to make sure changes moved from unstaged output into the staged section.

### Check untracked files before cleaning up

```bash
git status --short
```

This is especially useful before running `git clean`, switching branches, or creating a commit.

## Notes

- `git status` does not show line-by-line differences; use `git diff` for that.
- Running `git status` often helps prevent accidental commits.
