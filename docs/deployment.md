# Nginx File Directory — Deployment

## On your own web server

1. Download the latest `.zip` from
   [GitHub Releases](https://github.com/willtheorangeguy/Nginx-File-Directory/releases/latest),
   or clone the repository.
2. Copy `index.html` to the directory you want listed.
3. Edit it to describe the files that are actually there — see [Usage](./usage.md).
4. Upload.

That is the whole deployment. There are no icons and no stylesheet to bring along, which makes
this the simplest of the three file-directory projects to install.

## With Docker

```bash
docker pull ghcr.io/willtheorangeguy/nginx-file-directory:main
docker run -d -p 8000:80 ghcr.io/willtheorangeguy/nginx-file-directory:main
```

Then <http://localhost:8000/>.

**The image name is lowercase.** GHCR requires it, so `Nginx-File-Directory` will not pull even
though that is the repository name.

## Building it yourself

```bash
docker build -t nfd .
docker run -d -p 8000:80 nfd
```

Useful for previewing your edited copy rather than the published one.

## GitHub Pages

`docs.yml` deploys on every push to `main`, keeping
<https://willtheorangeguy.github.io/Nginx-File-Directory/> current.

Forking and enabling Pages gives you the same for your own copy — a hosted listing with no
server to run, which is one of the more genuinely useful things this project is for.

## Automation

| Workflow             | Trigger        | Does                        |
| -------------------- | -------------- | --------------------------- |
| `docs.yml`          | push to `main` | Deploys to GitHub Pages     |
| `docker-publish.yml` | push to `main` | Builds and pushes to GHCR   |
| `gitleaks.yml`       | pushes and PRs | Scans for committed secrets |

## Nothing to configure

No environment variables, no database, no build step. Deployment is copying one file.
