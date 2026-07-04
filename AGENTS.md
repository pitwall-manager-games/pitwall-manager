# Pitwall Manager — Agent Guide

## Commands (pnpm, not npm)

| Command | Action |
|---------|--------|
| `pnpm run dev` | Dev server with live reload for `src/` (hub landing page) |

## Project Structure

- **Vanilla JS** hub landing page at `src/`.
- **Individual games** in `games/` (gitignored). Each has its own GitHub repo.
- **Game Design Document:** `docs/GDD.md` — saga overview, links to individual game docs.

## Architecture Notes

- This repo is the **hub** for the Pitwall Manager game saga.
- Games in `games/` are gitignored and maintained in their own repos.
- No typechecking, no codegen, no migration tooling.

## Style Conventions

- No comments in code unless explaining a non-obvious decision.
- Variables named in camelCase; constants in UPPER_SNAKE_CASE.
- No semicolons (standard modern JS style).
- Prefer editing existing files over creating new ones.
