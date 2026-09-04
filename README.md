# The Watchtower — Swords of Secret Feedback Board

A static status page tracking community-reported bugs, UI feedback, accessibility issues,
and feature requests for Swords of Secret, meant to be shared with the dev team.

This folder is a complete, ready-to-host static site (just `index.html`, no build step).

## Option A — Netlify (fastest, zero setup)

1. Go to **https://app.netlify.com/drop**
2. Drag this whole folder onto the page.
3. Netlify publishes it instantly at a random URL like `https://random-name-123.netlify.app`.
4. To keep it and get a permanent, editable site, click **"Save to your team"** / sign in
   with a free Netlify account (GitHub, GitLab, email, etc.) right after the drop.
5. To publish updates later: either drag-and-drop the updated folder again (same site,
   new deploy), or connect the site to a GitHub repo (see Option B) for auto-deploys
   on every push.

## Option B — GitHub Pages (auto-publishes on every push)

1. Create a new repo on GitHub (e.g. `swords-of-secret-feedback`) — can be public or private
   (private repos need a paid plan for Pages; public is free).
2. From this folder, run:
   ```
   git init
   git add .
   git commit -m "Initial Watchtower feedback board"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch →
   Branch: main / (root)** → Save.
4. GitHub gives you a live URL, typically:
   `https://<your-username>.github.io/<repo-name>/`
5. From then on, every `git push` to `main` auto-publishes the updated page — no extra steps.

## Keeping it updated

Whenever there's a new round of feedback, ask Claude to regenerate `index.html` with the
latest items, then either:
- drag-and-drop the folder to Netlify again, or
- `git add index.html && git commit -m "Update feedback board" && git push`
  (auto-deploys via GitHub Pages).

If you'd like Claude to push updates directly in a future session, that needs either a
GitHub personal access token (repo scope) or `gh auth login` run once in that session —
happy to walk through either when you're ready.
