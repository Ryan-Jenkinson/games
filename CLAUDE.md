# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository purpose

This is a collection of browser-based games. Each game lives in its own subfolder (or as a standalone HTML file for simple single-file games).

## Running games

Open any `.html` file directly in a browser — no build step or server required:

```sh
open <game>/index.html
```

## Repository conventions

- **New game = new subfolder** (e.g. `snake/`, `chess/`) unless it's a single self-contained file
- Self-contained single-file games live at the repo root as `<name>.html`
- All assets (CSS, JS, images) for a game should live inside that game's subfolder
- No external dependencies or package managers — keep everything vanilla HTML/CSS/JS

## Git

Every commit auto-pushes to `origin main` via a `post-commit` hook.
