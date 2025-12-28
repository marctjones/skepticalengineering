# Skeptical Engineering Website

Portfolio site for skepticalengineering.com showcasing selected open source projects.

## Deployment

**GitHub:** https://github.com/marctjones/skepticalengineering

**Live sites:**
- https://skepticalengineering.pages.dev
- https://skepticalengineering.com

**To deploy changes:**
```bash
git add . && git commit -m "description" && git push
npx wrangler pages deploy . --project-name=skepticalengineering
```

Note: Auto-deploy from GitHub is not configured. Deploys are manual via wrangler.

## Site Structure

Single-page static site with 4 featured projects:

| Project | Status |
|---------|--------|
| PromptResponse | Active Development |
| Klareco | Experimental |
| Harbor + related (Rigging, Compass, Corsair) | Experimental |
| EDDI | Experimental |

## Brand Identity

### Philosophy

Skeptical Engineering takes its name and spirit from thoughtful questioning — not rejecting technology, but interrogating it. The brand draws inspiration from the Luddites, who weren't anti-technology but skilled craftsmen protesting technology deployed to exploit workers and undermine craft. We build software the same way: deliberately, skeptically, in service of people rather than hype.

**Core tension:** Boring but clever. The work is rigorous and unglamorous; the thinking behind it is sharp and creative. We solve hard problems so thoroughly that the solutions disappear into reliability.

### Logo: The Great Enoch

The primary logo is the Great Enoch hammer — the tool Luddites used to smash exploitative industrial looms in 19th century England — with a terminal prompt `>_` embedded in the hammer head.

**What it says:**
- We use technology, but we choose it deliberately
- Human judgment and craft over blind automation
- "The power of the craftsman" — skilled hands guided by skeptical minds
- Technology should serve people, not the reverse

**Secondary symbols:**
- **Loom/weave** — Constraints enabling creativity, the rigid warp allowing the pattern to emerge. "Stability through constraints."
- **Bridge** — Infrastructure that disappears when it works. Boring but essential.

### Visual Design

**Typography:**
- **IBM Plex Mono** — Sidebar navigation, project names, status badges, category headers. The terminal aesthetic: precise, monospaced, utilitarian.
- **IBM Plex Serif** — Body text. Bookish, readable, serious. Inspired by Typography for Lawyers — content that rewards careful reading.

**Color palette:**
- **Near-black (#1c1c1c)** — Sidebar background. Terminal darkness.
- **Warm cream (#f8f8f6)** — Content background. Paper, not screen.
- **Muted olive-greens (#80a080, #505048)** — Accent on hover. Subtle life in the terminal.
- **Status green (#4a7c4a border, #3a5c3a text)** — Active development.
- **Status yellow (#9a8a50 border, #6a6030 text)** — Experimental.

**Layout:**
- Left sidebar with navigation (Typography for Lawyers pattern)
- Constrained content width (720px) for readability
- Generous whitespace and line height (1.7)
- Projects grouped by category: Productivity, Security & Privacy, Research

**Aesthetic principles:**
- **No gradients, shadows, or decorative flourishes** — Substance over style
- **Monochrome with minimal accent** — Restrained, professional
- **Timeless over trendy** — Should look appropriate in 10 years
- **Terminal meets library** — The rigor of the command line, the depth of the bookshelf

### Tone of Voice

- **Direct and precise** — Say what you mean, no filler
- **Confident but not boastful** — Let the work speak
- **Dry wit** — "The interesting part is making it boring"
- **Substance over marketing** — Features and philosophy, not buzzwords
- **Acknowledges complexity** — Doesn't pretend hard problems are easy

### Distinction from joneslaw.io

These sites should feel unrelated at a glance:

| Aspect | joneslaw.io | skepticalengineering.com |
|--------|-------------|--------------------------|
| Layout | Centered, single column | Left sidebar + content |
| Typography | Sans-serif (system fonts) | Serif body + mono headers |
| Background | Cool gray (#fafafa) | Warm cream (#f8f8f6) |
| Sidebar | None | Dark terminal panel |
| Tone | Personal, professional | Technical, philosophical |

## Site Structure

- Dark terminal sidebar with monospace navigation (IBM Plex Mono)
- Serif body text for readability (IBM Plex Serif)
- Muted olive-gray palette, no flashy colors
- Each project: one paragraph + bulleted feature list
- Status badges with borders (green for active, yellow for experimental)

## Philosophy / Taglines

Primary tagline: **"The interesting part is making it boring."**

Other approved lines (rotate, use in content, etc.):
- "Constraints breed creativity."
- "Boring solutions to interesting problems."
- "Stable is the hard part."
- "Solve problems without making them."
- "Boring is a feature."

Counter to "move fast and break things" — innovation comes from working within constraints, shipping stable solutions, and doing the hard work so users don't have to.

## Related Sites

- joneslaw.io - Personal landing page (separate repo: marctjones/joneslaw-io)
