# Claude Code

Claude Code 是一个 AI 驱动的终端开发助手，旨在通过自然语言对话帮助开发者编写代码、调试问题和管理项目。

## 概述

这是一个基于 TypeScript 和 React Ink 构建的命令行工具，提供以下核心功能：

- **智能对话**：与 Claude AI 进行自然语言交互，获取编程帮助
- **代码生成与编辑**：自动生成代码片段、修改现有文件
- **项目管理**：集成 Git 操作、文件浏览和终端命令执行
- **插件系统**：支持 MCP (Model Context Protocol) 工具扩展
- **多模态支持**：支持图像分析、计算机控制等高级功能

## 技术栈

- **运行时**: [Bun](https://bun.sh/)
- **语言**: TypeScript
- **UI 框架**: [React Ink](https://github.com/vadimdemedes/ink) (终端 React 渲染器)
- **CLI 框架**: Commander.js
- **构建**: Bun 原生打包 (`bun:bundle`)

## 项目结构

```
├── main.tsx              # 应用入口点
├── setup.ts              # 初始化逻辑
├── commands.ts           # CLI 命令定义
├── commands/             # 命令实现
├── components/           # React Ink 组件
├── tools/                # AI 工具实现（文件操作、Git、终端等）
├── services/             # 核心服务（API、认证、分析等）
├── utils/                # 工具函数
├── hooks/                # 自定义 React Hooks
├── types/                # TypeScript 类型定义
├── constants/            # 常量配置
├── skills/               # 内置技能
├── plugins/              # 插件系统
├── bridge/               # 桥接模块
└── context/              # 应用状态管理
```

## 主要模块

### CLI 命令 (`commands/`)
- Git 操作（暂存、提交、PR）
- 文件和目录管理
- 系统诊断和配置
- MCP 服务器管理

### AI 工具 (`tools/`)
- **AgentTool**: 多代理协作和任务委派
- **BashTool**: 终端命令执行
- **FileReadTool**: 文件阅读和分析
- **FileEditTool**: 智能代码编辑
- **FileCreateTool**: 文件创建
- **GitTools**: Git 操作（状态、差异、提交、PR）
- **SearchTool**: 代码搜索（Grep、Glob）
- **MCP Tools**: 外部 MCP 服务器集成

### UI 组件 (`components/`)
- 聊天界面和消息渲染
- 输入处理和提示
- 文件浏览器和代码查看器
- 加载状态和进度指示器
- 错误处理和警告显示

### 服务 (`services/`)
- **API 客户端**: Anthropic Claude API 通信
- **认证**: OAuth 和 API 密钥管理
- **分析**: 事件追踪和遥测
- **MCP**: Model Context Protocol 客户端
- **策略限制**: 安全策略和配额管理

## 开发

### 前置要求

- [Bun](https://bun.sh/) 运行时

### 安装依赖

```bash
bun install
```

### 开发模式

```bash
bun dev
```

### 构建

```bash
bun build
```

### 运行测试

```bash
bun test
```

## 许可证

版权所有 (c) Anthropic PBC。保留所有权利。
