# AGENTS.md

This is a small static testing site for externally loaded Activenow scripts.
It is deployed automatically with GitHub Pages, so keep it as plain static
HTML/CSS/JS unless the task explicitly says otherwise.

## Project Shape

- `index.html` is the landing page.
- `page1.html` tests an Activenow signup table with LiveKid enabled.
- `page2.html` tests an Activenow signup table without LiveKid.
- Tailwind is loaded from CDN for quick styling.
- The "Fetch fresh & reload" button reloads the current page while cache-busting
  external scripts and styles.

## Editing Rules

- Keep changes small, direct, and readable.
- Do not introduce a build step, package manager, framework, or generated assets.
- Preserve GitHub Pages compatibility.
- Preserve the page navigation and fresh reload helper unless the task explicitly
  asks to change them.

## Activenow Script Swaps

When asked to use supplied Activenow scripts, replace only the externally loaded
Activenow script block, line by line, exactly as provided.

The correct place is inside:

```html
<div class='activenow-table-container'>
```

Replace the Activenow `<script ...></script>` there. Do not move it elsewhere.
Do not touch the Tailwind CDN script in `<head>`. Do not touch the fresh reload
helper script near the bottom of the page.

Keep the surrounding test markup intact unless the task explicitly includes new
markup for it.
