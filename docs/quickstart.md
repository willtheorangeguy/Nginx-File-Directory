# Nginx File Directory — Quickstart

## 1. See it

Live at <https://willtheorangeguy.github.io/Nginx-File-Directory/>, or locally:

```bash
git clone https://github.com/willtheorangeguy/Nginx-File-Directory.git
cd Nginx-File-Directory
```

Open `index.html` in a browser. No server needed.

## 2. Make it yours

The whole file is 21 lines. Open it in a text editor.

**Set the title and heading** — both say `Index of /directory` by default, and both need
changing.

**Add a line per entry** inside the `<pre>` block, following the examples:

```
<a href="notes.txt">notes.txt</a>                    08-17-2026 14:30                    1.1K
```

**Uncomment the parent link** if this listing sits inside another directory. It ships
commented out.

**Delete the example lines** you did not use — they point at files that do not exist.

## 3. Mind the whitespace

The columns align because of literal spaces inside the `<pre>` block. Nothing lays them out.

Turn off any "format on save" or trailing-whitespace trimming before editing, or the columns
will drift. See [Usage](./usage.md).

## 4. Publish

Copy `index.html` to your web server. That is the entire deployment — there are no icons and
no stylesheet to bring along.

Other options in [Deployment](./deployment.md).

## Try it in Docker

```bash
docker run -d -p 8000:80 ghcr.io/willtheorangeguy/nginx-file-directory:main
```

Then <http://localhost:8000/>. The image name is **lowercase** — GHCR requires it.

## Know this before you use it

It does not list a real directory. It shows exactly what you typed. See [FAQ](./faq.md).
