# Nginx File Directory — Usage

The page is a `<pre>` block containing one line per file or folder. Using it means editing
those lines to describe your directory.

You need a text editor — with automatic formatting **turned off**. See below.

## 1. Set the title and heading

Two places say `Index of /directory`: the `<title>` tag and the `<h1>`. Change both, or the
browser tab and the page will disagree.

## 2. Uncomment the parent link if you need it

```html
<!--<a href="../">../</a>-->
```

Ships commented out. Remove the `<!--` and `-->` if this listing sits inside another
directory. Leave `../` as the target to keep the link relative.

## 3. Add a line per entry

```text
<a href="folder/">folder/</a>                                           MM-DD-YYYY HH:MM                    -
<a href="file">file</a>                                              MM-DD-YYYY HH:MM                    -
```

For each line, replace:

| Placeholder                     | With                                                 |
| ------------------------------- | ---------------------------------------------------- |
| The text between the `<a>` tags | The display name — folders conventionally end in `/` |
| The `href`                      | The real path                                        |
| `MM-DD-YYYY HH:MM`              | The modified date                                    |
| `-`                             | The size, or leave as a dash for folders             |

Nginx's own format is name, date, size — no icon column and no description. That is why this
page has neither.

## 4. Whitespace is the layout

This is the one thing that makes editing this page different from its siblings.

The columns line up because of the **literal spaces** between the link and the date, and
between the date and the size. Nothing computes the alignment — there is no table and no CSS.

So before editing:

- Turn off **format on save** and any HTML formatter. A prettifier will reflow the `<pre>`
  contents and visibly break the columns.
- Turn off **trailing whitespace trimming**.
- Use a monospace font, or you will not be able to see what you are aligning.

Note also that the folder and file example lines use different amounts of spacing, because the
names differ in length. Copying a line means adjusting its spacing to match your filename.

## 5. Delete the leftovers

The shipped file contains example lines. **Delete every one you did not customise**, or your
listing advertises files that do not exist. Nothing checks this.

## 6. Publish

Copy `index.html` to your server. That is the whole deployment — see
[Deployment](./deployment.md).

## What it does not do

It does not read a directory. Nothing scans a folder and generates lines — the listing is
whatever you typed, and it goes stale the moment the real directory changes.
