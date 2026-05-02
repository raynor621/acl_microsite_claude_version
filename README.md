# ACL Tear Microsite — M. Brett Raynor, M.D.

A standalone single-page educational site about ACL injuries, designed to live at its own URL and point patients back to [brettraynormd.com](https://www.brettraynormd.com).

**Repo:** [github.com/raynor621/acl_microsite_claude_version](https://github.com/raynor621/acl_microsite_claude_version)
**Live URL:** _TBD — deploy via Vercel below_

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

### Option 1 — connect this repo to Vercel (recommended)
1. Go to [vercel.com/new](https://vercel.com/new) and click **Import Git Repository**.
2. Authorize Vercel to access GitHub (one-time) and pick `acl_microsite_claude_version`.
3. Accept the defaults — Vercel detects the static site automatically.
4. Click **Deploy**. Live URL in ~30 seconds.

Once connected, every commit to `main` auto-deploys. No manual redeploy step.

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

**For small text edits** (typo, phone number, single sentence): edit `index.html` directly via GitHub's web editor — open the repo, click the file, click the pencil icon. Commit. Vercel auto-deploys.

**For substantial changes** (new sections, swap images, design tweaks): edit the file locally and replace it on GitHub. The base64 image embeds make full-file replacement the cleanest path.

## Embedded assets

Logo, headshot, and anatomy illustration are embedded as base64 inside `index.html`. To swap any of them, replace the corresponding `data:image/...;base64,...` string. Source files live in the parent Obsidian vault under:

- `Templates/Logos/brett-raynor-md-logo.png` — header logo
- `Templates/Logos/toa-ols-logo.png` — footer logo
- `Templates/brett-raynor-headshot.jpg` — About section headshot
- `Templates/Medical Illustrations/acl-tear-illustration.png` — anatomy illustration

The Jotform appointment form is form ID **261207287495161** ("ACL Appointment Request"). To swap it, update the iframe `src` and `id` attributes plus the embed handler script call.

## Practice info

- **M. Brett Raynor, M.D.** — Texas Orthopaedic Associates, a division of OrthoLoneStar
- 7115 Greenville Ave, Suite 310, Dallas, TX 75231
- (214) 265-3211 · [brettraynormd.com](https://www.brettraynormd.com)
