# ptest

Placeholder todo app showing the round trip from **Claude Design** to **GitHub Pages**.

Live site: https://per-svensson.github.io/ptest/

## Repo layout

```
ptest.dc.html                The app — authored in Claude Design, committed as-is
support.js                   Runtime the design file loads
.github/workflows/pages.yml  On push to main: copies the source into a Pages site and deploys it
```

`ptest.dc.html` is published as `index.html`; nothing is compiled or bundled.

## One-time setup

1. Push these files to `main` (the old `index.html` boilerplate can be deleted).
2. **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. Push again, or run *Actions → Deploy to GitHub Pages → Run workflow*.

## Day-to-day loop

1. **Design** — open the Claude Design project and change the app by prompt or direct edit.
2. **Sync** — download the project and copy the changed files into your clone, or use *Handoff to Claude Code* and ask it to commit.
3. **Commit** — `git add -A && git commit -m "Update from Claude Design" && git push`.
4. **Publish** — the workflow runs automatically; the site updates in about a minute.

## Going further

- **One command:** with Claude Code in your clone, `claude "apply the latest Claude Design handoff and push"` covers steps 2–3.
- **Previews:** add a `pull_request` trigger to review design changes before merging to `main`.
