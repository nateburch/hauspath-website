# HausPath Website

Public marketing website for [HausPath](https://hauspath.com) — AI-powered workflow intelligence for sales teams.

## Pages

| File | Purpose |
|------|---------|
| `index.html` | Homepage — hero, features, how it works, CTA |
| `contact.html` | Contact form + info (phone, email, location) |
| `privacy.html` | Privacy Policy |
| `terms.html` | Terms of Service |
| `sms-terms.html` | SMS / Text Messaging Terms |
| `styles.css` | All styles (single file) |
| `assets/` | Logo and images |

## Setup

No build step. Open `index.html` in a browser or deploy to any static host.

## Contact Form

The contact form on `contact.html` uses [Formspree](https://formspree.io). The form action URL needs a real Formspree endpoint:

```html
<!-- Replace placeholder with your Formspree form ID -->
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

To set up:
1. Create a free account at [formspree.io](https://formspree.io)
2. Create a new form
3. Replace `placeholder` in the form action with your form ID

## Deployment

Static files — deploy anywhere:
- **GitHub Pages:** Push to `main`, enable Pages in repo settings
- **Netlify/Vercel:** Connect repo, deploy automatically
- **S3 + CloudFront:** Upload files to bucket with static hosting enabled

## Related

- Application repo: `hauspath` (private) — AWS infrastructure, Lambda, React dashboard
