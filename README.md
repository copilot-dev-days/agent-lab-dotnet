🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

# 🎲 Soc Ops — VS Code GitHub Copilot Agent Lab

> **A hands-on workshop where you build a Social Bingo game while mastering AI-powered development with VS Code Agent Mode and GitHub Copilot.**

🎮 **[Play the Game](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/)** • 📚 **[Start the Lab](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/)** • ⏱️ **~1 hour** • 🎯 **Intermediate**

---

## 🚀 What Is This?

**Soc Ops** is a Social Bingo game for in-person mixers — find people who match the questions and get 5 in a row! But more importantly, it's your canvas for learning how to build software with AI agents.

Starting from a working Blazor app, you'll use **VS Code Agent Mode** with **GitHub Copilot** to redesign the UI, generate custom content, and build new features — all guided by a structured lab that teaches real-world agentic development patterns.

---

## 🛠️ What You'll Build

| Step | You'll… |
|------|---------|
| 🧠 **Context Engineer** | Teach Copilot about your codebase with workspace instructions |
| 🎨 **Redesign the UI** | Transform the app's look with AI-assisted design sprints |
| 🃏 **Create Quiz Themes** | Generate custom bingo question sets with a Quiz Master agent |
| ⚙️ **Add New Features** | Build a Scavenger Hunt mode using TDD agents |

---

## 🎓 What You'll Learn

| Skill | Description |
|-------|-------------|
| **Context Engineering** | Write `.github/copilot-instructions.md` to ground every AI interaction |
| **Background Agents** | Run parallel tasks in isolated worktrees with Copilot CLI |
| **Cloud Agents** | Delegate long-running work to the cloud while you focus on other things |
| **Design-First Development** | Use Plan Mode to iterate on UI before writing a line of code |
| **Custom Agents** | Build a reusable Quiz Master agent with your own prompts |
| **TDD Agents** | Drive feature development with Red → Green → Refactor agents |

---

## 🧰 Tech Stack

- **.NET 10** + **Blazor WebAssembly** — C# in the browser
- **GitHub Copilot Agent Mode** — background, cloud, and custom agents
- **GitHub Pages** — automatic deploys on every push to `main`
- **GitHub Codespaces** — zero-config cloud dev environment

---

## ⚡ Quick Start

### Option A: GitHub Codespaces (recommended)

1. Click **Use this template** → **Create a new repository**
2. Open your new repo → **Code** → **Codespaces** → **Create codespace on main**
3. Wait for the devcontainer, then run `/setup` in the Copilot Chat panel

### Option B: Local Development

```bash
# Prerequisites: .NET 10 SDK, VS Code, GitHub Copilot extension

git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME
cd YOUR_REPO_NAME/SocOps
dotnet run
```

> 💡 **Tip:** Enable GitHub Pages under **Settings → Pages → GitHub Actions** so every commit auto-deploys your game live!

---

## 📚 Lab Guide

| Part | Title | Time |
|------|-------|------|
| [**00**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=00-overview) | Overview & Checklist | — |
| [**01**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=01-setup) | Setup & Context Engineering | 15 min |
| [**02**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=02-design) | Design-First Frontend | 15 min |
| [**03**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=03-quiz-master) | Custom Quiz Master | 10 min |
| [**04**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=04-multi-agent) | Multi-Agent Development | 20 min |

> 📝 Lab guides are also available in the [`workshop/`](workshop/) folder for offline reading.

---

## 🔧 Commands

```bash
cd SocOps
dotnet run    # Start dev server at http://localhost:5166
dotnet build  # Build the project
dotnet test   # Run tests
```

Deploys automatically to GitHub Pages on push to `main`.
