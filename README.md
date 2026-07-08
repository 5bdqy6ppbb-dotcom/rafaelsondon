# Rafael J. Sondon — Personal Website

A single-page personal website for Rafael J. Sondon: attorney, real estate developer, and author of *The American Papers*.

Built as a self-contained static site — one `index.html` with inline CSS and JavaScript, plus one image. No build step, no dependencies.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The entire website (markup, styles, and scripts inline) |
| `american-papers-cover.jpg` | Book cover shown in the "The Book" section |
| `.nojekyll` | Tells GitHub Pages to serve files as-is (skip Jekyll processing) |

## Publishing with GitHub Pages

1. Create a new repository on GitHub and push this folder to it:
   ```bash
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git branch -M main
   git push -u origin main
   ```
2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Choose the **main** branch and the **/ (root)** folder, then **Save**.
5. After a minute, your site will be live at:
   `https://<your-username>.github.io/<your-repo>/`

> Tip: To use a custom domain (e.g. `rafaelsondon.com`), add it under **Settings → Pages → Custom domain**. GitHub will create a `CNAME` file in the repo automatically.

## Editing

Everything lives in `index.html`. Open it in any browser to preview locally (double-click the file), or run a simple local server:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Social preview

The Open Graph and Twitter meta tags in `index.html` reference `american-papers-cover.jpg` with a relative path. For richer link previews on some platforms, replace the `og:image` / `twitter:image` values with the full published URL once the site is live, e.g. `https://<your-username>.github.io/<your-repo>/american-papers-cover.jpg`.
