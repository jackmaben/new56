# Project conventions — OptimizeTechStudio site

## Content rules (strict)
- **Never add copy from my side.** No invented headings, taglines, descriptions, trust lines, stats, or CTA text. All wording comes from the user or from text already on the site.
- No em dashes in new copy. Match the existing voice and punctuation exactly.
- Use only glyph markers already in use on the site (◉ ✦ ◇ ↻ ▦ ⊞ ✓ ◷ ◆ ✧). No emoji.
- Don't link to pages that don't exist.

## "Why Choose Us" sections
Present as a **2x2 grid of exactly 4 pillars**: `<div class="q-grid">` (omit `.three`, which is the 3-col variant). Card pattern:
```html
<div class="q-card"><div class="marker">&#9673;</div><h3>Pillar name</h3></div>
```
Headings only — no descriptive paragraph under each card. When trimming a longer list, keep 4 items verbatim across distinct axes (scale / method / delivery / ownership) and report which were dropped.

## SEO baseline for every page
- Self-referencing canonical; unique title and meta description.
- `<meta name="robots" content="index, follow, max-image-preview:large, max-snippet:-1, max-video-preview:-1">`.
- JSON-LD `@graph` with Organization + WebPage + Service (+ FAQPage where FAQs exist, + BreadcrumbList).
- Semantic landmarks: `<main>`, `<nav aria-label="Breadcrumb">`, `<header role="banner">`, `<footer role="contentinfo">`.
- Every `<section>` gets a stable `id` and `aria-labelledby` pointing at its own `<h2>` id.
- Add the URL to `sitemap.xml` with a current `lastmod`; bump `lastmod` and JSON-LD `dateModified` whenever the page changes.
- Give each new page in-body contextual inbound links from related pages, not just nav/footer.

## Structure
Avoid repeating identical section structure across pages — vary wrappers and section ordering between pages.
