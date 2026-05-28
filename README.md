# Innowiz templates — deployment

Static HTML site. No build step.

## Deploy to Vercel — easiest (web UI)

1. Go to https://vercel.com/new
2. Click **"Import" → "Upload"** (or drag this whole folder onto the page)
3. Project name: e.g. `innowiz-templates`
4. **Framework Preset**: "Other" (auto-detected)
5. Hit **Deploy**

That's it — you'll get a URL like `innowiz-templates.vercel.app`.

## Deploy via CLI

```bash
npm i -g vercel
cd deploy
vercel       # follow prompts for first deploy
vercel --prod
```

## File layout

```
deploy/
├── index.html              ← entry page (was "Innowiz worksheets.html")
├── colors_and_type.css     ← Innowiz design tokens
├── vercel.json             ← cache headers + clean URLs
├── fonts/                  ← Harabara + Roboto family
└── assets/                 ← logo + phase icons
```

## Custom domain

In the Vercel dashboard → **Project → Settings → Domains** → add e.g. `templates.innowiz.be`. Vercel shows you the DNS records to set at your registrar.

## Notes

- The worksheet images live on Google Drive — make sure those files stay shared as "Anyone with the link" or the site will show fallbacks.
- No server, no database, no API keys. Pure static.
