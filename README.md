# KX Game Studios website

The studio site, hosted on GitHub Pages. It is a Jekyll site with no plugins and no build step of its own: push to `main` and GitHub Pages builds and publishes it.

## Layout

| Path | What it is |
| --- | --- |
| `_config.yml` | Site name, tagline and the contact form address. |
| `index.html` | Home page. Lists every game automatically. |
| `games/<game>/` | One folder per game. Everything about a game lives here. |
| `contact/` | Contact form and its "message sent" page. |
| `_layouts/`, `_includes/` | Page templates: shared header and footer, game page, text page. |
| `css/site.css` | Site styles, built on the brand tokens. |
| `assets/` | The brand kit, unchanged. Read `assets/README.md` before changing how anything looks. |

## Add a game

1. Copy `games/_template/` to `games/<your-game>/`. The folder name becomes the URL: `/games/<your-game>/`. The template itself is not published, because its name starts with an underscore.
2. Edit `index.md`. The settings at the top control the page:
   - `title`, `tagline`: shown on the game page and on the home page card.
   - `order`: position on the home page, lowest first.
   - `app_store_url`, `play_store_url`: a button appears for each one that is set. With neither set, the game is shown as "Coming soon".
   - `icon`, `og_image`, `screenshots`: optional image files kept in the game's folder. Without an `icon`, the studio app icon is used.
   - `features`: the short cards under "What you do". Set `features_title` to change that heading.
   - The text below the settings is the "About the game" section.
3. Edit `privacy.md` (see below), and in it and `support.md` change `?game=your-game` to the folder name so the contact form preselects the game.

`games/blocks-of-the-ides/` is a complete example.

### Privacy policy

Each game has its own policy at `/games/<your-game>/privacy/`. Use that URL in the App Store and Play Store listings. On the site it is linked only from the footer of that game's pages, and it is marked `noindex` so search engines skip it.

`privacy.md` is a template with the parts to fill in marked in [square brackets]. Update `last_updated` whenever the policy changes.

### Other pages for a game

Add any other Markdown file to the game's folder, for example `support.md`, starting with:

```yaml
---
layout: game-page
title: Support
---
```

It is published at `/games/<your-game>/support/` and linked from the game's page under "More". Add `hidden: true` to keep a page out of that list.

## Contact form

The form posts to [FormSubmit](https://formsubmit.co), which forwards each message to an email address. No account is needed.

1. Set `contact_email` in `_config.yml`. While it is empty, the form shows a "not connected" note and the send button is disabled.
2. Publish, then send one test message. FormSubmit emails that address an activation link; messages are forwarded once it is clicked.

The address is visible in the page's HTML. After activation FormSubmit provides a random alias that can be put in `contact_email` in its place to keep the address private.

To use a different form service, change the `action` of the form in `contact/index.html`.

## Publish

In the GitHub repository, open Settings, then Pages, and set the source to "Deploy from a branch", branch `main`, folder `/ (root)`.

`url` and `baseurl` are deliberately not set in `_config.yml`: GitHub Pages fills them in, so the site works at `https://<org>.github.io/<repo>/` and at a custom domain without changes. If the published site ever loads without its styles, set `baseurl: "/<repo>"` in `_config.yml`.

## Preview locally

Needs Ruby 3 or newer (the Ruby that ships with macOS is too old).

```sh
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.
