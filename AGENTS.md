# AGENTS.md

This is a small static testing site for externally loaded Activenow staging
scripts. It is deployed automatically with GitHub Pages from `main`, so keep it
as plain static HTML/CSS/JS unless the task explicitly says otherwise.

## Project Shape

- `index.html` is a clean landing page and should not load an Activenow embed.
- `page1.html` tests Group Cyclic Events Table.
- `page2.html` tests Camps.
- `page3.html` tests Group Onetime Events.
- `page4.html` tests Court reservations.
- `page5.html` tests Personal Cyclic Events.
- `page6.html` tests Trial Lessons.
- Tailwind is loaded from CDN for quick styling.
- The "Fetch fresh & reload" button reloads the current page while cache-busting
  external scripts and styles.

## Editing Rules

- Keep changes small, direct, and readable.
- Do not introduce a checked-in build step, package manager, framework, or
  generated assets.
- A temporary local generator is fine only when the final committed output is
  plain HTML in the current GitHub Pages structure.
- Preserve GitHub Pages compatibility.
- Preserve the page navigation and fresh reload helper unless the task explicitly
  asks to change them.
- Keep the navigation links consistent across `index.html` and all `page*.html`
  files.

## Activenow Script Swaps

When asked to use supplied Activenow snippets, replace the target page's current
Activenow embed with the new snippet exactly as provided.

- Delete obsolete snippets instead of leaving old embeds commented out, unless
  the task explicitly asks to preserve them.
- Put each snippet inside the page's main test area, below the page heading.
- Do not put Activenow snippets on `index.html`.
- Do not touch the Tailwind CDN script in `<head>`.
- Do not touch the fresh reload helper script near the bottom of the page.
