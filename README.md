# LEVELUP — Gamified Fitness Platform

Marketing website for LEVELUP, an AI-powered gamified fitness platform. Static HTML site, ready to host on GitHub Pages or any static host.

## Structure

```
index.html        redirect → Home.dc.html
Home.dc.html       landing page (problem, insight, feature highlights, waitlist)
Features.dc.html   feature deep-dive + embedded prototype
Company.dc.html    vision/mission/values, org chart, registration, legal & privacy
_ds/               Nocturne design system (styles + component bundle) — do not edit
support.js         runtime required by the .dc.html pages — do not remove
```

## Before you launch

Replace the prototype placeholder in `Features.dc.html`: find the `<!-- PROTOTYPE EMBED -->` comment and swap the iframe `src` and "Open in new tab" `href` (both currently `about:blank`) for your prototype's live URL.

The waitlist form (on Home/Features/Company) is a front-end stub — it shows a confirmation alert but doesn't send anywhere. Wire it to an email service (e.g. Mailchimp, Formspree, a serverless function) before relying on it to capture real signups.

## Deploying to GitHub Pages

1. Push this folder's contents to a repository.
2. Repo Settings → Pages → Deploy from branch → select `main` (or your default branch) and `/ (root)`.
3. The site publishes at `https://<username>.github.io/<repo>/`.

`.nojekyll` is included so GitHub Pages serves the `_ds/` folder as-is (GitHub's default Jekyll build ignores folders starting with `_`).

## Local preview

Any static server works, e.g.:

```
npx serve .
```

then open the printed local URL.
