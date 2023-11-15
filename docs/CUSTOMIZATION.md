# Nginx File Directory Customization

The Nginx File Directory has been designed to be heavily customizable. More file and folder listings can be added and directory paths can be changed. **Just search for and change the placeholder values in each code section.** Additionally, ensure that you have deleted all the extra file and folder rows that are unnecessary for your file listing, so not to confuse users.

All of these instructions require [a text editor](https://code.visualstudio.com/) to be installed.

## Basics

1. _Line 8_: Update the `directory` placeholder text between the `<title>...</title>` tags with the actual directory name. This will be the title of the webpage.

```html
<head>
  <title>Index of /directory</title>
</head>
```

2. _Line 10_: Update the `directory` placeholder text between the `<h1>...</h1>` tags with the actual directory path. This will be the title displayed on the page.

```html
<h1>Index of /directory</h1>
```

3. _Line 13_: If this is a directory inside of another directory, remove the `<!--` and `-->` to uncomment the link to the directory above the current directory.

```html
<!--<a href="../">../</a>-->
```

4. _Line 13_: If this is a directory inside of another directory, change the `../` between the `<a>...</a>` tags with the actual link to the folder above.

## For a Folder

```html
<a href="folder/">folder/</a> MM-DD-YYYY HH:MM -
```

- Replace the `folder/` link (between the `href="..."` tag) with the actual link to the folder.
- Replace the `folder/` placeholder name (between the `<a>...</a>` tags) with the real name of the folder.
- Replace the `MM-DD-YYYY HH:MM` placeholder date with the date the folder was uploaded. **Do not delete the spaces as they are necessary for spacing.**
- Add more of these rows as necessary.

## For a File

```html
<a href="file/">file/</a> MM-DD-YYYY HH:MM -
```

- Replace the `file/` link (between the `href="..."` tag) with the actual link to the file.
- Replace the `file/` placeholder name (between the `<a>...</a>` tags) with the real name of the file.
- Replace the `MM-DD-YYYY HH:MM` placeholder date with the date the file was uploaded. **Do not delete the spaces as they are necessary for spacing.**
- Add more of these rows as necessary.
