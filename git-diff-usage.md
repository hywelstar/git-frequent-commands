# git-diff-usage

## Git diff 使用指南

Git Diff 命令用于比较文件之间的差异。

## 比较工作区与暂存区

可以使用以下命令比较当前工作区与暂存区的差异：

```bash
git diff
```

## 比较暂存区与最新提交

比较暂存区与最新提交之间的差异：

```bash
git diff --cached
```

## 比较两个提交之间的差异

可以通过指定两个提交的哈希值来比较它们之间的差异：

```bash
git diff <commit1> <commit2> -- <filename>
```

其中 `<commit1>` 和 `<commit2>` 是提交的哈希值，`<filename>` 是要比较的文件名。

## 示例

比较两个提交之间的差异示例：

```bash
git diff 85384f86df3d1375f851f4ea25d94d25fa501e0b a6be2f86357f008737c2bab37c85a434ecca4dfd -- git-clone-with-submodules.md
```

这会显示出两个提交之间在 `git-clone-with-submodules.md` 文件中的具体差异内容。
