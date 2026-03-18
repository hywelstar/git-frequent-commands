# Git Installation Guide

## When to Use This Guide

Use this guide when you are setting up Git on a new machine or helping a teammate get started quickly.

## Windows

Download Git from [Git for Windows](https://gitforwindows.org/). After installation, open Git Bash or a terminal and verify the installation:

```bash
git --version
```

## macOS

If Homebrew is available, install Git with:

```bash
brew install git
```

Then verify the installation:

```bash
git --version
```

## Ubuntu / Debian

### 1. Update package metadata

```bash
sudo apt update
```

### 2. Install Git

```bash
sudo apt install git
```

### 3. Confirm Git is available

```bash
git --version
```

## Recommended Next Step

After installing Git, configure your identity so future commits have the correct author information:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

You can continue with `git-config-usage.md` for more configuration examples.
