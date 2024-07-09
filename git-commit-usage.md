

# git-commit-usage

## Git Commit 规范指南

Git 提交信息应遵循一定的规范，以便于更好地管理和理解项目的变更历史。本文档介绍了提交信息的结构和规范。

## 提交信息结构

每个提交信息应包含以下三个部分：头部（Header）、主体（Body）、尾部（Footer）。

### 头部（Header）

头部包含了一个简短的描述，指明了变更的类型和涉及的范围（可选）。格式如下：

```
<type>(<scope>): <subject>
```

- **type**: 表示提交的类型，常见的类型包括 
  - `feat`（新功能）、
  - `fix`（修复bug）、
  - `docs`（文档更新）、
  - `style`（代码格式调整）、
  - `refactor`（重构代码）、
  - `test`（添加或修改测试）、
  - `chore`（构建过程或辅助工具的变动）等。

- **scope**（可选）: 表示影响范围，即变更涉及的模块或组件。
- **subject**: 是提交的简短描述，不超过50个字符。使用动词开头，使用第一人称现在时或者祈使句。

### 主体（Body）

主体部分可以提供更详细的描述，解释为什么做出这些变更、如何做以及变更背后的原因。主体部分通常在需要详细解释时使用，可以有多个段落，每行不超过72个字符。

### 尾部（Footer）

尾部通常包含与提交相关的关闭Issue的信息、Breaking Changes的描述等。

## 提交示例

### 示例1：添加新功能

```
feat(parser): add support for parsing JSON files

- Added JSON file parsing capability to the parser module.
- Updated documentation to reflect new functionality.
```

### 示例2：修复Bug

```
fix(utils): fix null pointer exception in StringUtils

- Fixed a bug where StringUtils was throwing NullPointerException when input is null.
```

