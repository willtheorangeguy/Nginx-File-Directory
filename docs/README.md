# Nginx File Directory — Documentation

A static reproduction of the Nginx directory listing page. One HTML file of 21 lines, no
icons, no stylesheet, no scripts.

```
Nginx-File-Directory/
├── docs/
│   ├── README.md          this page
│   ├── quickstart.md      see it, then make it yours
│   ├── installation.md    there is nothing to install
│   ├── usage.md           editing the listing
│   ├── configuration.md   the line format for folders and files
│   ├── architecture.md    why it is a <pre> block, not a table
│   ├── deployment.md      web server, Docker, GitHub Pages
│   ├── faq.md             automatic listings, alignment, what it is for
│   ├── troubleshooting.md broken alignment, wrong links
│   ├── roadmap.md         known gaps and non-goals
│   └── legal/             privacy policy and terms
├── index.html             the entire application
└── Dockerfile             Nginx serving the static file
```

## Pages

- [Quickstart](./quickstart.md) — open it, edit it, publish it
- [Installation](./installation.md) — clone or download; there is no install step
- [Usage](./usage.md) — setting the title and adding entries
- [Configuration](./configuration.md) — the line format for folders and files
- [Architecture](./architecture.md) — why the layout is preformatted text
- [Deployment](./deployment.md) — your server, Docker, or GitHub Pages
- [FAQ](./faq.md) — automatic listings, alignment, real use cases
- [Troubleshooting](./troubleshooting.md) — misaligned columns, dead links
- [Roadmap](./roadmap.md) — known gaps and deliberate non-goals

## Two things to know

**It is one file and nothing else.** Unlike its Apache and Chrome siblings there are no icons
to copy and no stylesheet to link. Deploying it is copying `index.html`.

**Alignment is literal whitespace.** The listing lives inside a `<pre>` block, so the columns
line up because of the actual spaces you typed. An editor that trims trailing whitespace or
reformats HTML will visibly break the layout — see [Usage](./usage.md).

## Related

The same idea in two other styles:
[Apache](https://github.com/willtheorangeguy/Apache-File-Directory) and
[Chrome](https://github.com/willtheorangeguy/Chrome-File-Directory).
