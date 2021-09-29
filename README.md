# nginx File Directory
The basic nginx file directory page, as a simple HTML page.

## Instructions
In order to change the `index.html` file, replace the following with their real values:

**Basics:**
```html
<title id="title">Index of example</title>
```
- Update the `example` placeholder text with the actual directory name. This will be the title of the webpage. 
```html
<h1 id="header">Index of :\directory</h1>
```
- Update the `:\directory` placeholder text with the actual directory path. This will be the title displayed on the page.  
```html
<div id="parentDirLinkBox" style="display:none">
  <a id="parentDirLink" href="up/level" class="icon up">
    <span id="parentDirText">[parent directory]</span>
  </a>
</div>
```
- If this is a directory inside of another directory, remove the `style="display:none"` placeholder. 
- Change the `up/level` with the actual link to the folder above.

**For a File or Folder:**
```html
<tr>
    <td data-value="File"><a class="icon file" draggable="true" href="link/to/file">File.txt</a></td>
    <td class="detailsColumn">File</td><td class="detailsColumn">0.00 MB</td><td class="detailsColumn">MM/DD/YY, HH:MM:SS PM</td>
  </tr>
```
- Replace the `"File"` placeholder value with the real name of the file. 
- Replace the `"link/to/file"` link with the actual link to the file. 
- Replace the `File.txt` placeholder name with the real name and extension of the file.
- Replace the `File` placeholder text with the actual file type.
- Replace the `0.00 MB` placeholder size with the real size of the file. 
- Replace the `MM/DD/YY, HH:MM:SS PM` placeholder date with the date the file was uploaded. 
- Add more of these rows as neccesary. 

## Credits
None of this would be possible without the [nginx Dev Team](http://nginx.org/en/docs/contributing_changes.html). Thanks to them for creating this. 

## nginx License
```
/* 
 * Copyright (C) 2002-2021 Igor Sysoev
 * Copyright (C) 2011-2021 Nginx, Inc.
 * All rights reserved.
 *
 * Redistribution and use in source and binary forms, with or without
 * modification, are permitted provided that the following conditions
 * are met:
 * 1. Redistributions of source code must retain the above copyright
 *    notice, this list of conditions and the following disclaimer.
 * 2. Redistributions in binary form must reproduce the above copyright
 *    notice, this list of conditions and the following disclaimer in the
 *    documentation and/or other materials provided with the distribution.
 *
 * THIS SOFTWARE IS PROVIDED BY THE AUTHOR AND CONTRIBUTORS ``AS IS'' AND
 * ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
 * IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
 * ARE DISCLAIMED.  IN NO EVENT SHALL THE AUTHOR OR CONTRIBUTORS BE LIABLE
 * FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
 * DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS
 * OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
 * HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
 * LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY
 * OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
 * SUCH DAMAGE.
 */
```
