# Copilot Instructions

## Build, test, and lint commands

This repository currently has no build system, test runner, or linter configured (`package.json`, `requirements.txt`, and other tool manifests are not present).

Use these commands for local execution checks:

| Purpose | Command |
| --- | --- |
| Run project locally (static server) | `python -m http.server 8000` |
| Open entry page | Open `http://localhost:8000/index.html` in a browser |
| Run full test suite | Not configured |
| Run a single test | Not configured |
| Run lint | Not configured |

## High-level architecture

The project is a static frontend site with a single HTML entry point:

- `index.html` contains the full page structure and most UI decisions.
- Bootstrap CSS/JS are loaded directly from CDN in `index.html` (no local dependency management).
- Local media assets are referenced with relative paths (current example: `img/img_Boca.png`).
- `css/` and `js/` directories exist as extension points for future styles/scripts but are currently empty.

## Key conventions for this repository

- Keep paths browser-friendly and relative to the repository root (for example `img/...` from `index.html`).
- Prefer simple static-site changes first (direct HTML updates), since there is no framework, bundler, or module system.
- Keep user-facing text in Spanish to match existing content.
- When adding CSS/JS files, place them in `css/` and `js/` respectively and link them explicitly from `index.html`.

## Recomendaciones
- Cada vez que ingreses un nuevo código, inserta un comentario en español que explique las etiquetas utilizadas.
- Los ejemplos y el contenido en genral necesito que esten en español.
