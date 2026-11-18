# open

One `https://` link that opens the right place on each device. Claude's apps only make `https://` links tappable, so a link to the Gmail app (`googlegmail://…`) can't be tapped from a Claude chat. This page bridges it.

- Phone: opens the app (Safari may ask "Open in Gmail?"), with buttons as a fallback.
- Computer: goes straight to the web version.

```
https://akabigcat.github.io/open/#gmail=<threadId>
https://akabigcat.github.io/open/#app=<app url>&web=<https url>
```

Everything after `#` stays in the browser and is never sent to GitHub, so the page and its logs hold no IDs or data. App schemes and web hosts are allowlisted in `index.html` so the page can't redirect anywhere else.

Used by the skills in the private `brain` repo (see its `global/CLAUDE.md`, "Links").

> 2026-11-17: no longer the main route. Gmail links now use `gmail.app.goo.gl` (opens the app with no prompt); this page is the fallback. See `context/links.md` in the brain repo.
