# Git Push 推送指南

## 适用场景

当你已经完成本地修改，并准备把代码同步到远程仓库时，可以参考本文档中的标准流程。

## 提交并推送代码的基本步骤

### 1. 检查工作区状态

在进行任何提交前，先确认当前工作区有哪些修改：

```bash
git status
```

如果想用更精简的格式查看状态，可以使用：

```bash
git status --short
```

### 2. 添加修改到暂存区

使用 `git add` 将修改加入暂存区：

```bash
git add <file1> <file2>
```

如果要一次性添加当前目录下的全部修改，可以使用：

```bash
git add .
```

### 3. 再次确认暂存结果

添加完成后，建议再次执行状态检查，确认需要提交的内容已经进入暂存区：

```bash
git status
```

### 4. 提交到本地仓库

使用 `git commit` 创建本地提交：

```bash
git commit -m "docs: update git command guides"
```

如果省略 `-m` 参数，Git 会打开默认编辑器，让你输入更完整的提交信息。

### 5. 推送到远程仓库

将当前分支推送到远程仓库：

```bash
git push origin <branch>
```

例如：

```bash
git push origin main
```

如果是第一次推送当前分支，并希望建立上游分支关系，可以使用：

```bash
git push -u origin <branch>
```

## 常见检查命令

### 查看当前所在分支

```bash
git branch --show-current
```

### 查看远程仓库信息

```bash
git remote -v
```

## 注意事项

- 推送前尽量先执行 `git status`，避免把临时文件一并提交。
- 与他人协作时，推送前可以先执行 `git pull --rebase`，减少冲突概率。
- 如果远程拒绝推送，需要先同步远程最新提交，再重新推送。
