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
Hugo and deploys `public/` to GitHub Pages.

## Writing from a browser

The repository is compatible with GitHub's web editor and GitHub Pages CMS.
A `.pages.yml` file can be added to enable a browser-based editor with media
uploads.

## License

- Site content: CC BY 4.0
- Theme: Chirpy Hugo, MIT
