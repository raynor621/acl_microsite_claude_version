# ACL Tear Microsite — M. Brett Raynor, M.D.

A standalone single-page educational site about ACL injuries, intended to be hosted at its own URL (subdomain or standalone domain) and to point patients back to [brettraynormd.com](https://www.brettraynormd.com).

## What's here

- **`index.html`** — the entire microsite. Self-contained: HTML, CSS, embedded base64 logos and images, and an inline Jotform iframe. The only external dependency is Google Fonts (Inter + Playfair Display) loaded over CDN.
- **`vercel.json`** — minimal static-site config (clean URLs, basic security headers).
- **`.gitignore`** — macOS / editor noise.

## Local preview

```bash
# From inside this folder:
python3 -m http.server 8080
# Then open http://localhost:8080 in a browser.
```

Or simply double-click `index.html` to open it in your default browser.

## Deploying to Vercel

### Option 1 — connect this GitHub repo to Vercel
1. Push this folder to a GitHub repo.
2. Go to [vercel.com/new](https://vercel.com/new), import the repo.
3. Accept the defaults — Vercel detects the static site automatically.
4. Click **Deploy**. Live URL in ~30 seconds.

### Option 2 — deploy from your local machine
```bash
npm i -g vercel
cd acl-microsite
vercel
# Follow prompts; accept defaults.
```

### Custom domain
Once deployed, attach a custom domain (e.g. `acl.brettraynormd.com` or a standalone like `raynoracl.com`) in the Vercel project's **Domains** tab.

## Editing content

The microsite is a single HTML file. Open `index.html` in any text editor to update copy. Sections are clearly marked with HTML comments (`<!-- HERO -->`, `<!-- SYMPTOMS & DIAGNOSIS -->`, etc.).

Logo, headshot, and anatomy illustration are embedded as base64. To swap any of them, replace the corresponding `data:image/...;base64,...` string. Source files live in the parent vault under `Templates/Logos/`, `Templates/`, and `Templates/Medical Illustrations/`.

The Jotform appointment form is form ID **261207287495161** ("ACL Appointment Request"). To swap it, update the iframe `src` and `id` attributes plus the embed handler script call.

## Practice info

- **M. Brett Raynor, M.D.** — Texas Orthopaedic Associates, a division of OrthoLoneStar
- 7115 Greenville Ave, Suite 310, Dallas, TX 75231
- (214) 265-3211 · [brettraynormd.com](https://www.brettraynormd.com)
