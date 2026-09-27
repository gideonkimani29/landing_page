# Josjos Glass Experts — Landing Page

A single-page, SEO + AEO-optimized landing page for Josjos Glass Experts (Eldoret, Kenya), built to deploy as-is on GitHub Pages.

## What's in here
```
index.html      → the whole site (HTML + CSS + a little JS)
assets/
  logo.jpeg     → brand logo (used as site logo + favicon + og:image)
  team.jpeg     → branded staff photo, used in the About section
robots.txt      → tells crawlers everything is indexable
sitemap.xml     → single-page sitemap for search engines
```

## Before you publish — 3 things to fix
1. **Replace the placeholder URL.** Search-and-replace
   `REPLACE-WITH-YOUR-GITHUB-USERNAME` in `index.html`, `robots.txt`, and
   `sitemap.xml` with your actual GitHub Pages URL once you know it (see
   step 2 below). This is what canonical tags, Open Graph tags, and the
   structured data point to — search engines and AI answer engines use it
   to attribute the content correctly.
2. **Confirm the service list.** The 8 services in the "What we do"
   section are my best guess from the branding, not confirmed facts.
   Edit the `<div class="service-card">` blocks in `index.html` to match
   what Josjos Glass Experts actually offers, and remove the windscreen
   card if that's not a real service.
3. **Swap in real photos when available.** `team.jpeg` is currently used
   in the About section. Real installation/work photos will help both
   conversion and SEO once you have them — add an `assets/gallery/`
   folder and a simple image grid section when ready.

## Deploy to GitHub Pages

1. **Create a new repo** on GitHub (e.g. `josjos-glass-experts`) — public,
   no README/gitignore needed since you already have files.
2. **Push these files to it:**
   ```bash
   cd josjos-glass-experts
   git init
   git add .
   git commit -m "Initial landing page"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/josjos-glass-experts.git
   git push -u origin main
   ```
3. **Enable Pages:** in the repo, go to **Settings → Pages**. Under
   "Build and deployment", set **Source** to `Deploy from a branch`,
   branch `main`, folder `/ (root)`. Save.
4. GitHub will give you a live URL, typically:
   `https://YOUR-USERNAME.github.io/josjos-glass-experts/`
   It can take a minute or two to go live the first time.
5. Go back and paste that exact URL over every
   `REPLACE-WITH-YOUR-GITHUB-USERNAME.github.io/josjos-glass-experts/`
   placeholder in `index.html`, `robots.txt`, and `sitemap.xml`, then
   commit and push again.

### Optional: custom domain
If you buy a domain (e.g. `josjosglass.co.ke`), add a `CNAME` file at
the repo root containing just the domain name, point the domain's DNS
`A`/`ALIAS` records at GitHub Pages per
[GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site),
and update the URLs in step 5 above to the custom domain instead.

## Why this page is set up for SEO **and** AEO

**SEO (search engines):**
- Descriptive `<title>` and meta description with the service + "Eldoret" keyword pair.
- `canonical`, Open Graph, and Twitter Card tags for clean link previews.
- Semantic HTML (`header`, `main`, `section`, `address`, heading hierarchy).
- Fast static page — no framework, no render-blocking scripts.

**AEO (AI answer engines — Google AI Overviews, ChatGPT/Perplexity browsing, voice assistants):**
- `LocalBusiness`/`HomeAndConstructionBusiness` JSON-LD with name, phone,
  address, and service area, so engines can extract exact facts rather
  than guessing from prose.
- `FAQPage` JSON-LD matched to real on-page Q&A copy — answer engines
  strongly favor content that's already phrased as a direct question and
  a direct, self-contained answer.
- Each FAQ answer is written to stand alone (no "as mentioned above")
  since answer engines often quote a single sentence out of context.

## Local preview
Just open `index.html` in a browser — no build step required. To preview
with a local server (recommended so relative paths behave exactly like
GitHub Pages):
```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```
