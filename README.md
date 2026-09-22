# Figure Tools

A small, no-dependency, multi-page site for building publication-style scientific figures by hand. Everything runs in the browser — no build step, no server.

- **`index.html`** — home page describing the site, linking to both tools.
- **`timeline.html`** — study/trial **timeline diagrams**: custom scale unit & range, tick count, font size, a compressible timeline break, colored highlight regions, and colored vertical event markers.
- **`domains.html`** — **protein domain / structure organization maps**: protein residue range, backbone styling, per-domain start/end residue, name (with position above/below/inside and horizontal/vertical orientation), fill color, outline color/width/dash style, per-boundary-number label placement (above/below, horizontal/vertical), and one-click random styling for quick drafts.

Both tools render live to an SVG on the right and have an **Export as SVG** button.

## Run it locally
Just open `index.html` in any browser.

## Host it on GitHub Pages
1. Create a new repository on GitHub (e.g. `figure-tools`).
2. Add `index.html`, `timeline.html`, `domains.html` (and this `README.md`) to the repo — via the GitHub web UI ("Add file → Upload files") or:
   ```
   git init
   git add index.html timeline.html domains.html README.md
   git commit -m "Initial figure tools site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to "Deploy from a branch", pick branch `main` and folder `/ (root)`, then Save.
5. Wait a minute, then your site will be live at:
   `https://<your-username>.github.io/<your-repo>/`

## Editing further
Each page is self-contained — its controls panel, SVG rendering logic, and styling are all inline in that one HTML file — so you can tweak colors, defaults, or layout directly in `timeline.html` or `domains.html` without touching the other.
