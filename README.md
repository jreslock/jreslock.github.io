# jreslock.github.io

This repository contains the source code for my personal website, built with [Hugo](https://gohugo.io/) and deployed to GitHub Pages.

## Project Overview

This is a personal website/portfolio that includes:
- A resume section showcasing professional experience and skills
- A blog/article section for technical content
- An about page with personal information

The site uses the [Ananke theme](https://github.com/theNewDynamic/gohugo-theme-ananke) with some customizations for the resume layout.

## Development

### Prerequisites

- [Hugo Extended](https://gohugo.io/installation/) (version 0.145.0 or later)
- Git

### Local Development

To run the site locally:

```bash
# Clone the repository
git clone https://github.com/jreslock/jreslock.github.io.git
cd jreslock.github.io

# Start the Hugo development server
hugo server -D
```

The site will be available at [http://localhost:1313](http://localhost:1313).

### Adding Content

- **Blog posts**: Add new markdown files to `content/post/`
- **Resume updates**: Edit `content/resume/_index.md`
- **About page**: Edit `content/about/_index.md`

## Deployment

The site is automatically deployed to GitHub Pages using GitHub Actions whenever changes are pushed to the `main` branch. The workflow configuration is located in `.github/workflows/hugo.yaml`.

## Project Structure

- `config.toml`: Site configuration
- `content/`: All content for the site
  - `_index.md`: Homepage content
  - `about/`: About page content
  - `post/`: Blog articles
  - `resume/`: Resume content
- `layouts/`: Custom layouts that override theme defaults
  - `resume/`: Custom resume layout
- `static/`: Static assets (images, etc.)
- `themes/`: Contains the Ananke theme
- `public/`: Generated site (not checked into git)

## License

All content is copyright © Jason Reslock unless otherwise noted.