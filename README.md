# Cosine Website

Static marketing site for Cosine: electrified thermochemical reactor systems
with high-efficiency power electronics.

## Structure

```
index.html            Landing page (hero, technology, applications, news, contact)
team.html             Team page (CEO, CTO, Advisor)
assets/css/style.css  All styling (brand colors defined in :root at the top)
assets/js/main.js     Nav behavior + scroll animations
assets/img/           Favicon and sponsor logos
cosinelogo.svg        Nav logo
Team/                 Team headshots
News/                 News section photos
Sponsors/             Original sponsor logo files
```

## Things to customize

- **Team bios**: `team.html` has draft bios for Calvin Lin (CEO), Connor
  Cremers (CTO), and Jonathan Fan (Advisor); refine as needed.
- **Stats**: the numbers in the stats strip on `index.html` (>95% efficiency,
  1,000°C+, zero emissions) are illustrative marketing copy. Adjust to your
  real figures.
- **Sponsor logos**: the "Supported by" strip on `index.html` shows the four
  program logos from `assets/img/sponsors/` (NSF Seed Fund, MIT Climate &
  Energy Prize, Stanford Doerr School of Sustainability, Stanford High Impact
  Technology Fund). They render grayscale and regain color on hover; per-logo
  heights are tuned in the sponsors block of `assets/css/style.css`.
- **Contact email**: currently `calvin@cosine-energy.com` throughout.
- **Colors**: edit the CSS variables at the top of `assets/css/style.css`.

## Deploying + connecting your Squarespace domain

This is a plain static site, so host it anywhere. Easiest options:

### Option A: Netlify (simplest)

1. Go to [netlify.com](https://netlify.com), sign up, and drag this whole
   folder onto the dashboard (or connect a Git repo).
2. In Netlify: **Domain settings → Add custom domain** → enter your domain.
3. In Squarespace: **Settings → Domains → (your domain) → DNS Settings**, then add:
   - `A` record: host `@`, value `75.2.60.5` (Netlify's load balancer)
   - `CNAME` record: host `www`, value `<your-site>.netlify.app`
4. Back in Netlify, enable HTTPS (automatic via Let's Encrypt).

### Option B: GitHub Pages (free)

1. Create a GitHub repo, push this folder, and enable **Settings → Pages**
   (deploy from the main branch, root).
2. In the Pages settings, set your custom domain.
3. In Squarespace DNS settings, add:
   - `A` records for host `@`: `185.199.108.153`, `185.199.109.153`,
     `185.199.110.153`, `185.199.111.153`
   - `CNAME` record: host `www`, value `<username>.github.io`

### Option C: Vercel / Cloudflare Pages

Both work the same way: import the folder or repo, add the custom domain, and
they'll show you the exact A/CNAME records to enter in Squarespace's DNS panel.

> **Note:** DNS changes can take up to 48 hours to propagate, though it's
> usually under an hour.

## Local preview

```
python -m http.server 4173
```

Then open http://localhost:4173.
