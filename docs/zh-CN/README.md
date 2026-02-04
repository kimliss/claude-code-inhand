<div align="center">

# Claude Code Inhand

**Claude Code 在手，拥有一切。**

为 [Claude Code](https://docs.anthropic.com/en/docs/claude-code) 打造的插件市场 — 11 个插件，6 大分类，覆盖完整开发生命周期。

[![Plugins](https://img.shields.io/badge/插件-11-blue)](../../plugins/)
[![Categories](https://img.shields.io/badge/分类-6-green)](#插件目录)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](../../LICENSE)

[English](../../README.md) | **简体中文**

[快速开始](#快速开始) · [插件目录](#插件目录) · [参与贡献](#参与贡献)

</div>

---

## 特性

- **全栈覆盖** — 后端、前端、移动端、DevOps、数据库插件一应俱全
- **LSP 集成** — 内置 Go、Java、Python、Vue、Swift、Dart 语言服务器支持
- **10 个 AI Agent** — 规划、代码审查、TDD、安全审计、架构设计等
- **3 种上下文模式** — 开发、调研、审查工作流自由切换
- **可扩展** — 使用内置模板创建自定义插件

## 快速开始

```bash
# 添加插件市场
claude plugin marketplace add kimliss/claude-code-inhand

# 安装插件
claude plugin install dev-toolkit
claude plugin install go-dev
```

## 插件目录

### 通用开发

| 插件 | 说明 | LSP |
|------|------|-----|
| [dev-toolkit](../../plugins/dev-toolkit/) | 通用开发工具包，含 10 个 Agent、3 种上下文模式、4 个 Skill | — |

### 后端

| 插件 | 说明 | LSP |
|------|------|-----|
| [go-dev](../../plugins/go-dev/) | Go 开发，项目脚手架 | `gopls` |
| [java-dev](../../plugins/java-dev/) | Java / Spring Boot 开发 | `jdtls` |
| [python-dev](../../plugins/python-dev/) | Python (Django / FastAPI) 开发 | `Pyright` |

### 前端

| 插件 | 说明 | LSP |
|------|------|-----|
| [vue-dev](../../plugins/vue-dev/) | Vue.js / Nuxt 开发 | `Vue Language Server` |
| [react-dev](../../plugins/react-dev/) | React / Next.js 开发 | — |

### 移动端

| 插件 | 说明 | LSP |
|------|------|-----|
| [android-dev](../../plugins/android-dev/) | Android / Kotlin / Jetpack Compose | — |
| [ios-dev](../../plugins/ios-dev/) | iOS / Swift / SwiftUI | `sourcekit-lsp` |
| [flutter-dev](../../plugins/flutter-dev/) | Flutter / Dart 跨平台开发 | `Dart Language Server` |

### DevOps

| 插件 | 说明 | LSP |
|------|------|-----|
| [devops-toolkit](../../plugins/devops-toolkit/) | CI/CD、Docker、Kubernetes、Terraform | — |

### 数据库

| 插件 | 说明 | LSP |
|------|------|-----|
| [database-toolkit](../../plugins/database-toolkit/) | Schema 设计、查询优化、数据迁移 | — |

## dev-toolkit

驱动日常开发的核心插件。

| 组件 | 详情 |
|------|------|
| **Agents** | `planner` · `code-reviewer` · `tdd-guide` · `security-reviewer` · `architect` · `build-error-resolver` · `e2e-runner` · `refactor-cleaner` · `doc-updater` · `database-reviewer` |
| **Contexts** | `dev` — 快速实现 · `research` — 探索调研 · `review` — 代码质量与安全审查 |
| **Skills** | `iterative-retrieval` · `backend-patterns` · `frontend-patterns` · `explain-code` |

## 项目结构

```
claude-plugins-inhand/
├── .claude-plugin/
│   └── marketplace.json        # 插件注册表 (11 个插件)
├── plugins/                    # 所有插件
│   ├── dev-toolkit/
│   ├── go-dev/
│   ├── java-dev/
│   ├── python-dev/
│   ├── vue-dev/
│   ├── react-dev/
│   ├── android-dev/
│   ├── ios-dev/
│   ├── flutter-dev/
│   ├── devops-toolkit/
│   └── database-toolkit/
├── docs/                       # 多语言文档
│   └── zh-CN/                  # 简体中文
├── external_plugins/           # 外部插件引用 (预留)
└── templates/                  # 插件开发模板
```

## 参与贡献

```bash
# 从模板创建新插件
cp -r templates/plugin-template plugins/your-plugin
```

详见 [CONTRIBUTING.md](../../templates/CONTRIBUTING.md)。

## 许可证

本项目基于 [GNU General Public License v3.0](../../LICENSE) 许可。
