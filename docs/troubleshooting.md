# Nginx File Directory — Troubleshooting

## The columns are misaligned

The most common problem with this page specifically.

Alignment comes from literal spaces inside the `<pre>` block. An HTML formatter, a
prettifier, or format-on-save will reflow that content and the columns drift.

Fix:

1. Turn off format-on-save and any HTML formatter for this file.
2. Turn off trailing-whitespace trimming.
3. Use a monospace font so you can see what you are aligning.
4. Re-space the affected lines by hand.

Note that the example folder and file lines carry different amounts of spacing, because their
names differ in length. Copying a line means adjusting its spacing to match your filename.

## A link goes nowhere

Every link is hand-written and nothing validates it. Check the `href` matches the real
filename — including case, on a case-sensitive server — and that it is relative to where
`index.html` actually sits.

## The listing shows files that are not there

Leftover example lines. Delete every line you did not customise — see [Usage](./usage.md).

## The heading and the browser tab disagree

Two places carry the directory name: the `<title>` tag and the `<h1>`. Changing one and not
the other is easy to miss.

## The parent directory link is missing

It ships commented out. Remove the surrounding `<!--` and `-->` to enable it.

## `docker pull` fails with a name error

Use lowercase:

```bash
docker pull ghcr.io/willtheorangeguy/nginx-file-directory:main
```

GHCR requires lowercase image names.

## The container starts but the page is blank

Check the port mapping. The container serves on 80 internally; the documented command maps it
to 8000, so use <http://localhost:8000/>.

## GitHub Pages is not updating

`pages.yml` deploys on push to `main`. Check the Actions tab — the badge in the README
reflects the last run.

## The copyright headers disappeared

An aggressive formatter can strip leading comments. `index.html` opens with the Nginx notice
and the project's own; both are the attribution and should be preserved. Restore them from git
if they were removed.

## Dates and sizes are wrong

They are plain text and nothing computes them.
