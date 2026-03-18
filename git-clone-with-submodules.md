# Git Clone with Submodules

## When to Use This Guide

Use this guide when a repository includes Git submodules. A normal `git clone` fetches the main repository, but submodule directories may remain empty until they are initialized.

## 1. Clone and initialize submodules immediately

The recommended approach is to clone with `--recurse-submodules`:

```bash
git clone --recurse-submodules <repository_url>
```

Example:

```bash
git clone --recurse-submodules https://github.com/zalebool/git-frequent-commands.git
```

## 2. Initialize submodules after cloning

If the repository is already cloned, enter the project and initialize submodules manually:

```bash
cd <repository_name>
git submodule update --init --recursive
```

Example:

```bash
cd git-frequent-commands
git submodule update --init --recursive
```

## 3. Check submodule status

Use this command to verify that submodules are initialized correctly:

```bash
git submodule status
```

## 4. Update submodules

If submodule references have changed or you want to pull newer upstream content for them, run:

```bash
git submodule update --remote --merge
```

## Other Common Operations

### Add a new submodule

```bash
git submodule add <repository_url> <path>
git commit -m "Add new submodule <submodule_name>"
```

### Remove a submodule

```bash
git submodule deinit -f <path_to_submodule>
git rm -f <path_to_submodule>
rm -rf .git/modules/<path_to_submodule>
git commit -m "Remove submodule <submodule_name>"
```

## Notes

- After pulling updates from the main repository, run `git submodule update --init --recursive` if submodule references changed.
- Git stores submodule commit references, not a full copy of the submodule contents inside the parent repository.
