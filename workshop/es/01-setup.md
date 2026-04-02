<!-- l10n-sync: source-file="workshop/01-setup.md" -->
# Parte 1: Configuración & Ingeniería de Contexto

[🎮 Demo en Vivo](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/) • [📚 Guía del Lab](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/) • [← Descripción General](00-overview.md)

---

> ⏱️ **Tiempo:** ~15 minutos

En esta sección, configurarás tu entorno de desarrollo y le enseñarás a GitHub Copilot sobre tu código.

---

## 🔧 Configuración Inicial

### Paso 1: Crea Tu Repositorio

1. Abre [github.com/copilot-dev-days/agent-lab-dotnet](https://github.com/copilot-dev-days/agent-lab-dotnet)
2. Haz clic en **Use this template** → **Create a new repository**
   - Nombre: `my-soc-ops-csharp`
   - Visibilidad: **Public**
3. ✅ ¡Tu propio repositorio Soc Ops está listo!

### Paso 2: Activa GitHub Pages

1. Ve a **Settings** → **Pages** de tu repositorio
2. En "Build and deployment", selecciona **GitHub Actions**
3. ✅ Cada commit ahora se publicará en: `https://{username}.github.io/{repo-name}`

### Paso 3: Elige Tu Entorno de Desarrollo

#### Opción A: GitHub Codespaces (más rápido)

1. Abre tu nuevo repositorio en GitHub
2. Haz clic en **Code** → **Codespaces** → **Create codespace on main**
3. Espera a que el devcontainer termine la configuración

#### Opción B: VS Code Local

1. Abre VS Code
2. Ejecuta el comando: `Git: Clone` → `Clone from GitHub`
3. Selecciona tu nuevo repositorio
4. Cuando se te solicite, instala las **extensiones recomendadas**

### Paso 4: Ejecuta el Agente de Configuración

En el panel de Chat:

```
/setup
```

El agente va a:
- Detectar tu entorno
- Instalar dependencias faltantes
- Iniciar el servidor de desarrollo

✅ **Éxito:** ¡La app está corriendo en tu navegador!

---

## 📚 Entendiendo la Ingeniería de Contexto

La ingeniería de contexto es cómo le enseñas a la IA sobre tu código específico. Esto hace que las sugerencias de Copilot sean más precisas y relevantes.

### Tarea 1: Generar Instrucciones del Workspace

Las instrucciones guían todas las interacciones agénticas, haciéndolas eficientes y confiables.

**Pasos:**

1. Ejecuta el comando: `Chat: Generate Workspace Instructions File`
2. Espera a que el agente analice tu código
3. Revisa las instrucciones generadas (¡probablemente demasiado detalladas!)
4. Continúa con:
   ```
   Compress down by half and add a mandatory development checklist 
   (lint, build, test) to the top
   ```
5. **Haz commit** del archivo de instrucciones

✅ **Resultado:** Todas las futuras solicitudes tienen un mapa básico de tu workspace.

---

### Tarea 2: Background Agents para Trabajo Paralelo

Los background agents se ejecutan en git worktrees aislados — perfectos para tareas que no necesitan supervisión.

**Pasos:**

1. Haz clic en `+` en el Chat → **New background agent**
2. Ingresa:
   ```
   Add linting rules for unused vars and async/await usage; fix any errors
   ```
3. Déjalo ejecutarse, luego **Revisa** y **Aplica** los cambios
4. Haz clic derecho en la sesión para eliminarla cuando termines

**Prueba un Cloud Agent también:**

1. Haz clic en `+` → **New cloud agent**
2. Ingresa:
   ```
   Make the README more engaging as a landing page to the project
   ```

✅ **Resultado:** Reglas de linting agregadas, errores corregidos, README mejorado — ¡todo fusionado de vuelta a main!

---

### Tarea 3: Explora las Instrucciones Existentes

Tu repositorio viene con instrucciones preconfiguradas que ayudan a la IA a entender el proyecto.

#### Instrucciones de Utilidades CSS

📄 Consulta `.github/instructions/css-utilities.instructions.md`

Estas documentan las clases CSS personalizadas estilo Tailwind disponibles en este proyecto Blazor.

> 💡 **Opcional:** Elimina el texto principal y vuelve a ejecutar el prompt para ver cómo lo genera

#### Instrucciones de Diseño Frontend

📄 Consulta `.github/instructions/frontend-design.instructions.md`

Las instrucciones de "sin gradientes morados" desafían al agente a pensar como un diseñador.

> 💡 **Piensa en:** ¿Qué otros sesgos de la IA podrías desafiar y redirigir?

---

## ✅ ¡Parte 1 Completa!

Aprendiste cómo:
- Configurar tu entorno de desarrollo
- Generar y refinar instrucciones del workspace
- Usar background y cloud agents para trabajo paralelo
- Entender archivos de instrucciones existentes
