# Leadership Delta — program microsite (static)

Single self-contained file: `index.html`. No build step, no backend. The enquiry buttons are `mailto:` links, so it works the moment it's hosted. Fonts load from Google Fonts (online).

## Fastest way to get a shareable link

**Option A — Netlify Drop (no account, ~30 seconds)**
1. Go to https://app.netlify.com/drop
2. Drag the **`leadership-delta-site`** folder (the one containing `index.html`) onto the page.
3. You get a live URL instantly (e.g. `random-name.netlify.app`). Rename the site in Site settings if you like.

**Option B — Vercel CLI (~1 minute)**
```bash
cd "leadership-delta-site"
npx vercel          # first run asks you to log in via browser; then deploys
npx vercel --prod   # promote to a production URL
```

**Option C — GitHub → Vercel (best for ongoing edits)**
1. Create a new repo on github.com (e.g. `leadership-delta-site`), public or private.
2. Push this folder:
   ```bash
   cd "leadership-delta-site"
   git init && git add . && git commit -m "Leadership Delta microsite v0.1"
   git branch -M main
   git remote add origin https://github.com/<you>/leadership-delta-site.git
   git push -u origin main
   ```
3. On vercel.com → **Add New → Project → Import** the repo → Deploy. Auto-redeploys on every push.

## Custom domain
In Netlify or Vercel, add a domain/subdomain (e.g. `leadershipdelta.paulgibbonsadvisory.com`) under the project's Domains settings, then point a CNAME at it from your DNS.

## Notes / to-do before going fully public
- **BETA flag** (bottom-left) is still on — remove the `<div class="betaflag">…</div>` when ready.
- **Stats** are sourced (BCG, Gartner, Nufar Gaspar, Saks). The training-transfer figure is framed as a range; keep that framing.
- **Branding:** decide Paul-branded vs co-branded for Miguel's client before sharing widely.
- **Enquiry form:** currently `mailto:`. For a real captured form, wire Formspree / Vercel Forms (needs Option C or a small build) — a later step.
