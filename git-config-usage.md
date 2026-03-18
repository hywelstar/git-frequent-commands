# Git Config 使用指南

## 适用场景

当你首次安装 Git、切换开发设备，或者想统一提交身份与常用工具时，可以通过 `git config` 完成配置。

## 查看当前配置

### 查看所有配置

```bash
git config --list
```

### 区分配置来源

```bash
git config --list --show-origin
```

这有助于判断某个配置来自系统级、全局级还是当前仓库。

## 常见配置项

### 配置用户名

```bash
git config --global user.name "Your Name"
```

### 配置邮箱

```bash
git config --global user.email "you@example.com"
```

### 设置默认编辑器

```bash
git config --global core.editor "vim"
```

### 设置默认分支名

```bash
git config --global init.defaultBranch main
```

## 仓库级与全局级配置

- `--global`：对当前用户的所有 Git 仓库生效。
- 不带 `--global`：仅对当前仓库生效。

例如，只为当前仓库设置邮箱：

```bash
git config user.email "project@example.com"
```

## 常用别名

### 设置简洁日志别名

```bash
git config --global alias.lg "log --oneline --graph --decorate --all"
```

### 设置状态别名

```bash
git config --global alias.st status
```

配置后就可以使用：

```bash
git lg
git st
```

## 注意事项

- 团队协作中，用户名和邮箱应与代码托管平台保持一致，便于识别提交人。
- 如果提交作者信息错误，可以修改配置后再重新创建提交。
