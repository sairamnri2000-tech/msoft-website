# MSOFT Technologies Website

Static website for MSOFT Technologies, hosted on GitHub Pages.

## Files

| File | Purpose |
|---|---|
| `index.html` | Home page (About, Services, How we work, Contact) |
| `privacy.html` | Privacy policy |
| `404.html` | "Page not found" page |
| `favicon.svg` | Browser tab icon (MSOFT logo mark) |
| `robots.txt` | Lets search engines index the site |
| `fetch_images.py` | Downloads the images into `images/` so the site doesn't depend on Pexels/Pixabay |

## Go live on GitHub Pages (test URL)

1. Run `python3 fetch_images.py` in this folder. This creates `images/` and updates `index.html`.
2. Create a public GitHub repo, for example `msoft-website`.
3. Upload all files and the `images/` folder to the repo root (don't upload `index.html.bak`).
4. In the repo, open **Settings → Pages**. Set Source to **Deploy from a branch**, Branch to `main` and folder to `/ (root)`, then save.
5. After 1–2 minutes the site is live at `https://<your-username>.github.io/msoft-website/`.

## Later: custom domain

1. Verify the domain first: **GitHub account Settings → Pages → Add a domain**.
2. At the domain registrar, add:
   - 4 A records for `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - A CNAME record: `www` → `<your-username>.github.io`
   - **Do not touch MX records** (email).
3. In **Repo Settings → Pages → Custom domain**, enter the domain. Once the certificate is ready (up to 24h), tick **Enforce HTTPS**.
4. Add a `sitemap.xml` with the final domain and submit it in Google Search Console.
5. Only after the new site works on HTTPS, delete the old GoDaddy website. Check what else is on that GoDaddy plan (domain, email) before cancelling it.

## Image credits

Photos from Pexels and Pixabay (free to use under their licenses).
