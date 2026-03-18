# Git 安装指南

## 适用场景

当你需要在新设备上开始使用 Git，或帮助同事快速完成安装时，可以参考本文档。

## Windows

前往 [Git for Windows](https://gitforwindows.org/) 下载并安装，安装完成后打开 Git Bash 或终端执行：

```bash
git --version
```

## macOS

如果已经安装 Homebrew，可以执行：

```bash
brew install git
```

安装完成后执行：

```bash
git --version
```

## Ubuntu / Debian

### 1. 更新包列表

```bash
sudo apt update
```

### 2. 安装 Git

```bash
sudo apt install git
```

### 3. 验证安装结果

```bash
git --version
```

## 安装完成后的建议操作

首次安装完成后，建议继续配置用户名与邮箱：

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

你也可以继续阅读 `git-config-usage.md` 了解更多配置项。
