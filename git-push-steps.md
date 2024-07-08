# git-push-setps

## Git push 推送指南

提交代码到版本控制系统（如 Git）通常涉及以下基本步骤：

### 提交代码的步骤

1. **工作目录状态检查**：
   - 在进行任何更改之前，建议先检查工作目录的状态，确认当前的修改状态。

   ```bash
   git status
   ```

2. **添加修改到暂存区**：
   - 使用 `git add` 命令将修改或新增的文件添加到 Git 的暂存区（Staging Area）。

   ```bash
   git add <file1> <file2> ...    # 添加指定文件
   git add .                      # 添加所有修改的文件
   ```

3. **确认更改**：
   - 使用 `git status` 再次确认修改已经添加到了暂存区。

   ```bash
   git status
   ```

4. **提交到本地仓库**：
   - 使用 `git commit` 命令将暂存区中的文件提交到本地仓库，并附带提交信息。

   ```bash
   git commit -m "Your commit message"
   ```

   - 如果省略 `-m` 参数，Git 将会打开默认文本编辑器（如 Vim 或 Nano），以便你输入详细的提交信息。

5. **推送到远程仓库（可选）**：
   - 如果是首次推送或者需要同步更新到远程仓库，可以使用 `git push` 命令将本地提交推送到远程仓库。

   ```bash
   git push origin <branch>
   ```

   - `<branch>` 是指要推送的分支名称，通常是 `main` 或 `master`。