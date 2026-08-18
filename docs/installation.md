# Nginx File Directory — Installation

There is no installation. It is one static HTML file — no build step, no dependencies, no
runtime.

## Get it

```bash
git clone https://github.com/willtheorangeguy/Nginx-File-Directory.git
cd Nginx-File-Directory
```

Or download the latest `.zip` from
[GitHub Releases](https://github.com/willtheorangeguy/Nginx-File-Directory/releases/latest).

## Run it

Open `index.html` in any browser. It works from the filesystem — nothing on the page fetches
anything.

## What you need to copy

Just `index.html`.

This is the simplest of the three file-directory projects: there are no icons and no
stylesheet, so the whole deployment is one file. Its
[Apache](https://github.com/willtheorangeguy/Apache-File-Directory) and
[Chrome](https://github.com/willtheorangeguy/Chrome-File-Directory) siblings both need an
`icons/` folder alongside; this one does not.

## Requirements

A text editor, to make the page describe your files rather than the examples. Turn off
format-on-save first — see [Usage](./usage.md).

## Container image

```bash
docker pull ghcr.io/willtheorangeguy/nginx-file-directory:main
docker run -d -p 8000:80 ghcr.io/willtheorangeguy/nginx-file-directory:main
```

The image name is lowercase; GHCR requires it. See [Deployment](./deployment.md).

## Next

[Quickstart](./quickstart.md), or [Usage](./usage.md) to start editing.
