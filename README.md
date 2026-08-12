# 🚀 devstarter — Zero-Config Devcontainer Templates

> Open any project in VS Code with one click. No setup. No config. Just code.

[![GitHub stars](https://img.shields.io/github/stars/your-username/devstarter?style=social)](https://github.com/your-username/devstarter)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Dependabot](https://img.shields.io/badge/Dependabot-enabled-brightgreen)](https://github.com/dependabot)

---

## 🤯 The Problem

- **Contributors can't contribute** because setting up dev environments takes **2 hours**.
- **Teams waste days** debugging "it works on my machine" issues.
- **Students give up** before writing a single line of code.

## ✨ The Solution

**`devstarter`** provides production-ready `.devcontainer` configurations for the 6 most popular languages. 

- ✅ **0 minutes** to start coding (not 120).
- ✅ **Identical environments** for every contributor.
- ✅ **Pre-configured linting, debugging, and testing.**

---

## 🎯 Supported Languages

| Language | Version | Extensions Included | Testing Framework |
|----------|---------|---------------------|-------------------|
| 🐍 Python | 3.12 | Pylint, autopep8, debugpy | pytest |
| 🟢 Node.js | 20 | ESLint, Prettier, TypeScript | npm test |
| 🐹 Go | 1.22 | Language Server, Delve, Staticcheck | go test |
| 🦀 Rust | Latest | rust-analyzer, Clippy, Crates | cargo test |
| ⚙️ C++ | 20 (Bookworm) | C++ Tools, CMake, Clang-Format | gtest/ctest |
| ☕ Java | 21 | Java Pack, Maven, Gradle | JUnit |

---

## 🚀 Quick Start

### Option 1: Use a Template Directly (Clone)

```bash
# Clone the repo
git clone https://github.com/Pradeep-B28/devstarter.git

# Copy the template you need into your project root
cp -r devstarter/templates/python /path/to/your/project/.devcontainer

# Open in VS Code
code /path/to/your/project
