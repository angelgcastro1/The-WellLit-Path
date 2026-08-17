# The Well-Lit Path

Coaching &amp; consulting site for Tobias Neal. Single self-contained page —
no build step, no dependencies. Deploy by serving `index.html` at the root.

## Structure

- `index.html` — the entire site: six pages (Home, About, Coaching,
  Consulting, Resources, Contact) behind a hash router. GSAP, all photography,
  and the favicon are embedded inline, so the file works offline apart from
  Google Fonts.
- `favicon/` — standalone icon files for deployment at the site root.

## Deploying

Vercel, Netlify, Cloudflare Pages, or GitHub Pages will all serve this as-is.
No framework detection or build command is required.

## Before launch

1. **Calendly** — search `YOUR-HANDLE` in `index.html`. It appears twice, as the
   `href` on the two booking buttons. Replace both with the real scheduling URL.
2. **Testimonials** — the home page has three. The first is real; the second and
   third are placeholder copy and need replacing with genuine quotes.
3. **FAQ answers** — drafted from the offer details and need Tobias's sign-off,
   especially the reschedule and reduced-cost policies.
4. **Forms** — the contact form and the resources email capture are front-end
   only. Wire them to a form handler.
5. **Workshops &amp; Facilitation** — listed as a third service on the home page.
   Confirm this is a real offer.

## Favicon

The small sizes (16/32/48) use a simplified glyph, since the full emblem's
detail is illegible below about 64px. Larger sizes use the real emblem. To wire
up the standalone files, add to `<head>`:

```html
<link rel="icon" href="/favicon/favicon.ico" sizes="any">
<link rel="icon" type="image/png" sizes="32x32" href="/favicon/favicon-32.png">
<link rel="apple-touch-icon" sizes="180x180" href="/favicon/apple-touch-icon.png">
<meta name="theme-color" content="#1C2E24">
```
