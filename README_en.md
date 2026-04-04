# 1Panel Tools Desktop

English | [中文](./README.md)

## Overview

`1Panel Tools Desktop` is the desktop-packaged edition of `1Panel-Tools`. It uses Tauri 2 to wrap the existing Docker Compose to 1Panel AppStore tool into a distributable desktop application.

This repository focuses on:

- keeping the current web tool behavior and core implementation intact
- adding Windows/Linux desktop packaging
- providing GitHub Actions CI and GitHub Releases publishing

![1Panel Tools Desktop](./public/1Panel-Tools.png)

## Original Authors And Contributors

- Upstream foundation: `IT-Tools`
- Original upstream author: `Corentin Th`
- 1Panel-oriented adaptation: `arch3rPro/1Panel-Tools`
- Desktop packaging, release workflow integration, and desktop distribution contribution in this repository: `ixbaicn`

## Scope Of Changes

This repository mainly adds:

- the Tauri 2 desktop wrapper
- desktop build outputs and packaging
- GitHub Actions CI / Release workflows
- attribution and licensing notices for the desktop distribution

This repository does not claim a rewrite of the original core business features. The Docker Compose to 1Panel AppStore implementation, tool flow, and existing feature behavior remain based on the inherited project structure.

See [NOTICE](./NOTICE) and [LICENSE](./LICENSE) for attribution and licensing details.

## Current Features

- Docker Compose to 1Panel AppStore conversion
- App metadata and parameter editing
- Export-ready output generation
- Local desktop development
- Desktop installer builds
- GitHub Releases upload for desktop bundles

## Local Development

### Requirements

- Node.js 22+
- pnpm 9.11+
- Rust stable
- Tauri 2 build dependencies

### Install

```bash
pnpm install
```

### Web Dev

```bash
pnpm dev
```

### Desktop Dev

```bash
pnpm tauri:dev
```

### Build Desktop Bundles

```bash
pnpm tauri:build
```

## GitHub Release Flow

The repository already includes a desktop release workflow:

1. Push the target code to `main`
2. Create and publish a GitHub Release
3. GitHub Actions builds the desktop app
4. The generated bundles are uploaded to that Release

## License

This project remains licensed under `GNU GPLv3`.

- Full license text: [LICENSE](./LICENSE)
- Attribution, contributor, and modification notice: [NOTICE](./NOTICE)
