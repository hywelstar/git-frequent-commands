# Git Log Guide

## When to Use This Guide

Use `git log` when you need to inspect commit history, trace a change, understand branch relationships, or filter commits by author or date.

## Basic Commands

### Show the full history

```bash
git log
```

### Show a compact one-line history

```bash
git log --oneline
```

### Show a graph of branch history

```bash
git log --oneline --graph --decorate --all
```

This is especially helpful when you want to understand merges and parallel branch development.

## Common Filters

### Show the most recent 5 commits

```bash
git log -n 5
```

### Filter by author

```bash
git log --author="Alice"
```

### Filter by time range

```bash
git log --since="7 days ago"
```

### Show history for one file

```bash
git log -- <filename>
```

Example:

```bash
git log -- README.md
```

## Combine Log with Diff Output

### Show a summary of changed files per commit

```bash
git log --stat
```

### Show patch details for each commit

```bash
git log -p
```

## A Handy Everyday Command

A common log command for day-to-day work is:

```bash
git log --oneline --graph --decorate -n 10
```

## Notes

- `git log` shows committed history, not uncommitted working tree changes.
- To inspect uncommitted changes, use `git status` or `git diff` instead.
