# Eco Fest: Celebrate — Jekyll site

Single-page Jekyll site for the Eco Festival run by Churches Together in Headington. Hosted on GitHub Pages.

## Run locally

This project requires **Ruby 3.1** (`github-pages` uses `jekyll-3.9` / `liquid-4.0` which are incompatible with Ruby 3.2+).

```bash
# First time: install Ruby 3.1 via Homebrew
brew install ruby@3.1

# Add to your shell so the right Ruby is used
export PATH="/opt/homebrew/opt/ruby@3.1/bin:$PATH"

# Install gems and serve
bundle install
bundle exec jekyll serve
```

Open <http://127.0.0.1:4000>.

> **Tip:** Add `export PATH="/opt/homebrew/opt/ruby@3.1/bin:$PATH"` to your `~/.zshrc` so you don't have to repeat it.

## Before going live — two manual steps

### 1. Add images

Drop these two files into `assets/images/`:

| File | Purpose |
|------|---------|
| `logo.png` | Churches Together in Headington logo (displayed in the hero) |
| `eco-fest-poster.jpg` | Event poster (used as the Open Graph / social media preview image) |

### 2. Set your GitHub Pages URL

Open `_config.yml` and fill in `url` and `baseurl`:

```yaml
url: "https://yourusername.github.io"
baseurl: "/eco-fest"   # the repo name; use "" if the repo is yourusername.github.io
```

## Deploy to GitHub Pages

Push to `main`. In the repo's **Settings → Pages**, set the source to **Deploy from branch → main → / (root)**.

GitHub Pages builds with its own Ruby 3.1 environment, so no local Ruby setup is needed for production.

## Updating event details

All event-specific values (date, venue, emails, deadline) live in `_config.yml` — edit once and they update everywhere on the page.

Stall and activity content lives in `_data/stalls.yml`.
