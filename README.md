# Design Interviewer — landing

Static site, no build step. Upload the whole folder to any static host
(Netlify Drop, Vercel, GitHub Pages, Cloudflare Pages, Tilda/Webflow embed, etc.).

- index.html — the page (all CSS/JS inline; fonts from Google Fonts)
- demo.mp4 — hero demo video (720p, ~7 MB)
- demo-poster.jpg — video poster and social preview image
- sample-report.pdf — sample report behind the "Sample report (PDF)" button

## Pilot sign-up form (set this before going live)

The "Join the pilot" form sends the visitor's email to your form collector.
Open index.html, find `var FORM_ENDPOINT = '';` and paste your endpoint, e.g.
`https://formspree.io/f/xxxxxxx`. The form POSTs FormData with the fields
`email` and `source=landing-pilot`, which works with Formspree, Getform, Basin
or a Google Apps Script web app.

Until FORM_ENDPOINT is set, the form only shows the thank-you message and sends nothing.
