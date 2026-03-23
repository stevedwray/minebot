# Minebot agent instructions

When working in this repository:

1. Preserve the current build unless explicitly asked to refactor it.
2. Do not change project-wide configuration unless needed for the requested task.
3. Before making large edits, inspect the relevant existing files first.
4. Keep all implementations compatible with NeoForge 1.21.1 and Java 21.
5. Avoid adding autonomous command execution, generated script execution, or OP-dependent behavior.
6. Prefer an MVP path:
   - custom mod identity
   - simple bot entity
   - simple task enum
   - follow/stay/go-to
   - block mining
   - combat
   - only then planner integration
7. For git work:
   - create a feature branch for non-trivial changes
   - make small commits with clear messages
   - summarize what changed and what still needs testing
8. Do not vendor external reference repositories into this repo.
9. Treat this project as a private-server companion bot, not an admin tool.
