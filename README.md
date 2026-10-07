# juanagranadosr.github.io

Personal site — built with Jekyll, plain HTML/CSS/Markdown, no JS framework.

## Run it locally

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

If you edit `_config.yml`, restart the server (Jekyll only picks up config changes on restart).

## Structure

- `index.md`, `projects.md`, `research.md`, `cv.md`, `contact.md` — the main pages. Edit these directly, they're Markdown with a little HTML mixed in.
- `intuition-lab/` — the Intuition Lab landing page plus the three standalone interactive demos (self-contained HTML/JS files, untouched from the original).
- `_posts/` — blog posts (`YYYY-MM-DD-title.md`). The blog lives at `/blog/` but isn't linked in the nav yet. The placeholder post has `published: false` so it won't appear until you're ready — then just add real posts and link `/blog/` from `_config.yml`'s `nav` list whenever you want it live.
- `assets/images/photo.jpg` — swap this for an updated photo any time, same filename.
- `assets/files/resume.pdf` — the downloadable CV PDF linked from the CV page and footer.
- `_layouts/`, `_includes/`, `assets/css/main.css` — the design. One accent color + a few CSS variables at the top of `main.css` control the whole look, including a dark-mode variant.

## Deploying

A GitHub Actions workflow (`.github/workflows/pages.yml`) builds and deploys automatically on every push to `main`.

One-time setup on GitHub: in the repo's **Settings → Pages**, set **Source** to **GitHub Actions** (instead of "Deploy from a branch"). After that, every push to `main` redeploys the live site automatically.
