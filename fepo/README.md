# 2026 FEPO Football Handicapping Challenge — site

A no-build static site: plain HTML/CSS/JS, no framework, no bundler.
Same pattern as Treadcap — push to GitHub, Netlify auto-deploys.

## Files

- `index.html` — main landing page (title bar + 3 buttons)
- `hanks-analytics.html` — gallery page, pulls image links from `content.json`
- `registration.html` — placeholder page for rules/sign-up info
- `content.json` — **the file you edit every week**

## Weekly update workflow

You should not need to touch any HTML/CSS to make routine updates. Just edit
`content.json`:

```json
{
  "welcomeMessage": "text shown under the title",
  "contestLink": { "label": "CONTEST LINK", "url": "..." },
  "hanksAnalytics": { "label": "HANKS ANALYTICS", "images": ["https://.../chart1.png"] },
  "registration": { "label": "REGISTRATION INFO", "url": "registration.html" }
}
```

- Add new chart/image URLs to the `images` array to have them show up on the
  Hanks Analytics page.
- Change `welcomeMessage` any time you want to refresh the greeting.
- Commit and push — Netlify redeploys automatically, usually within a minute.

## Deploying for the first time

1. Push this folder to a new GitHub repo.
2. In Netlify: **Add new site → Import an existing project** → pick the repo.
3. Build command: none. Publish directory: `/` (repo root).
4. Deploy. Netlify gives you a URL immediately; add a custom domain later if
   you want one.

## Still TBD

- Real Hanks Analytics images (currently an empty gallery with a placeholder
  message)
- Real Registration Info page content
- Final welcome message copy
