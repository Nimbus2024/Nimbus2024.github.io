# MBlog

Personal blog built with [Hugo](https://gohugo.io/) and the
[Stack](https://github.com/CaiJimmy/hugo-theme-stack) theme, deployed to
GitHub Pages.

## Requirements

- Hugo extended 0.170.1 or newer
- Dart Sass 1.108.2 or newer (`sass` on `PATH`, or set `DART_SASS_BINARY`)

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
- Pages (about, archives, search): `content/page/`
- Avatar and processed images: `assets/img/`
- Static images (including post uploads): `static/images/posts/`

Post front matter uses Hugo conventions: `title`, `date`, `slug`,
`categories`, `tags`, `description`, `math`, `comments`, `draft`.

## Deployment

Push to `main`; `.github/workflows/pages-deploy.yml` builds the site with
Hugo and deploys `public/` to GitHub Pages.

## Writing from a browser

The repository is compatible with GitHub's web editor and GitHub Pages CMS.
A `.pages.yml` file can be added to enable a browser-based editor with media
uploads.

## License

- Site content: CC BY 4.0
- Theme: Stack, GPL-3.0-only
