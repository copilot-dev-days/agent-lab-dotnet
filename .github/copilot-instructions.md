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

## References

- `README.md` for prerequisites and local commands.
- `workshop/GUIDE.md` and `workshop/01-setup.md` for lab context.
- `.github/instructions/css-utilities.instructions.md` for styling utilities.
- `.github/instructions/frontend-design.instructions.md` for UI redesign tasks.
