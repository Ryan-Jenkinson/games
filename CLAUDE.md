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

## Git — automatic backup

A `post-commit` hook auto-pushes every commit to `origin main`, so nothing is ever lost locally.

**After every change to any file, Claude must:**
1. Stage the changed files (`git add <files>`)
2. Commit with a clear message describing what changed and why
3. The push happens automatically via the hook — no manual push needed

Do this after each logical unit of work, not just at the end of a session. This ensures GitHub always reflects the latest state and provides a full history of every change made.

## Memory

Use the `.claude/` memory system to record:
- What has been built in each game/project (features, known bugs, decisions made)
- User preferences and feedback from the current project
- Any context that would help a future Claude instance pick up where this one left off

Update memory files whenever something significant is decided or completed.
