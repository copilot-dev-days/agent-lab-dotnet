<!-- l10n-sync: source-file="workshop/04-multi-agent.md" -->
# Parte 4: Desarrollo Multi-Agent

[🎮 Demo en Vivo](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/) • [📚 Guía del Lab](GUIDE.md) • [← Parte 3](03-quiz-master.md)

---

> ⏱️ **Tiempo:** ~20 minutos

Construye nuevas funcionalidades usando agentes especializados: agentes TDD para código confiable y agentes de diseño para UI hermosa.

---

## 🧪 Tarea 1: Modo Búsqueda del Tesoro (Guiado por TDD)

Agentes personalizados con handoffs dividen workflows complejos en pasos más pequeños, manteniéndote en control para decisiones críticas.

### Lo Que Vamos a Construir

Un nuevo modo **Scavenger Hunt**:
- Las mismas preguntas del bingo
- Mostradas como una lista simple con checkboxes
- Medidor de progreso en la parte superior
- Clic para marcar elementos como completados

### Pasos

#### Fase 1: Planificar

1. Inicia un nuevo Chat en **Plan Mode**
2. Ingresa:
   ```
   Add a new Scavenger Hunt mode: same questions, but shown as a 
   simple list with checkboxes and a progress meter
   ```
3. **Itera en el plan** — verifica que:
   - ✅ Agrega el modo a la pantalla de inicio
   - ✅ Crea un nuevo componente para la vista de lista
   - ✅ Incluye un indicador de progreso
   - ❌ No se excede con las funcionalidades

#### Fase 2: TDD Red (Escribir Pruebas que Fallan)

1. Selecciona el agente **TDD Red**
2. Haz clic en **Start**
3. Observa mientras escribe pruebas para:
   - Renderizado de componentes
   - Interacciones con checkbox
   - Cálculo de progreso
   - Gestión de estado

4. Revisa el **Test Explorer** de VS Code para ver las pruebas fallando

#### Fase 3: TDD Green (Hacer que las Pruebas Pasen)

1. Cuando Red termine, selecciona el agente **TDD Green**
2. Observa mientras:
   - Implementa el código mínimo para pasar las pruebas
   - Ejecuta pruebas después de cada cambio
   - Itera hasta que todas las pruebas pasen

#### Fase 4: Refactor (Limpiar)

1. Selecciona el agente **TDD Refactor**
2. Déjalo limpiar el código manteniendo las pruebas en verde

### Recuperación vía Checkpoint

Si algo sale mal:
1. Usa los **Checkpoints** del Chat para revertir
2. Regresa a antes de que "TDD Red" comenzara
3. Intenta de nuevo con prompts ajustados

> 💡 **Bonus:** Prueba **TDD Supervisor** para un flujo TDD completamente automatizado

✅ **Resultado:** ¡Una funcionalidad Scavenger Hunt completamente probada, construida con TDD disciplinado!

---

## 🎴 Tarea 2: Modo Baraja de Cartas (Guiado por Diseño)

Usa el agente **Pixel Jam** para enfocarte en la iteración de UI mientras construyes nuevas funcionalidades.

### Lo Que Vamos a Construir

Un nuevo modo **Card Deck Shuffle**:
- El jugador abre el juego
- Toca para obtener una carta aleatoria
- La carta gira con animación
- Muestra una pregunta para discutir

### Pasos

1. Inicia un nuevo Chat
2. Selecciona **Pixel Jam** como agente
3. Ingresa:
   ```
   New mode: Card Deck Shuffle. Every player opens the game, 
   taps, and gets a random card with a question
   ```
4. Observa mientras itera en la UI
5. Sigue refinando:
   ```
   Add a cool 3D flip animation when revealing the card
   ```
   ```
   Make the card styling match the cyberpunk theme
   ```
6. **Haz commit** cuando estés satisfecho

### Qué Hace Pixel Jam de Manera Diferente

- Se enfoca en el **diseño visual** primero
- Itera en **UI/UX** antes de la lógica
- Usa las instrucciones de diseño frontend
- Crea interfaces pulidas y animadas

---

## 🔍 Tarea 3: Agente de Revisión de UX

Combina herramientas MCP, workflows personalizados y aislamiento de subagentes para capacidades poderosas de revisión.

### Pasos

1. Inicia un nuevo Chat con **Pixel Jam**
2. Ingresa:
   ```
   Run review
   ```
3. Cuando se te solicite, haz clic en **Allow for this Workspace** para acceso a la herramienta Playwright
4. Observa mientras:
   - Toma screenshots de cada página
   - Analiza problemas de usabilidad
   - Verifica accesibilidad
   - Revisa consistencia visual

### Qué Se Revisa

| Categoría | Verificaciones |
|-----------|---------------|
| **Usabilidad** | Flujo de navegación, claridad de botones, feedback |
| **Accesibilidad** | Contraste de colores, navegación por teclado, lectores de pantalla |
| **Visual** | Consistencia, espaciado, alineación |
| **Interacción** | Áreas de toque, estados de hover, animaciones |

### Acciones de Seguimiento

Después de la revisión:
```
File the critical findings as GitHub issues
```
```
Fix the accessibility issues you found
```
```
Assign the navigation bug to a background agent
```

✅ **Resultado:** ¡Una revisión completa de UX con hallazgos accionables!

---

## 🎯 Desafíos Bonus

Si te queda tiempo, intenta estos:

| Desafío | Enfoque |
|---------|---------|
| Corregir problemas de UX | Delega a background o cloud agent |
| Múltiples temas | Agrega selector de tema a la pantalla de inicio |
| Compartir en redes | Agrega botón de compartir al estado de victoria |
| Tabla de posiciones | Rastrea y muestra puntajes altos |
| Efectos de sonido | Agrega retroalimentación de audio para interacciones |

---

## ✅ ¡Parte 4 Completa!

Aprendiste cómo:
- Usar agentes TDD para desarrollo guiado por pruebas
- Construir funcionalidades con el ciclo Red-Green-Refactor
- Usar agentes enfocados en diseño como Pixel Jam
- Ejecutar revisiones completas de UX
- Combinar múltiples agentes para workflows complejos

---

## 🎉 ¡Workshop Completo!

¡Felicidades! Completaste el VS Code GitHub Copilot Agent Lab.

### Lo Que Construiste

- ✅ Una app Social Bingo completamente rediseñada
- ✅ Temas de quiz personalizados
- ✅ Modo Scavenger Hunt (construido con TDD)
- ✅ Modo Card Deck Shuffle (guiado por diseño)

### Lo Que Aprendiste

1. **Ingeniería de Contexto** — Enseñándole a la IA sobre tu código
2. **Primitivas Agénticas** — Background, cloud y agentes personalizados
3. **Desarrollo Design-First** — Iteración de UI con asistencia de IA
4. **Desarrollo Guiado por Pruebas** — Código confiable con agentes TDD

### Sigue Adelante

- 📺 [VS Code en YouTube](https://www.youtube.com/code)
- 📖 [VS Code Copilot Docs](https://code.visualstudio.com/docs/copilot/overview)
- 🌟 [Awesome Copilot](https://github.com/github/awesome-copilot)
