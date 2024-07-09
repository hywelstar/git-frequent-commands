# git-branch-operations.md

## Git 分支操作指南

在 Git 中，分支操作涉及到创建、切换、查看、合并和删除等几个主要的操作。下面是这些操作的具体步骤和命令：

### 1. 创建分支

创建一个新的分支，通常基于当前所在的分支（如 `master` 或 `main`）：

```bash
git branch <branch-name>
```

例如，创建名为 `feature/new-feature` 的分支：

```bash
git branch feature/new-feature
```

### 2. 切换分支

切换到已存在的分支：

```bash
git checkout <branch-name>
```

或者，使用 `git switch` 命令（推荐使用 `git switch` 替代 `git checkout`）：

```bash
git switch <branch-name>
```

例如，切换到 `feature/new-feature` 分支：

```bash
git switch feature/new-feature
```

### 3. 查看分支

查看当前仓库中所有的分支及其状态：

```bash
git branch
```

添加 `-a` 选项可以查看所有本地和远程分支：

```bash
git branch -a
```

### 4. 合并分支

将指定分支的更改合并到当前分支：

首先切换到要接受更改的目标分支，例如 `main` 分支：

```bash
git switch main
```

然后执行合并操作：

```bash
git merge <branch-to-merge>
```

### 5. 删除分支

删除指定的本地分支：

```bash
git branch -d <branch-name>
```

如果要强制删除（即使分支上的更改没有合并到其他分支），使用 `-D` 选项：

```bash
git branch -D <branch-name>
```

### 6. 查看分支历史

查看分支的提交历史和分支图：

```bash
git log --graph --oneline --all
```

这会显示所有分支的提交历史，并以图形方式展示分支之间的关系。

### 7. 推送分支到远程仓库

如果需要将新创建的分支推送到远程仓库：

```bash
git push origin <branch-name>
```

例如，将 `feature/new-feature` 分支推送到远程仓库：

```bash
git push origin feature/new-feature
```

这些基本的分支操作命令能够帮助你有效地管理和使用 Git 中的分支，从而更好地组织和协调项目的开发流程。