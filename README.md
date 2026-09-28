<div align="center">

# 🚀 devstarter — Zero-Config Devcontainer Templates

### *Production-Ready, Standardized Development Environments for VS Code & GitHub Codespaces*

[![VS Code Devcontainers](https://img.shields.io/badge/VS%20Code-Devcontainers-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white)](https://code.visualstudio.com/docs/remote/containers)
[![GitHub Codespaces](https://img.shields.io/badge/GitHub-Codespaces-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/features/codespaces)
[![Docker](https://img.shields.io/badge/Docker-Containers-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

<p align="center">
  Stop wasting engineering hours debugging local environment mismatches, toolchain versions, and linter drift.<br />
  <strong>devstarter</strong> delivers pre-configured, isolated, multi-language container environments engineered for maximum developer velocity.
</p>

</div>

---

## 📋 Table of Contents
- [Why devstarter?](#-why-devstarter)
- [Supported Language Stacks](#-supported-language-stacks)
- [Repository Architecture](#-repository-architecture)
- [Quick Start Guide](#-quick-start-guide)
- [CLI & Codespaces Usage](#-cli--codespaces-usage)
- [Customization & Extensions](#-customization--extensions)
- [Troubleshooting & FAQ](#-troubleshooting--faq)
- [License & Copyright](#-license--copyright)

---

## 💡 Why devstarter?

Setting up a local development environment often means dealing with:
- ❌ Incompatible language runtimes and SDK versions across team members.
- ❌ Fragmented linter, formatter, and debugger configurations.
- ❌ "Works on my machine" roadblocks during onboarding.

**devstarter** solves this with standardized, containerized environments:
- ✅ **Single Source of Truth**: Dockerfile + `devcontainer.json` define everything: OS, SDKs, VS Code extensions, and formatters.
- ✅ **Zero Host Pollution**: Run multiple conflicting compiler or Node/Python versions without polluting your host machine.
- ✅ **Cloud & Local Parity**: Identical experience whether running locally in VS Code or in the cloud via GitHub Codespaces.

---

## 📦 Supported Language Stacks

| Language / Stack | Directory | Pre-Installed Tooling & Extensions | Base Container Image |
| :--- | :--- | :--- | :--- |
| 🐍 **Python 3.11+** | [`template/python`](template/python) | Pyright, Ruff, Black, pytest, Jupyter, ipykernel, git | `mcr.microsoft.com/devcontainers/python:3.11` |
| 🟢 **Node.js / TypeScript** | [`template/node`](template/node) | ESLint, Prettier, Vitest, npm, pnpm, yarn | `mcr.microsoft.com/devcontainers/typescript-node:20` |
| ⚡ **C / C++** | [`template/cpp`](template/cpp) | GCC, Clang, CMake, GDB, LLDB, C/C++ Extension Pack | `mcr.microsoft.com/devcontainers/cpp:debian` |
| 🐹 **Go 1.21+** | [`template/go`](template/go) | Official Go Extension, gopls, golangci-lint, delve debugger | `mcr.microsoft.com/devcontainers/go:1.21` |
| 🦀 **Rust** | [`template/rust`](template/rust) | rust-analyzer, cargo-edit, CodeLLDB debugger, clippy, rustfmt | `mcr.microsoft.com/devcontainers/rust:latest` |
| ☕ **Java 17+** | [`template/java`](template/java) | Java Extension Pack, Maven, Gradle, Spring Boot tools, JUnit | `mcr.microsoft.com/devcontainers/java:17` |

---

## 📂 Repository Architecture

```text
devstarter/
├── .devcontainer/                # Default root devcontainer configuration
│   ├── devcontainer.json         # Primary container specifications
│   └── Dockerfile                # Base image customizations
├── .github/
│   └── dependabot.yml            # Automated dependency update configuration
├── template/                     # Language-specific template libraries
│   ├── cpp/                      # C/C++ modern toolchain configuration
│   ├── go/                       # Go microservices & CLI setup
│   ├── java/                     # Java / Spring Boot / Maven environment
│   ├── node/                     # TypeScript / Node.js full-stack setup
│   ├── python/                   # Python data science & web setup
│   └── rust/                     # Rust systems programming environment
├── LICENSE                       # MIT License with copyright
└── README.md                     # Comprehensive documentation
```

---

## ⚡ Quick Start Guide

### Option 1: VS Code with Remote - Containers
1. Ensure **Docker Desktop** is installed and running on your system.
2. Install the **[Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)** extension in VS Code.
3. Select your desired language template from `template/<language>` and copy its contents into your target repository's `.devcontainer/` folder:
   ```bash
   # Example: adopting the Python template in your project
   mkdir -p my-project/.devcontainer
   cp -r devstarter/template/python/* my-project/.devcontainer/
   ```
4. Open `my-project` in VS Code.
5. Click the bottom-left notification: **"Reopen in Container"** (or press `F1` and select `Dev Containers: Reopen in Container`).

### Option 2: GitHub Codespaces
1. Push your repository containing the `.devcontainer` configuration to GitHub.
2. Click the green **Code** button on GitHub -> **Codespaces** tab -> **Create codespace on main**.
3. Within minutes, your complete IDE, runtime, and debuggers are fully spun up in the cloud.

---

## 🛠️ CLI & Advanced Usage

If you prefer using the `@devcontainers/cli`:

```bash
# Install Dev Containers CLI globally
npm install -g @devcontainers/cli

# Build and start container for current folder
devcontainer up --workspace-folder .

# Execute shell command inside running container
devcontainer exec --workspace-folder . zsh
```

---

## 🔧 Customization & Extension

Each `devcontainer.json` supports custom VS Code settings and lifecycle hooks:
- **`postCreateCommand`**: Run automated installation commands upon initialization (e.g., `pip install -r requirements.txt` or `npm install`).
- **`customizations.vscode.extensions`**: Add your team's favorite VS Code marketplace extensions.
- **`forwardPorts`**: Automatically forward database or local server ports (e.g. `[3000, 8000, 5432]`).

---

## ❓ Troubleshooting & FAQ

<details>
<summary><strong>Docker daemon connection error</strong></summary>
Ensure Docker Desktop is active and "Expose daemon on tcp://localhost:2375 without TLS" or WSL2 integration is enabled if running on Windows.
</details>

<details>
<summary><strong>File permission discrepancies between container and host</strong></summary>
Devcontainer images automatically map standard UID/GID (1000:1000) for seamless file ownership between host OS and container runtime.
</details>

---

## 📄 License & Copyright

```
Copyright (c) 2025-2026 Pradeep Basha (Pradeep-B28). All Rights Reserved.

Licensed under the MIT License. You may freely use, modify, and distribute
this project under the terms of the MIT license.
```

Maintained with 💻 by **[Pradeep Basha](https://github.com/Pradeep-B28)**.
