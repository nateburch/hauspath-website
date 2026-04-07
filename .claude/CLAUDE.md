# CLAUDE.md — HausPath Website

## Project Overview

Public marketing website for HausPath — AI-powered workflow intelligence for sales teams. Static HTML/CSS, no build tools.

## Tech Stack

- **Pure HTML/CSS** — no JavaScript framework, no bundler, no build step
- **Fonts:** Inter (Google Fonts CDN), Gilroy (display font, fallback to Inter/system)
- **No dependencies** — everything is vanilla

## Brand Colors (CSS Variables)

| Variable | Hex | Usage |
|----------|-----|-------|
| `--cyan` | `#00CFFF` | Primary accent, gradient start |
| `--blue` | `#116AF8` | Links, buttons, gradient end |
| `--navy` | `#010921` | Body text, dark backgrounds |
| `--gradient` | `135deg, #00CFFF → #116AF8` | Hero text, CTA backgrounds |
| `--gray-50` through `--gray-800` | Slate scale | UI elements, borders, muted text |

## File Structure

```
hauspath-website/
├── index.html        # Homepage
├── contact.html      # Contact form + info
├── privacy.html      # Privacy Policy
├── terms.html        # Terms of Service
├── sms-terms.html    # SMS Terms
├── styles.css        # All styles (single file)
├── assets/
│   └── logo.png      # HausPath logo
├── README.md
└── .claude/
    └── CLAUDE.md     # This file
```

## Patterns

- **Single stylesheet** — all CSS lives in `styles.css`. Don't split into multiple files.
- **Shared components** — nav and footer HTML is duplicated across pages (no templating). When changing nav/footer, update ALL pages.
- **Mobile responsive** — all layouts must work on phone browsers. Use existing breakpoints in `styles.css`.
- **No JavaScript frameworks** — inline `<script>` at bottom of each page for nav toggle and scroll behavior only.
- **SVG icons inline** — icons are inline SVG, not external files or icon fonts.

## Contact Form

Uses Formspree (`https://formspree.io/f/placeholder`). Needs a real Formspree form ID before going live.

## Contact Info

- Email: hello@hauspath.com
- Phone: (703) 350-4000
- Location: Fairfax, Virginia
- Support email: support@hauspath.com
- Privacy email: privacy@hauspath.com

## When Adding New Pages

1. Copy the nav and footer from `index.html`
2. Include the same `<head>` boilerplate (meta, fonts, styles.css)
3. Include the same `<script>` block at bottom
4. Add the page to the nav links in ALL existing pages
5. Add the page to the footer links in ALL existing pages

## Related

- **Application repo:** `hauspath` (separate repo) — AWS infrastructure, Lambda, React dashboard
- **Brand book:** Dropbox → Hauspath Logos and Branding → Brand Book
