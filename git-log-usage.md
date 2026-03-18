# Git Log 使用指南

## 适用场景

当你需要查看提交历史、定位某次变更、分析分支关系或筛选某位作者的提交时，可以使用 `git log`。

## 基本命令

### 查看完整提交历史

```bash
git log
```

### 查看精简的一行日志

```bash
git log --oneline
```

### 查看图形化分支历史

```bash
git log --oneline --graph --decorate --all
```

这个命令非常适合观察分支合并关系。

## 常见过滤方式

### 查看最近 5 条提交

```bash
git log -n 5
```

### 按作者筛选

```bash
git log --author="Alice"
```

### 按时间筛选

```bash
git log --since="7 days ago"
```

### 查看某个文件的历史

```bash
git log -- <filename>
```

例如：

```bash
git log -- README.md
```

## 结合 diff 查看变更

### 查看每次提交的改动摘要

```bash
git log --stat
```

### 查看每次提交的具体内容

```bash
git log -p
```

## 推荐组合

日常开发中常用的历史查看命令：

```bash
git log --oneline --graph --decorate -n 10
```

## 注意事项

- `git log` 关注的是提交历史，不会展示未提交的工作区修改。
- 若想查看当前未提交的改动，应改用 `git status` 或 `git diff`。
