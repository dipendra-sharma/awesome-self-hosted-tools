# MkDocs with Material Theme - Static Site Generator

MkDocs is a fast, simple static site generator that's geared towards building project documentation. This setup uses the popular **Material for MkDocs** theme.

## Features
- Write documentation in Markdown
- Live preview with hot reloading
- Built-in search and navigation
- Responsive Material Design theme

## Quick Start
1. Add your Markdown files to the `docs/` directory.
2. Run the service:
   ```bash
   docker compose up -d
   ```
3. Open `http://localhost:8409` in your browser.

## Configuration
- Port: **8409** (maps to internal port 8000)
- Base image: `squidfunk/mkdocs-material`
- Documentation files mounted from `./docs`

## Useful Commands
- `mkdocs serve` – start a local preview server
- `mkdocs build` – build the static site into the `site/` directory

## License

MIT License

