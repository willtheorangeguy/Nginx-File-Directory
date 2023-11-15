<!-- Logo -->
<h1 align="center">
  <img src="https://raw.githubusercontent.com/willtheorangeguy/Nginx-File-Directory/main/docs/images/logo.png" height="250px" alt="Nginx File Directory">
  <br>
  Nginx File Directory
  <br>
</h1>

<!-- Copy -->
<h4 align="center">The basic Nginx file directory page, as a simple HTML page.</h4>

<!-- Badges -->
<div align="center">
  <!-- Stability -->
  <img alt="Docker State" src="https://github.com/willtheorangeguy/Nginx-File-Directory/actions/workflows/docker-publish.yml/badge.svg">
  <!-- Stability -->
  <img alt="GitHub Pages State" src="https://github.com/willtheorangeguy/Nginx-File-Directory/actions/workflows/pages.yml/badge.svg">
  <!-- Gitleaks -->
  <img alt="Gitleaks State" src="https://github.com/willtheorangeguy/Nginx-File-Directory/actions/workflows/gitleaks.yml/badge.svg">
  <!-- Version -->
  <img alt="GitHub Version" src="https://img.shields.io/github/v/release/willtheorangeguy/Nginx-File-Directory">
  <!-- Issues -->
  <img alt="GitHub Issues" src="https://img.shields.io/github/issues/willtheorangeguy/Nginx-File-Directory">
  <!-- Pull Requests -->
  <img alt="GitHub Pull Requests" src="https://img.shields.io/github/issues-pr/willtheorangeguy/Nginx-File-Directory">
  <!-- Discord -->
  <img alt="Discord Server ID" src="https://img.shields.io/discord/962928811207430164">
  <!-- Downloads -->
  <img alt="Downloads" src="https://img.shields.io/github/downloads/willtheorangeguy/Nginx-File-Directory/total">
  <!-- Language Count -->
  <img alt="GitHub Languages" src="https://img.shields.io/github/languages/count/willtheorangeguy/Nginx-File-Directory">
</div>

<!-- Navigation -->
<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#download">Download</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#support">Support</a> •
  <a href="#contributing">Contributing</a> •
  <a href="#changelog">Changelog</a> •
  <a href="#credits">Credits & Contributors</a>
</p>

<!-- Screenshot(s) -->

![screenshot](https://raw.githubusercontent.com/willtheorangeguy/Nginx-File-Directory/main/docs/images/welcome.png)

## Key Features

- Basic file directory view.
- Name and upload date.
- Folder and file links.
- Compatible with all web servers and websites.
- Cross platform.

## Download

You can **[download](https://github.com/willtheorangeguy/Nginx-File-Directory/releases/latest) the source code** to modify the code and create your own file directory page.

You can also access the **production version the website**, available on all platforms, **[here](https://willtheorangeguy.github.io/Nginx-File-Directory/)**.

## How To Use

To clone and run this website, you'll need [Git](https://git-scm.com/downloads) installed on your computer. If you would rather not use Git, you can just download the code from GitHub above. From your command line:

```bash
# Clone this repository
$ git clone https://github.com/willtheorangeguy/Nginx-File-Directory.git

# Go into the repository
$ cd Nginx-File-Directory

# Run the webpage
$ index.html
```

You can also pull the [Docker](https://www.docker.com/) image from GitHub Packages. From your command line:

```bash
# Pull image
$ docker pull ghcr.io/willtheorangeguy/nginx-file-directory:main

# Run container
$ docker run -d -p 8000:80 ghcr.io/willtheorangeguy/nginx-file-directory:main

# Now, navigate to localhost in your browser to see the webpage
```

However, **to make this your own directory**, follow the steps below:

### Basics

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

### For a File or Folder

```html
<a href="folder/">folder/</a> MM-DD-YYYY HH:MM -
```

- Replace the `folder/` or `file/` link (between the `href="..."` tag) with the actual link to the file or folder.
- Replace the `folder/` or `file/` placeholder name (between the `<a>...</a>` tags) with the real name of the file or folder.
- Replace the `MM-DD-YYYY HH:MM` placeholder date with the date the file or folder was uploaded.
- Add more of these rows as necessary.

## Support

Further customization options for different types of files and folder structures can be found in [`CUSTOMIZATION`](https://github.com/willtheorangeguy/Nginx-File-Directory/blob/main/docs/CUSTOMIZATION.md). More documentation is available in the **[Documentation](https://github.com/willtheorangeguy/Nginx-File-Directory/tree/main/docs)** and on the **[Wiki](https://github.com/willtheorangeguy/Nginx-File-Directory/wiki)**. If more support is required, please open a **[GitHub Discussion](https://github.com/willtheorangeguy/Nginx-File-Directory/discussions/new)** or join our **[Discord](https://discord.gg/uQR9AfwBxU)**.

## Contributing

Please contribute using [GitHub Flow](https://guides.github.com/introduction/flow). Create a branch, add commits, and [open a pull request](https://github.com/willtheorangeguy/Nginx-File-Directory/compare).

Please read [`CONTRIBUTING`](CONTRIBUTING.md) for details on our [`CODE OF CONDUCT`](CODE_OF_CONDUCT.md), and the process for submitting pull requests to us.

## Changelog

See the [`CHANGELOG`](CHANGELOG.md) file for details.

## Credits

This software uses the following open source packages, projects, services or websites:

<!-- Credits Table -->
<table>
  <tr>
    <th align="center"><img src="https://applets.imgix.net/https%3A%2F%2Fassets.ifttt.com%2Fimages%2Fchannels%2F2107379463%2Ficons%2Fmonochrome_large.png?w=240&h=240&s=8a19bbc158996d098e2fb18310ba7f33" width="150" height="150" alt="GitHub"/></th>
    <th align="center"><img src="https://www.w3.org/assets/logos/w3c/w3c-no-bars.svg" width="150" height="150" alt="W3C"/></th>
    <th align="center"><img src="https://videos.w3schools.com/files/images/w3schools_logo_500_04AA6D.png" width="150" height="150" alt="W3Schools"/></th>
    <th align="center"><img src="https://www.logolynx.com/images/logolynx/06/0614238d6c1c151cf0f8201f4463cc8a.png" width="150" height="150" alt="Nginx"/></th>
  </tr>
  <tr>
    <td align="center">GitHub</td>
    <td align="center">W3C</td>
    <td align="center">W3Schools</td>
    <td align="center">Nginx</td>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/">Web</a> - <a href="https://github.com/pricing">Plans</a></td>
    <td align="center"><a href="https://www.w3.org">Web</a> - <a href="https://www.w3.org/support/">Donate</a></td>
    <td align="center"><a href="https://www.w3schools.com">Web</a> - <a href="https://www.w3schools.com/pro/index.php">Pro</a></td>
    <td align="center"><a href="https://nginx.org/">Web</a></td>
  </tr>
</table>

## Contributors

- [@willtheorangeguy](https://github.com/willtheorangeguy) - Sponsor on [PayPal](https://paypal.me/wvdg44?country.x=CA&locale.x=en_US)

## You may also like...

- [Running Calculator](https://github.com/willtheorangeguy/Running-Calculator) - A running speed calculator for any unit of distance.
- [PyWorkout](https://github.com/willtheorangeguy/PyWorkout) - A minimal CLI to keep you inspired during your workout! Easily used and customized, with support for multiple workout plans, different muscle groups and video workouts.
- [PyAvatar](https://github.com/willtheorangeguy/PyAvatar) - Easily display all of your creative avatars to keep them consistent across websites.

## License

**The website code in this repository is created by the [Nginx Development Team](https://nginx.org/) and maintained by the Nginx Authors. The server is released under the BSD 3-Clause License, and this project follows those licensing guidelines.**

This project is licensed under the [BSD 2-Clause “Simplified” License](https://choosealicense.com/licenses/bsd-2-clause/) - see the [`LICENSE`](LICENSE.md) file for details. See the [Privacy Policy](https://github.com/willtheorangeguy/Nginx-File-Directory/blob/main/docs/legal/PRIVACY.md) and [Terms and Conditions](https://github.com/willtheorangeguy/Nginx-File-Directory/blob/main/docs/legal/TERMS.md) for legal information.
