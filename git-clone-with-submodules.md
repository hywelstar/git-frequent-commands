# Git Clone 子模块指南

## 适用场景

当仓库包含 Git Submodule 时，普通的 `git clone` 只会拉取主仓库内容，子模块目录可能为空。此时应使用本文档中的方式进行克隆与初始化。

## 1. 克隆仓库并自动初始化子模块

推荐直接使用 `--recurse-submodules` 参数：

```bash
git clone --recurse-submodules <repository_url>
```

例如：

```bash
git clone --recurse-submodules https://github.com/zalebool/git-frequent-commands.git
```

## 2. 已克隆仓库后再初始化子模块

如果仓库已经克隆完成，但子模块尚未初始化，可以进入仓库后执行：

```bash
cd <repository_name>
git submodule update --init --recursive
```

例如：

```bash
cd git-frequent-commands
git submodule update --init --recursive
```

## 3. 确认子模块状态

可以使用以下命令查看子模块是否已成功初始化：

```bash
git submodule status
```

## 4. 更新子模块

当子模块引用发生变化，或者需要拉取子模块远程最新内容时，可以执行：

```bash
git submodule update --remote --merge
```

## 其他常见操作

### 添加新子模块

```bash
git submodule add <repository_url> <path>
git commit -m "Add new submodule <submodule_name>"
```

### 移除子模块

```bash
git submodule deinit -f <path_to_submodule>
git rm -f <path_to_submodule>
rm -rf .git/modules/<path_to_submodule>
git commit -m "Remove submodule <submodule_name>"
```

## 注意事项

- 拉取主仓库更新后，如果子模块引用变动，通常还需要再次执行 `git submodule update --init --recursive`。
- 提交含有子模块的项目时，Git 记录的是子模块提交引用，而不是子模块目录的全部文件内容。
