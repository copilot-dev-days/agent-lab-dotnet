<!-- l10n-sync: source-file="README.md" -->
# 🎲 Soc Ops — VS Code GitHub Copilot Agent Lab

> **Um workshop prático onde você constrói um jogo de Social Bingo enquanto domina o desenvolvimento com IA usando o modo Agente do VS Code e o GitHub Copilot.**

🎮 **[Jogar](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/)** • 📚 **[Começar o Lab](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/)** • ⏱️ **~1 hora** • 🎯 **Intermediário**

---

## 🚀 O que é isso?

**Soc Ops** é um jogo de Social Bingo para encontros presenciais — encontre pessoas que correspondam às perguntas e consiga 5 em uma fileira! Mas, mais importante, é sua tela para aprender a construir software com agentes de IA.

Partindo de um app Blazor funcional, você usará o **modo Agente do VS Code** com **GitHub Copilot** para redesenhar a UI, gerar conteúdo personalizado e adicionar novas funcionalidades — tudo guiado por um lab estruturado que ensina padrões reais de desenvolvimento agêntico.

---

## 🛠️ O que Você Vai Construir

| Etapa | Você vai… |
|-------|-----------|
| 🧠 **Engenharia de Contexto** | Ensinar o Copilot sobre seu código com instruções de workspace |
| 🎨 **Redesenhar a UI** | Transformar a aparência do app com sprints de design assistidos por IA |
| 🃏 **Criar Temas de Quiz** | Gerar sets de perguntas personalizados com um agente Quiz Master |
| ⚙️ **Adicionar Funcionalidades** | Construir um modo de Caça ao Tesouro usando agentes TDD |

---

## 🎓 O que Você Vai Aprender

| Habilidade | Descrição |
|------------|-----------|
| **Engenharia de Contexto** | Escreva `.github/copilot-instructions.md` para fundamentar cada interação com a IA |
| **Agentes em Segundo Plano** | Execute tarefas paralelas em worktrees isolados com Copilot CLI |
| **Agentes na Nuvem** | Delegue trabalho demorado para a nuvem enquanto foca em outras coisas |
| **Desenvolvimento Design-First** | Use o modo Plano para iterar na UI antes de escrever uma linha de código |
| **Agentes Personalizados** | Construa um agente Quiz Master reutilizável com seus próprios prompts |
| **Agentes TDD** | Impulsione o desenvolvimento com agentes Red → Green → Refactor |

---

## 🧰 Stack Tecnológico

- **.NET 10** + **Blazor WebAssembly** — C# no navegador
- **GitHub Copilot Agent Mode** — agentes em segundo plano, na nuvem e personalizados
- **GitHub Pages** — deploys automáticos a cada push para `main`
- **GitHub Codespaces** — ambiente de desenvolvimento na nuvem sem configuração

---

## ⚡ Início Rápido

### Opção A: GitHub Codespaces (recomendado)

1. Clique em **Use this template** → **Create a new repository**
2. Abra seu novo repositório → **Code** → **Codespaces** → **Create codespace on main**
3. Aguarde o devcontainer, depois execute `/setup` no painel de Chat do Copilot

### Opção B: Desenvolvimento Local

```bash
# Pré-requisitos: .NET 10 SDK, VS Code, extensão do GitHub Copilot

git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO
cd SEU_REPOSITORIO/SocOps
dotnet run
```

> 💡 **Dica:** Habilite o GitHub Pages em **Settings → Pages → GitHub Actions** para que cada commit publique seu jogo automaticamente!

---

## 📚 Guia do Lab

| Parte | Título | Tempo |
|-------|--------|-------|
| [**00**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=00-overview) | Visão Geral & Lista Rápida | — |
| [**01**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=01-setup) | Configuração & Engenharia de Contexto | 15 min |
| [**02**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=02-design) | Frontend Design-First | 15 min |
| [**03**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=03-quiz-master) | Quiz Master Personalizado | 10 min |
| [**04**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=04-multi-agent) | Desenvolvimento Multi-Agent | 20 min |

> 📝 Os guias do lab também estão disponíveis na pasta [`workshop/pt_BR/`](workshop/pt_BR/) para leitura offline.

---

## 🔧 Comandos

```bash
cd SocOps
dotnet run    # Iniciar servidor em http://localhost:5166
dotnet build  # Compilar o projeto
dotnet test   # Executar testes
```

O deploy é feito automaticamente no GitHub Pages ao fazer push para `main`.
