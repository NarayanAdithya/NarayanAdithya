# SEO Strategy — Get narayanadithya.github.io/NarayanAdithya Ranking #1

> **Owner:** Adithya Narayan
> **Site:** https://narayanadithya.github.io/NarayanAdithya/
> **Goal:** Rank #1 on Google for "Adithya Narayan" and related long-tail keywords
> **Status:** 🔴 Not indexed / not ranking

---

## Context

"Adithya Narayan" is a competitive name. Major competitors in search results include:

- **Aditya Narayan** — Bollywood singer, 4M+ Instagram followers, dominates page 1
- **Adithya Narayan (CMU)** — Researcher at Carnegie Mellon, Google Scholar profile
- **Adithya Narayan (LinkedIn employee)** — UIUC grad, LinkedIn profile ranks high
- Multiple RocketReach, ZoomInfo, and other aggregator pages

**Strategy:** Own long-tail keywords first ("Adithya Narayan software engineer", "Adithya Narayan ION Trading", "Adithya Narayan Kerala"), then build authority to compete for the bare name.

---

## Task List for Claude Code

Use this file as a reference when making changes to the repository. Each task is a discrete, implementable change.

---

### Task 1: Add SEO Meta Tags to `index.html`

Add the following inside `<head>`:

```html
<!-- Primary Meta Tags -->
<title>Adithya Narayan | Software Engineer & Security Specialist — ION Trading</title>
<meta name="description" content="Adithya Narayan — Software Engineer at ION Trading with 3+ years in test automation, security operations, performance engineering, and full-stack development. Based in Kozhikode, Kerala. Python, DevOps, InfoSec.">
<meta name="keywords" content="Adithya Narayan, software engineer, ION Trading, Python developer, DevOps, security, automation, Kerala, VIT Vellore, FX trading, Jenkins, Docker, Flask">
<meta name="author" content="Adithya Narayan">
<meta name="robots" content="index, follow">

<!-- Canonical URL -->
<link rel="canonical" href="https://narayanadithya.github.io/NarayanAdithya/">

<!-- Open Graph / Social Sharing -->
<meta property="og:type" content="website">
<meta property="og:url" content="https://narayanadithya.github.io/NarayanAdithya/">
<meta property="og:title" content="Adithya Narayan | Software Engineer & Security Specialist">
<meta property="og:description" content="3+ years building, breaking, and securing mission-critical FX trading systems at ION Trading. Automation, security, DevOps, and AI.">
<meta property="og:image" content="https://narayanadithya.github.io/NarayanAdithya/app/static/img/adithya.JPG">
<meta property="og:locale" content="en_IN">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Adithya Narayan | Software Engineer & Security Specialist">
<meta name="twitter:description" content="3+ years building, breaking, and securing mission-critical FX trading systems at ION Trading.">
<meta name="twitter:image" content="https://narayanadithya.github.io/NarayanAdithya/app/static/img/adithya.JPG">

<!-- Geo Tags (helps local search) -->
<meta name="geo.region" content="IN-KL">
<meta name="geo.placename" content="Kozhikode, Kerala">
```

**Notes:**
- Replace the `og:image` and `twitter:image` URLs if you have a higher-res social preview image (ideally 1200x630px)
- If the site already has a `<title>` tag, replace it — don't add a second one

---

### Task 2: Add Structured Data (JSON-LD)

Add this script tag inside `<head>` or at the end of `<body>`. This tells Google exactly who you are:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Adithya Narayan",
  "url": "https://narayanadithya.github.io/NarayanAdithya/",
  "image": "https://narayanadithya.github.io/NarayanAdithya/app/static/img/adithya.JPG",
  "jobTitle": "Software Developer",
  "worksFor": {
    "@type": "Organization",
    "name": "ION Trading India Pvt. Ltd."
  },
  "alumniOf": {
    "@type": "CollegeOrUniversity",
    "name": "Vellore Institute of Technology"
  },
  "knowsAbout": ["Python", "DevOps", "Security", "Test Automation", "Jenkins", "Docker", "Flask", "Foreign Exchange Trading Systems"],
  "sameAs": [
    "https://www.linkedin.com/in/adithya-narayan-3747081a3/",
    "https://github.com/NarayanAdithya",
    "mailto:adithyanarayan1234@gmail.com"
  ],
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Kozhikode",
    "addressRegion": "Kerala",
    "addressCountry": "IN"
  }
}
</script>
```

---

### Task 3: Create `sitemap.xml`

Create a file called `sitemap.xml` in the **repository root** (so it's served at `narayanadithya.github.io/NarayanAdithya/sitemap.xml`):

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://narayanadithya.github.io/NarayanAdithya/</loc>
    <lastmod>2026-04-06</lastmod>
    <changefreq>monthly</changefreq>
    <priority>1.0</priority>
  </url>
</urlset>
```

**Notes:**
- Update `<lastmod>` to the current date whenever you push changes
- If you add a blog or more pages later, add them as additional `<url>` entries

---

### Task 4: Create `robots.txt`

Create a file called `robots.txt` in the **repository root**:

```txt
User-agent: *
Allow: /

Sitemap: https://narayanadithya.github.io/NarayanAdithya/sitemap.xml
```

---

### Task 5: Add Semantic HTML Improvements

Review the site's HTML and ensure:

1. **There is exactly one `<h1>` tag** — it should contain "Adithya Narayan" (already looks correct)
2. **Section headings use proper hierarchy** — `<h2>` for major sections (Tech Stack, Journey, Projects, Demos), `<h3>` for subsections
3. **All images have descriptive `alt` attributes** — e.g., `alt="Adithya Narayan — Software Engineer"` for the profile photo, `alt="Python programming language logo"` for tech stack icons
4. **Anchor links have descriptive text** — avoid naked "Click here" links; use "View CELIS project on GitHub" style

---

### Task 6: Improve Page Performance

Google ranks faster pages higher. Check and fix:

1. **Compress images** — Run all images through a compressor (tinypng.com or `imagemin`). The profile photo and project screenshots should be under 200KB each
2. **Add `loading="lazy"` to images** below the fold (anything not visible on first screen load)
3. **Minify CSS and JS** if not already done
4. **Add `<meta name="viewport" content="width=device-width, initial-scale=1">** if missing (likely already present)

---

### Task 7: Add a 404 Page

Create a `404.html` in the repo root so broken links don't hurt SEO:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page Not Found — Adithya Narayan</title>
  <style>
    body { font-family: system-ui, sans-serif; display: flex; align-items: center; justify-content: center; min-height: 100vh; margin: 0; background: #0a0a0a; color: #e0e0e0; }
    .container { text-align: center; }
    h1 { font-size: 4rem; margin-bottom: 0.5rem; }
    p { color: #999; margin-bottom: 2rem; }
    a { color: #60a5fa; text-decoration: none; border: 1px solid #60a5fa; padding: 0.75rem 1.5rem; border-radius: 8px; }
    a:hover { background: #60a5fa; color: #0a0a0a; }
  </style>
</head>
<body>
  <div class="container">
    <h1>404</h1>
    <p>This page doesn't exist. But I do.</p>
    <a href="/NarayanAdithya/">Take Me Home</a>
  </div>
</body>
</html>
```

---

## Manual Tasks (Can't Be Automated via Claude Code)

These require browser access and account logins:

### M1: Submit to Google Search Console
1. Go to https://search.google.com/search-console/
2. Add property → URL prefix → `https://narayanadithya.github.io/NarayanAdithya/`
3. Verify via the HTML tag method (add the meta tag Google gives you to `<head>`)
4. Submit `sitemap.xml` under Sitemaps section
5. Request indexing for your main URL

### M2: Update External Profiles with Portfolio Link
Make sure these all point to `https://narayanadithya.github.io/NarayanAdithya/`:

- [ ] GitHub profile bio (currently points to Heroku — update it)
- [ ] LinkedIn website field
- [ ] LinkedIn featured section (add as a link)
- [ ] DevPost profile
- [ ] PyPI package (DankBot) — add homepage URL
- [ ] Any other profiles (Twitter/X, Hashnode, etc.)

### M3: Share the Site
Post about your portfolio on LinkedIn to generate initial traffic and social signals. Google notices when a URL gets shared and clicked.

---

## Long-Term Growth (Optional, High Impact)

### Blog Content
Add 2–3 blog posts to create more indexable pages:
- "How I Built Automation Infrastructure from Scratch at ION Trading"
- "Implementing MFA Solo — Lessons from a One-Person Security Project"
- "From College Hackathons to Enterprise FX Systems"

Each post naturally includes your name + keywords and gives Google more reasons to rank your site.

### Custom Domain (Strongly Recommended)
If you buy `adithyanarayan.dev` or `adithyanarayan.com`:
- Custom domains rank significantly better than `*.github.io` subpaths
- GitHub Pages supports custom domains natively (just add a CNAME file)
- Cost: ~$10-15/year

---

## Tracking Progress

After completing the tasks above:
1. Wait 1–2 weeks for Google to crawl
2. Search `site:narayanadithya.github.io` on Google — if results appear, you're indexed
3. Search "Adithya Narayan software engineer" — you should start appearing within 2–4 weeks
4. Search "Adithya Narayan" — realistic to reach page 1 in 2–3 months with backlinks and content

---

*Last updated: April 2026*