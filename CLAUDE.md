# CLAUDE.md

## Project Overview

Nginx-File-Directory is a standalone HTML template replicating the Nginx file directory listing page. It's a single `index.html` file with no JavaScript—pure HTML/CSS designed to work on any web server.

## Repository Structure

```
index.html              # The core deliverable — single-file HTML template
Dockerfile              # nginx:stable container serving the template
package.json            # NPM metadata only (no dependencies)
.deepsource.toml        # DeepSource static analysis config
.github/workflows/      # CI: Docker publish, GitHub Pages deploy, Gitleaks
docs/                   # Usage, customization, legal docs
```

## Tech Stack

- **Source**: Pure HTML/CSS (no JS frameworks, no build step)
- **Container**: Docker with `nginx:stable` base image
- **Deployment**: GitHub Pages (auto-deploys on push to main) + GitHub Container Registry

## Development Workflow

There is no build step. Edit `index.html` directly, then test in a browser.

### Testing

No automated test suite exists. `npm test` exits with an error by design.

Manual testing checklist:
- Open `index.html` in Chrome, Firefox, and Edge
- Validate HTML via W3C validator
- Check accessibility basics

### Linting

No automated linter is configured. DeepSource runs Prettier formatting checks and Docker/JS analysis externally.

### Docker

```bash
docker build -t nginx-file-directory .
docker run -p 8080:80 nginx-file-directory
```

## Code Conventions

- **Indentation**: 4 spaces
- **Copyright headers**: Required in source files (Nginx Development Team + willtheorangeguy)
- **HTML style**: Keep layout/functionality as close to original Nginx design as possible
- **Versioning**: Semantic Versioning (v1.x.x), currently v1.2.0

## CI/CD

| Workflow | Trigger | Purpose |
|---|---|---|
| `docker-publish.yml` | Push, tag, PR, daily schedule | Build/push Docker images to GHCR |
| `pages.yml` | Push to main | Deploy to GitHub Pages |
| `gitleaks.yml` | Push/PR | Secret scanning |

## Key Files to Know

- `index.html` — The only source file. 22-line HTML template with placeholder file/folder entries.
- `docs/CUSTOMIZATION.md` — How to edit directory names, add files/folders, change formatting.
- `docs/USAGE.md` — Installation via GitHub download or Docker.
- `CONTRIBUTING.md` — Contribution guidelines and coding standards.
