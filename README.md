# Ivy PvE — Badlands website draft

A responsive static website for GitHub Pages.

## Pages
- `index.html` — landing page
- `news.html` — announcements and updates
- `server.html` — connection details and rules
- `items.html` — custom item catalogue with working category filters
- `vehicles.html` — vehicle showcase

## Publish on GitHub Pages
1. Create a new GitHub repository (for example `ivy-pve-website`).
2. Upload all files and folders in this package, keeping the `assets` folder.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose branch `main` and folder `/ (root)`, then save.
6. Wait for GitHub Pages to publish the site.

## Before publishing
Search for `ADD`, `TBD`, `PLACEHOLDER`, and sample copy in the HTML files. Replace the server IP, port, Discord invite, rules, dates, custom item details and vehicle specifications with real information.

The website uses no build tools or server-side code. The mobile navigation and item category filters are powered by `assets/site.js`. The header image is `assets/ivy-badlands.png`.


## Visual direction
The styling combines desert sand and burnt-orange highlights with charcoal/olive military panels, field-report labels, tactical line details and cinematic Badlands artwork. It is intended to feel like a military survival community site rather than a generic gaming template.
