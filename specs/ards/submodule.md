# ADR  
**App Project**  
**Date: 5/15/2025**

## Context / Problem  
The project involves multiple contributors working in separate team repositories. To maintain a clean architecture and promote separation of responsibilities while still allowing integration, we need a way to link the team’s codebase to the main project repository without duplicating or manually syncing code.

## Options Considered  
- Copy-pasting code from team repo into the project repo  
- Git subtree merging  
- Using Git submodules  
- Hosting shared code in a monorepo  

## Decision & Outcome  
We will use **Git submodules** to include the team repository as a subdirectory within the main project repository. This allows for clear separation of concerns while maintaining traceability and syncing updates via Git.

## Pros & Cons  

### Pros  
- Keeps team repos modular and independently version-controlled  
- Enables reuse without code duplication  
- Changes in the team repo can be selectively pulled into the project repo  

### Cons  
- Submodules require additional Git commands and care (e.g., `git submodule update`)  
- Developers must remember to initialize and update submodules when cloning  
- Conflicts can arise if the submodule pointer isn't maintained properly  
