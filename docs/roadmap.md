# Nginx File Directory — Roadmap

Known gaps, observed from the repository. Limitations, not a schedule.

## Not gaps

**It does not generate listings.** Being a hand-written static page is the design. Adding
generation would need a server, which is the thing it is imitating rather than a copy of it.

**There are no icons and no stylesheet.** Nginx emits neither, so neither does this. Adding
them would make the page less faithful, not more useful.

Both recorded so nobody "fixes" them.

## Real gaps

**Whitespace alignment is fragile and nothing protects it.** The columns line up by literal
spaces inside a `<pre>` block, so any formatter that touches the file breaks the layout
visibly. There is no `.editorconfig` and no Prettier ignore rule to prevent it — adding either
would make the repository safe to open in a configured editor.

This is the most valuable change available here, because it is the failure people will
actually hit.

**Nothing validates the listing.** Links, dates, and sizes are hand-typed, with no check that a
line points at a file that exists.

**The example lines are a trap.** The shipped `index.html` includes samples, and forgetting to
delete them advertises files that are not there. Shipping them commented out would make the
mistake impossible.

**The title appears twice.** The `<title>` tag and the `<h1>` both carry the directory name,
and changing one without the other is easy to miss.

**No tests**, and none is obviously right for a 21-line static file — though a check that the
copyright headers survive would be cheap and would catch a real regression.

## Repository hygiene

**Per-repo issue templates override the org defaults.** `.github/ISSUE_TEMPLATE/` holds
Markdown templates predating the org-level YAML forms, and GitHub prefers local ones. Removing
them would inherit the shared set.

## Licensing note

The project is BSD 2-Clause while Nginx is BSD 3-Clause. The upstream notice is preserved in
`LICENSE_nginx.md` and in the header of `index.html`, which is the right arrangement — but
anyone redistributing material derived from the Nginx design is governed by the upstream terms.

## Non-goals

- **Being a real directory index.** Nginx already does that.
- **Icons, CSS, or JavaScript.** Each would make it less like the page it reproduces.
- **A build step.** The value is that deployment is copying one file.
