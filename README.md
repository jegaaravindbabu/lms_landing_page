# Online Academy — Landing Page

Marketing landing page and funnel for a white-label LMS ("Start Your Own Online Academy"),
aimed at coaching institutes & tuition centres. Static HTML — no build step.

## Pages
| File | Purpose |
|------|---------|
| `index.html` | Main landing page (hero → 2-min demo → features → pricing → lead form) |
| `thank-you.html` | Post-submit page (Book demo + WhatsApp, Google Ads conversion) |
| `privacy.html` | Privacy policy (required for Google Ads) |

## Configure before going live
Edit the settings block near the top of `index.html` (and keep `thank-you.html` in sync):

```js
const WHATSAPP_NUMBER = "919XXXXXXXXX";   // country code, no + or spaces
const BRAND           = "Online Academy"; // your business name / wordmark
const DEMO_URL        = "https://...";     // your live product demo
const DEMO_VIDEO_ID   = "";                // 2-min demo YouTube video ID
const WEB3FORMS_KEY   = "";                // optional: emails you every lead (web3forms.com)
```

Also paste your Google Ads / GA4 tag in the commented `<head>` block on `index.html` and
`thank-you.html`, and enable the conversion snippet on `thank-you.html`.

## Deploy (Vercel)
1. Import this repo in Vercel — **Framework preset: Other**, no build command, output = repo root.
2. Add your custom domain in **Settings → Domains**.
3. The landing page will be your ad's Final URL (e.g. `yourdomain.com`).

## Local preview
Open `index.html` in a browser, or run `python -m http.server 5500` in this folder and
visit `http://localhost:5500`.
