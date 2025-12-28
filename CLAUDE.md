# Skeptical Engineering Website

Portfolio site for skepticalengineering.com showcasing selected open source projects.

## Current Status

**Site content is complete.** The `index.html` file contains all project descriptions.

### Remaining Tasks

1. **Initialize git repo and commit:**
   ```bash
   git init
   git add .
   git commit -m "Initial skepticalengineering.com portfolio site"
   ```

2. **Create GitHub repo and push:**
   ```bash
   gh repo create skepticalengineering --public --source=. --push
   ```

3. **Deploy to Cloudflare Pages:**
   ```bash
   wrangler pages deploy . --project-name=skepticalengineering
   ```

4. **Connect custom domain** in Cloudflare Pages dashboard:
   - Go to Pages > skepticalengineering > Custom domains
   - Add `skepticalengineering.com`

## Site Structure

Single-page static site with 4 featured projects:

| Project | Description Length | Status |
|---------|-------------------|--------|
| PromptResponse | 2 paragraphs | Active Development |
| Klareco | 3 paragraphs | Experimental |
| Harbor | 2 paragraphs + related projects (Rigging, Compass, Corsair) | Experimental |
| EDDI | 1 paragraph | Experimental |

## Design

- Minimal, light aesthetic matching joneslaw.io style
- No personal info or links to joneslaw.io
- Each project links to its GitHub repo
- Status badges: "Active Development" (green) or "Experimental" (yellow)

## Related Sites

- joneslaw.io - Personal landing page (deployed, auto-deploys from marctjones/joneslaw-io)
