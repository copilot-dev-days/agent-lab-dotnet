<!-- l10n-sync: source-file="README.md" -->
# 🎲 Soc Ops — VS Code GitHub Copilot Agent Lab

> **Un workshop práctico donde construyes un juego de Social Bingo mientras dominas el desarrollo con IA usando el modo Agente de VS Code y GitHub Copilot.**

🎮 **[Jugar](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/)** • 📚 **[Empezar el Lab](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/)** • ⏱️ **~1 hora** • 🎯 **Intermedio**

---

## 🚀 ¿Qué es esto?

**Soc Ops** es un juego de Social Bingo para encuentros presenciales — ¡encuentra personas que coincidan con las preguntas y consigue 5 en fila! Pero más importante aún, es tu lienzo para aprender a construir software con agentes de IA.

Partiendo de una app Blazor funcional, usarás el **modo Agente de VS Code** con **GitHub Copilot** para rediseñar la UI, generar contenido personalizado y añadir nuevas funcionalidades — todo guiado por un lab estructurado que enseña patrones de desarrollo agéntico del mundo real.

---

## 🛠️ Lo que Construirás

| Paso | Lo que harás… |
|------|--------------|
| 🧠 **Ingeniería de Contexto** | Enseñarás a Copilot sobre tu código con instrucciones de workspace |
| 🎨 **Rediseñar la UI** | Transformarás la apariencia de la app con sprints de diseño asistidos por IA |
| 🃏 **Crear Temas de Quiz** | Generarás sets de preguntas personalizados con un agente Quiz Master |
| ⚙️ **Agregar Funcionalidades** | Construirás un modo Búsqueda del Tesoro usando agentes TDD |

---

## 🎓 Lo que Aprenderás

| Habilidad | Descripción |
|-----------|-------------|
| **Ingeniería de Contexto** | Escribe `.github/copilot-instructions.md` para fundamentar cada interacción con la IA |
| **Agentes en Segundo Plano** | Ejecuta tareas paralelas en worktrees aislados con Copilot CLI |
| **Agentes en la Nube** | Delega trabajo de larga duración a la nube mientras te concentras en otras cosas |
| **Desarrollo Design-First** | Usa el modo Plan para iterar en la UI antes de escribir una sola línea de código |
| **Agentes Personalizados** | Construye un agente Quiz Master reutilizable con tus propios prompts |
| **Agentes TDD** | Impulsa el desarrollo de funcionalidades con agentes Red → Green → Refactor |

---

## 🧰 Stack Tecnológico

- **.NET 10** + **Blazor WebAssembly** — C# en el navegador
- **GitHub Copilot Agent Mode** — agentes en segundo plano, en la nube y personalizados
- **GitHub Pages** — deploys automáticos en cada push a `main`
- **GitHub Codespaces** — entorno de desarrollo en la nube sin configuración

---

## ⚡ Inicio Rápido

### Opción A: GitHub Codespaces (recomendado)

1. Haz clic en **Use this template** → **Create a new repository**
2. Abre tu nuevo repositorio → **Code** → **Codespaces** → **Create codespace on main**
3. Espera a que el devcontainer esté listo, luego ejecuta `/setup` en el panel de Chat de Copilot

### Opción B: Desarrollo Local

```bash
# Requisitos: .NET 10 SDK, VS Code, extensión de GitHub Copilot

git clone https://github.com/TU_USUARIO/TU_REPOSITORIO
cd TU_REPOSITORIO/SocOps
dotnet run
```

> 💡 **Consejo:** Habilita GitHub Pages en **Settings → Pages → GitHub Actions** para que cada commit publique tu juego automáticamente.

---

## 📚 Guía del Lab

| Parte | Título | Tiempo |
|-------|--------|--------|
| [**00**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=00-overview) | Descripción General & Lista Rápida | — |
| [**01**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=01-setup) | Configuración & Ingeniería de Contexto | 15 min |
| [**02**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=02-design) | Frontend Design-First | 15 min |
| [**03**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=03-quiz-master) | Quiz Master Personalizado | 10 min |
| [**04**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=04-multi-agent) | Desarrollo Multi-Agent | 20 min |

> 📝 Las guías del lab también están disponibles en la carpeta [`workshop/es/`](workshop/es/) para lectura offline.

---

## 🔧 Comandos

```bash
cd SocOps
dotnet run    # Iniciar servidor en http://localhost:5166
dotnet build  # Compilar el proyecto
dotnet test   # Ejecutar tests
```

El deploy se hace automáticamente en GitHub Pages al hacer push a `main`.
