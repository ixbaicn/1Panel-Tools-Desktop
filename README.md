# 1Panel Tools Desktop

[English](./README_en.md) | 中文

## 项目简介

`1Panel Tools Desktop` 是 `1Panel-Tools` 的桌面端封装版本，使用 Tauri 2 将现有的 Docker Compose 转 1Panel AppStore 工具打包为可分发的桌面应用。

当前仓库的目标是：

- 保留现有 Web 工具的核心功能与交互逻辑
- 增加 Windows/Linux 桌面端构建与发布能力
- 提供 GitHub Actions 自动构建与 GitHub Releases 发布流程

![1Panel Tools Desktop](./public/1Panel-Tools.png)

## 原作者与贡献者

- 上游基础项目：`IT-Tools`
- 上游原作者：`Corentin Th`
- 1Panel 方向改造：`arch3rPro/1Panel-Tools`
- 当前仓库桌面端封装、构建发布流程与桌面分发适配贡献者：`ixbaicn`

## 改动说明

当前仓库主要提供桌面端封装能力，包括：

- Tauri 2 桌面端工程
- 桌面端构建与安装包输出
- GitHub Actions CI / Release 工作流
- 项目归属、贡献者与许可证说明整理

未在本次整理中声明重写原有核心业务逻辑。Docker Compose 转 1Panel AppStore 的主要功能实现、页面流程和工具行为，仍基于现有项目体系。

更多归属与许可证信息见 [NOTICE](./NOTICE) 与 [LICENSE](./LICENSE)。

## 当前功能

- Docker Compose 转 1Panel AppStore
- 应用元信息与参数配置
- 转换结果导出
- 桌面端本地运行
- 桌面端安装包构建
- GitHub Releases 自动上传桌面构建产物

## 本地开发

### 环境要求

- Node.js 22+
- pnpm 9.11+
- Rust stable
- Tauri 2 构建依赖

### 安装依赖

```bash
pnpm install
```

### Web 开发

```bash
pnpm dev
```

### 桌面端开发

```bash
pnpm tauri:dev
```

### 构建桌面安装包

```bash
pnpm tauri:build
```

## GitHub 发布

仓库已包含桌面端发布工作流：

1. 推送代码到 `main`
2. 创建并发布 GitHub Release
3. GitHub Actions 自动构建桌面应用
4. 构建产物自动上传到该 Release

## 许可证

本项目继续遵循 `GNU GPLv3`。

- 许可证正文见 [LICENSE](./LICENSE)
- 原作者、贡献者与改动范围说明见 [NOTICE](./NOTICE)
