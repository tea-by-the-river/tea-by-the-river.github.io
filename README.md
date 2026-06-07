# tea-by-the-river.github.io

Jekyll + Minima site for organizing tea party events, deployed to GitHub Pages.

## Local preview

```bash
source /opt/homebrew/opt/chruby/share/chruby/chruby.sh
chruby ruby-3.4.1
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000. If `bundle install` fails on `http_parser.rb`, try:

```bash
bundle exec jekyll serve --no-livereload
```

## Adding an event

Create `events/<slug>.md` with this front matter:

```yaml
---
layout: event
title: "Event Name"
date: 2026-07-18 15:00:00 -0500
location: Venue Name
maps_url: https://maps.google.com/?q=...   # optional
what: Tea and food description
luma_url: https://lu.ma/your-event-slug    # optional
---

Optional extra details here.
```

Push to `main` — GitHub Actions builds and deploys automatically.