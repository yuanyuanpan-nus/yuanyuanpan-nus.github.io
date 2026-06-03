# Design — Yuanyuan Pan Academic Page

## Design Context

### Users
- Finance faculty, hiring committees, and seminar hosts evaluating a job-market Ph.D. candidate
- Co-authors and graduate students seeking contact and paper lists
- Context: quick scan of credentials, job market paper, and publication pipeline

### Brand Personality
- Rigorous, calm, credible — three words: **scholarly**, **precise**, **approachable**
- Evoke confidence and intellectual clarity without corporate flash

### Aesthetic Direction
- **Visual direction (chosen):** Cool & minimal — editorial finance-academic, not startup or trading-terminal
- **Aesthetic style (chosen):** Museum Whitespace — artifact-like typography, extreme breathing room, narrow reading column
- **Anti-references:** Neon fintech dashboards, brutalist chaos, generic AI purple gradients, cramped CV PDF layout
- **Reference:** Skipped — derived from portrait (formal, neutral, professional) and CV discipline (finance academia)
- **Theme:** Dual light/dark with toggle; default follows `prefers-color-scheme`

### Design Principles
1. Content hierarchy mirrors CV sections — no hero marketing copy beyond page-story text
2. Typography carries authority: serif display for name, sans for body and metadata
3. Whitespace and line-length optimize long publication reading
4. Links and status labels (R&R, Accepted, JMP) are scannable structural elements, not decoration
5. Portrait is documentary, not stylized — no heavy filters on the photo

## Design System

### Palette
| Role | Light | Dark |
|------|-------|------|
| Background | `#f7f5f1` | `#0f1218` |
| Surface | `#ffffff` | `#171c26` |
| Text primary | `#1c2433` | `#e8eaef` |
| Text muted | `#5c6578` | `#9aa3b5` |
| Accent | `#1e4d6b` | `#7eb8d4` |
| Border | `#e2ddd4` | `#2a3344` |
| Highlight (JMP) | `#6b4e1e` / bg `#f5edd8` | `#e8c98a` / bg `#2a2418` |

### Typography
- **Display:** "Fraunces", Georgia, serif — name and section headings
- **Body:** "Source Sans 3", system-ui, sans-serif — 16px base, line-height 1.65
- **Scale:** Name 2.25rem; h2 1.35rem; body 1rem; meta 0.875rem

### Style
- Product: academic personal / research portfolio
- Pattern: sticky sidebar + scrollable main (desktop); stacked single column (mobile)
- Effects: subtle 1px borders, no glass blur, no heavy shadows; 150ms color transitions

### Anti-patterns
- Emoji icons; horizontal scroll; placeholder-only forms; gray-on-gray body text
- Promoting job-market line into separate hero band outside About section

### Aesthetic Implementation

**Layout structure:** `display: flex` — fixed-width sidebar (~260px) with portrait, name, affiliation, icon links, in-page nav; `main` flex-grow with `max-width: 42rem` prose column.

**Surface treatment:** Sections separated by `border-top: 1px solid var(--border)` and generous `padding-top: 2.5rem`. Publication blocks use no card chrome — list rhythm only. Optional light `background: var(--surface)` on sidebar only.

**Typography expression:** Headings `font-family: var(--font-display)`, weight 600, letter-spacing -0.02em. Body weight 400. Strong emphasis (job market) uses `font-weight: 600` within About, not a badge in header.

**Decorative rules:** No gradients, no illustration, no stock photos. Single accent color for links and focus rings. Timeline dots for News only.

**Spatial rhythm:** Section gaps 2.5–3rem; paragraph margin 1rem; publication entries 1.25rem apart — airy.

**Signature CSS:**
```css
font-family: var(--font-display);
max-width: 42rem;
border-top: 1px solid var(--border);
color: var(--accent);
letter-spacing: -0.02em;
```
