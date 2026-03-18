# Git Config Guide

## When to Use This Guide

Use `git config` when you are setting up Git for the first time, moving to a new machine, or standardizing your local workflow.

## Inspect Existing Configuration

### List all configuration values

```bash
git config --list
```

### Show where each configuration came from

```bash
git config --list --show-origin
```

This helps you tell whether a value comes from the system, global, or repository-level config.

## Common Settings

### Set your name

```bash
git config --global user.name "Your Name"
```

### Set your email

```bash
git config --global user.email "you@example.com"
```

### Set the default editor

```bash
git config --global core.editor "vim"
```

### Set the default initial branch name

```bash
git config --global init.defaultBranch main
```

## Global vs. Repository-Level Settings

- `--global` applies to all repositories for the current user.
- Omitting `--global` applies the setting only to the current repository.

For example, to use a different email in only one repository:

```bash
git config user.email "project@example.com"
```

## Useful Aliases

### Add a compact log alias

```bash
git config --global alias.lg "log --oneline --graph --decorate --all"
```

### Add a short status alias

```bash
git config --global alias.st status
```

Then you can use:

```bash
git lg
git st
```

## Notes

- In team projects, keep your Git username and email aligned with your hosting platform account.
- If you create a commit with the wrong author information, update the config and recreate or amend the commit.
