# Nginx File Directory — FAQ

## Does it list my files automatically?

No. It is a hand-written listing that looks like Nginx output. Nothing scans a folder and
nothing keeps it in sync — it shows exactly what you typed.

A real Nginx server generates this per request from the filesystem. This is a static picture
of one.

## Then what is it for?

Anywhere you want the appearance of an Nginx index without a server producing one:

- A placeholder or landing page for a file drop.
- A curated list where you control what appears.
- A mock-up or screenshot.
- Serving a fixed set of files from static hosting like GitHub Pages, which cannot generate
  indexes at all.

## Why are my columns misaligned?

Because an editor reformatted the file. The listing sits in a `<pre>` block, so the columns
line up by literal whitespace — nothing computes them.

Turn off format-on-save and trailing-whitespace trimming before editing. See
[Usage](./usage.md).

## Why are there no icons?

Because Nginx does not emit any. Its `autoindex` output is name, date, and size in
preformatted text. The Apache and Chrome versions have icons because those pages do.

## Where is the stylesheet?

There isn't one, and that is faithful to the original. The page is unstyled preformatted text.

## Why does `docker pull` fail?

The image name is lowercase — `ghcr.io/willtheorangeguy/nginx-file-directory`. GHCR requires
lowercase, so the capitalised repository name will not work.

## The listing shows files that do not exist.

Leftover example lines. Deleting the ones you did not customise is a manual step nothing can
check for you.

## Do I need to copy anything besides `index.html`?

No. This is the simplest of the three — one file, no icons folder, no CSS.

## Is there a version for other servers?

Yes: [Apache](https://github.com/willtheorangeguy/Apache-File-Directory) and
[Chrome](https://github.com/willtheorangeguy/Chrome-File-Directory).

## Why is the project BSD 2-Clause when Nginx is BSD 3-Clause?

The upstream notice is preserved in `LICENSE_nginx.md` and in the header of `index.html`; the
project's own licence is BSD 2-Clause. Anything you redistribute that derives from the Nginx
design is governed by the upstream terms.

## Are the dates and sizes accurate?

They are plain text. Nothing computes them, so they are as accurate as you make them.
