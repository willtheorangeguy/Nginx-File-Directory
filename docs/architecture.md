# Nginx File Directory — Architecture

## The whole application

```text
index.html      21 lines
Dockerfile      Nginx, serving that one file
```

No icons, no stylesheet, no scripts, no dependencies. This is the most minimal of the three
file-directory projects, because the page it imitates is the most minimal.

## A `<pre>` block, not a table

Apache and Chrome both render their listings as HTML tables. Nginx does not — its
`autoindex` output is preformatted text, with columns aligned by literal spaces.

This project reproduces that faithfully, which has one consequence that matters more than any
other: **whitespace is the layout**. Nothing computes column positions, so the alignment you
see is the alignment you typed.

That is why [Usage](./usage.md) opens by telling you to disable format-on-save. An HTML
prettifier will reflow the `<pre>` contents and the columns will visibly drift.

It also explains the absence of icons. Nginx does not emit them, so neither does this.

## Static means hand-maintained

Nothing reads a directory. Every line exists because someone typed it, and nothing validates
that a link resolves or a date is accurate.

| Property                    | Because                        |
| --------------------------- | ------------------------------ |
| Works from `file://`        | Nothing is fetched             |
| Deploys by copying one file | There is nothing to build      |
| Goes stale silently         | Nothing re-reads the directory |

A real Nginx server generates this per request. This is a picture of one.

## Upstream notices are in the file

`index.html` opens with two copyright headers: the Nginx one covering the original design, and
the project's own. Preserve both when editing — they are the attribution, and the full upstream
notice is in `LICENSE_nginx.md`.

## Docker

`Dockerfile` runs Nginx serving the static file — pleasingly circular, and convenience rather
than necessity. Any web server, or none, will do.

## Automation

| Workflow             | Purpose                                   |
| -------------------- | ----------------------------------------- |
| `docs.yml`          | Deploys to GitHub Pages on push to `main` |
| `docker-publish.yml` | Publishes the image to GHCR               |
| `gitleaks.yml`       | Scans for committed secrets               |

Dependabot updates Actions and the Docker base image. There are no application dependencies.

## No tests

None, and for a 21-line static file that is defensible — verification is opening it and
looking.
