# rr-go — go.redefiningretirement.io

Resource hub for RedefiningRetirement.io — guides, comparisons, and tools for Gen X creators and solopreneurs building audiences they own.

**Live URL:** https://go.redefiningretirement.io
**Main site:** https://redefiningretirement.io

## Stack

- Astro (static site)
- Vanilla CSS (no Tailwind)
- Deployed on Vercel

## Local development

```bash
npm install
npm run dev
```

Dev server runs at `http://localhost:4321`

## Pages

| Route | Description |
|---|---|
| `/` | Homepage |
| `/topics/newsletters/` | Newsletter topic hub |
| `/topics/creator-tools/` | Creator tools topic hub |
| `/topics/ai-resources/` | AI resources topic hub |
| `/compare/beehiiv-vs-substack/` | Platform comparison |
| `/guides/move-your-audience-to-a-newsletter/` | How-to guide |
| `/resources/` | All resources index |

## Deploying to Vercel

### First-time setup

1. Push this repo to GitHub as `coreykmedia/rr-go` (or similar)
2. Go to [vercel.com](https://vercel.com) → Add New Project → Import the repo
3. Framework preset: **Astro** (Vercel auto-detects)
4. Click Deploy

### Add the custom domain

1. In Vercel project → Settings → Domains
2. Add `go.redefiningretirement.io`
3. Vercel will give you a CNAME record to add in your DNS
4. In your DNS provider (wherever redefiningretirement.io DNS is managed):
   - Add a CNAME record: `go` → `cname.vercel-dns.com`
5. Wait for DNS to propagate (usually under 30 minutes)

### Ongoing deploys

Push to `main` branch → Vercel auto-deploys.

```bash
git add -A && git commit -m "Update [description]" && git push origin main
```

## Expanding the site

Expand one cluster at a time:
1. **Newsletters first** — add more comparisons (`/compare/`), more guides (`/guides/`)
2. **Creator Tools** — individual tool reviews, tool stack posts
3. **AI Resources** — specific workflows, prompt guides, tool comparisons

Add pages as static `.astro` files in the appropriate folder. Internal linking back to the main site (`redefiningretirement.io`) on every page.
