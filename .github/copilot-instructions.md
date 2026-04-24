# Project Guidelines

## Mandatory Checklist

- Before finishing work, run lint or diagnostics for the touched files and fix reported issues.
- Run `dotnet build SocOps/SocOps.csproj`.
- Run `dotnet test` when a test project exists; otherwise state that the workspace currently has no tests.

## Project Shape

- Work in `SocOps/`; treat `.solutions/` as reference checkpoints unless the task explicitly targets them.
- App startup is in `SocOps/Program.cs`; routing is in `SocOps/App.razor`.
- Main gameplay lives in `SocOps/Pages/Home.razor`, driven by `BingoGameService`.
- Keep UI in `SocOps/Components/`, types in `SocOps/Models/`, questions in `SocOps/Data/`, and rules in `SocOps/Services/BingoLogicService.cs`.
- Keep `SocOps/Services/BingoGameService.cs` focused on UI state, persistence, and change notifications.

## Conventions

- Use standard C# conventions and nullable-aware code.
- Components using `BingoGameService` must subscribe and unsubscribe from `OnStateChanged`.
- Reuse utilities in `SocOps/wwwroot/css/app.css` before adding new CSS.

## Design Guide

- Keep gameplay behavior unchanged during visual redesigns; treat styling and markup updates as presentation-only unless the task explicitly requests feature changes.
- Define and reuse CSS design tokens (colors, spacing, typography, shadows) in `SocOps/wwwroot/css/app.css`; avoid one-off inline styles.
- Preserve clear state signaling for bingo tiles (default, marked, free, winning) using multiple cues (color, contrast, iconography, or border treatment), not color alone.
- Use expressive, intentional visual direction per task (for example, themed palettes and typography), while maintaining readability on both desktop and mobile.
- Prefer transform/opacity-based animations for performance and keep motion meaningful (screen entrance, state celebration, interaction feedback).
- Verify responsive behavior at narrow widths (including 320px) so tile text remains legible and tap targets remain usable.
- Maintain accessible contrast and semantic controls (`button`, `aria-label`, `aria-pressed`) when restyling components.
- For new UI work, prioritize changes in these files: `SocOps/Components/StartScreen.razor`, `SocOps/Components/GameScreen.razor`, `SocOps/Components/BingoBoard.razor`, `SocOps/Components/BingoSquare.razor`, `SocOps/Components/BingoModal.razor`, and `SocOps/wwwroot/css/app.css`.

## References

- `README.md` for prerequisites and local commands.
- `workshop/GUIDE.md` and `workshop/01-setup.md` for lab context.
- `.github/instructions/css-utilities.instructions.md` for styling utilities.
- `.github/instructions/frontend-design.instructions.md` for UI redesign tasks.
