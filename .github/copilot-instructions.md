# Minebot repository instructions

This repository is a NeoForge 1.21.1 Minecraft mod written in Java 21.

## Project goals
- Build an embodied in-game bot for a private NeoForge server.
- The bot must be an actual in-world entity, not a chat assistant.
- The bot must not rely on OP permissions.
- Start with a minimal, safe MVP:
  - spawn bot
  - follow player
  - stay
  - go to target position
  - mine a specific block
  - attack a specific hostile mob
- The LLM is a planner only. It must never generate executable code for the game to run.
- Any future LLM output must be constrained to strict validated structured data, not arbitrary commands.

## Working style
- Make the smallest safe change that moves the project forward.
- Prefer simple, explicit code over clever abstractions.
- Do not introduce broad frameworks unless clearly justified.
- Do not add features that were not requested.
- Keep classes small and responsibilities clear.
- Explain tradeoffs briefly when proposing architecture.

## Technical constraints
- Use Java 21.
- Use the existing NeoForge Gradle project layout.
- Keep secrets out of git.
- Prefer dependency usage or clean reimplementation over copying external project code.
- Keep reference repos out of this repository.

## Initial architecture direction
- Separate the project into:
  - embodiment / entity layer
  - task / controller layer
  - planner / LLM integration layer
- The embodiment layer must work without any LLM integration.
- The first milestone is a bot entity that can be spawned and can follow/stay reliably.

## Output expectations
- When suggesting file changes, name the files clearly.
- Prefer concrete code changes over vague advice.
- Prefer stepwise implementation plans.
- When uncertain, keep the implementation minimal and leave TODO comments rather than inventing behavior.
