# 🚀 devstarter — Zero-Config Devcontainer Templates

> Open any project in VS Code with **one click**. No setup. No config. Just code.

[![GitHub stars](https://img.shields.io/github/stars/Pradeep-B28/devstarter?style=social)](https://github.com/Pradeep-B28/devstarter/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/Pradeep-B28/devstarter?style=social)](https://github.com/Pradeep-B28/devstarter/forks)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Dependabot](https://img.shields.io/badge/Dependabot-enabled-brightgreen)](https://github.com/dependabot)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

---

## 📖 Table of Contents

- [🤯 The Problem](#-the-problem)
- [✨ The Solution](#-the-solution)
- [🎯 Supported Languages](#-supported-languages)
- [🚀 Quick Start](#-quick-start)
- [🧪 Test Your Template](#-test-your-template)
- [🔄 Auto-Updates with Dependabot](#-auto-updates-with-dependabot)
- [🛠 Customizing a Template](#-customizing-a-template)
- [📂 Repository Structure](#-repository-structure)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 🤯 The Problem

Setting up a development environment is **painfully slow**:

- ⏱️ **Contributors waste 2 hours** just getting dependencies installed.
- 🐛 **"It works on my machine"** — the most hated phrase in software engineering.
- 😫 **Students give up** before writing a single line of code.
- 🔄 **Teams have inconsistent environments** leading to production bugs.

---

## ✨ The Solution

**`devstarter`** provides **production-ready `.devcontainer` configurations** for the 6 most popular programming languages.

**What you get:**
- ✅ **Zero minutes** to start coding (not 120).
- ✅ **Identical environments** for every contributor.
- ✅ **Pre-configured linting, debugging, and testing** out of the box.
- ✅ **GitHub Codespaces ready** — code in your browser instantly.
- ✅ **Weekly security updates** via Dependabot.

---

## 🎯 Supported Languages

| Language | Version | VS Code Extensions | Testing Framework |
|----------|---------|-------------------|-------------------|
| 🐍 **Python** | 3.12 | Pylint, autopep8, debugpy, Pylance | `pytest` |
| 🟢 **Node.js** | 20 | ESLint, Prettier, TypeScript, npm-intellisense | `npm test` |
| 🐹 **Go** | 1.22 | Language Server, Delve, Staticcheck | `go test` |
| 🦀 **Rust** | Latest | rust-analyzer, Clippy, Crates, Even Better TOML | `cargo test` |
| ⚙️ **C++** | 20 | C++ Tools, CMake, Clang-Format, Better C++ Syntax | `gtest/ctest` |
| ☕ **Java** | 21 | Java Pack, Maven, Gradle, Spring Initializr | `JUnit` |

---

## 🚀 Quick Start

### Option 1: Use in Your Project (Copy a Template)

```bash
# Clone this repo
git clone https://github.com/Pradeep-B28/devstarter.git

# Copy the template you need into your project root
cp -r devstarter/templates/python /path/to/your/project/.devcontainer

# Open in VS Code
code /path/to/your/project