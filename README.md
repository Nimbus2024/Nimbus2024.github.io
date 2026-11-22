# MBlog

Personal blog built with [Hugo](https://gohugo.io/) and
[chirpy-hugo](https://github.com/cpalau/chirpy-hugo), a Hugo port of the
Chirpy theme. Deployed to GitHub Pages.

## Requirements

- Hugo 0.150 or newer (extended recommended)
- Git (for `enableGitInfo` / last-modified dates)

The theme ships precompiled CSS and vendor assets, so Dart Sass and Node are
not needed to build the site.

## Local development

```bash
hugo server -D
```

Production build:

```bash
hugo --gc --minify
```

## Content

- Posts: `content/posts/`
- About: `content/about.md`
- Archives: `content/archives.md`
- Avatar and site images: `static/assets/img/`
- Post images: `static/assets/img/posts/` (or `static/posts/`)

Post front matter uses Chirpy-compatible fields: `title`, `date`, `slug`,
`categories`, `tags`, `description`, `math`, `comments`, `pin`,
`media_subpath`, `draft`.

## Deployment

Push to `main`; `.github/workflows/pages-deploy.yml` builds the site with
Hugo and deploys `public/` to GitHub Pages. Pull requests run
`.github/workflows/ci.yml`, which builds the site but does not deploy.

## Writing from a browser (Pages CMS)

This repository includes `.pages.yml` for [Pages CMS](https://pagescms.org/).
It edits `content/posts/`, `content/about.md`, and `content/archives.md`
directly in the GitHub repository and uploads images to
`static/assets/img/posts/`.

1. Open <https://app.pagescms.org> and sign in with GitHub.
2. Install the Pages CMS GitHub App on this repository only.
3. Open the repository in Pages CMS and start writing.
4. Saving creates a commit; GitHub Actions rebuilds and deploys the site.

Notes:

- `slug` becomes the filename (`content/posts/<slug>.md`) and therefore the
  URL (`/posts/<slug>/`). Avoid changing it after publishing.
- `draft: true` keeps a post out of the build until you turn it off.
- Use the rich-text Source mode for complex Markdown or LaTeX.
- Pages CMS writes dates with a fixed `+08:00` offset. A post dated in the
  future is excluded by Hugo until that time and the next build.
- Compress images and strip EXIF/GPS metadata before uploading; Pages CMS
  uploads the original file.

## Dependency updates

`.github/dependabot.yml` checks GitHub Actions weekly and the theme submodule
monthly. Review and merge those pull requests manually.

## License

- Site content: CC BY 4.0
- Theme: Chirpy Hugo, MIT
