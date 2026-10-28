# LinkXcel — standalone static site

Free backlink tools hub, built for profile backlink creators who run teams.
No backend, no login, no database, no paid service. Every tool runs in the
visitor's browser. No Blogger tags are used anywhere in this site.

## Deploy (GitHub Pages)

1. Put the contents of this folder at the root of a GitHub Pages repository
   (or any static host). There is no build step.
2. GitHub Pages serves `index.html` as the homepage automatically.
3. No environment variables, secrets, or server configuration are needed.

## Structure

- `index.html` — tools hub (search, category filters, 12 tool cards, Tool Notes,
  How It Works, FAQ, SEO meta + JSON-LD).
- `tools/<slug>.html` — one page per tool. Each page embeds that tool's
  original CSS/JavaScript (re-housed from its full HTML document into this
  page; see "Code gaps fixed" in the delivery report for the small repairs).
- `blog.html` — fetches the live Blogger JSON feed in the browser and lists
  every post except the 12 tool posts and the banner post, so new blog
  articles appear automatically. Shows "No blog articles yet" when the
  filtered list is empty, and a clear error message if the feed cannot load.
- `assets/logo.png`, `assets/favicon.png` — site logo and favicon.
- `redirects.json` — old Blogger URL → new page for every tool.

## Old → new URLs

See `redirects.json`. The old Blogger site is left untouched; if you want old
links to keep working, point each old tool post at its new page (or keep the
old site as an archive and link to the new hub from it).
