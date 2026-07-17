# Cosine Website

Static marketing site for Cosine: electrified thermochemical reactor systems
with high-efficiency power electronics.

## Structure

```
index.html               Home (hero, stats, contact CTA, sponsors)
technology/index.html    Technology page  -> cosine-energy.com/technology/
applications/index.html  Applications page -> /applications/
news/index.html          News page -> /news/
team/index.html          Team page -> /team/
team.html                Redirect for the old /team.html URL
assets/css/style.css     All styling (brand colors defined in :root at the top)
assets/js/main.js        Nav behavior + scroll animations
assets/img/              Favicon, sponsor logos, team headshots, news photos
cosinelogo.svg           Nav logo
Sponsors/                Original sponsor logo files
```

Each page lives in its own folder so URLs stay clean (no `.html`, no `#`).
All asset and link paths are absolute (`/assets/...`), which assumes the site
is served from the domain root (true for cosine-energy.com).

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

