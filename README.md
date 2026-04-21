# Brain Function Project
### Cognitive Enrichment for Adults 30+
*Neuroscience · UX Design · HTML/CSS/JS Implementation*

---

## What this is

A scientifically grounded, fully responsive web application presenting 25 curated cognitive enrichment tasks for adults 30+. Built as a standalone HTML/CSS/JS project with no backend, no framework, and no dependencies beyond Google Fonts.

---

## Files

```
standalone_html_project/
├── index.html    — Full page: hero, domains, filter bar, task grid, FAQ, footer
├── styles.css    — Design system: CSS vars, grid, components, animations, responsive
├── script.js     — IntersectionObserver, filtering, search, rendering, parallax, counters
├── tasks.json    — 25 task entries (full schema)
└── README.md     — This file
```

---

## How to run

Open `index.html` in any modern browser. For local development (to avoid CORS issues with `tasks.json`):

```bash
# Python 3
python -m http.server 8080

# Node.js (npx)
npx serve .
```

Then visit `http://localhost:8080`.

---

## Task Schema

Each entry in `tasks.json` follows this structure:

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique slug identifier |
| `title` | string | Display title |
| `hook` | string | One-sentence engaging opener |
| `cognitive_functions` | string[] | One or more of the 6 domains |
| `difficulty` | 1–4 | 1=Beginner, 2=Intermediate, 3=Advanced, 4=Expert |
| `time_minutes` | number | Estimated session duration |
| `time_label` | string | Human-readable time (e.g. "20 min") |
| `difficulty_label` | string | Human-readable level |
| `steps` | string[] | 3–6 actionable steps |
| `benefits` | string[] | 2–3 evidence-grounded benefit statements |
| `evidence_source` | string | Citation for primary research support |
| `prerequisites` | string | Required background knowledge or "None" |
| `related_tasks` | string[] | IDs of complementary tasks |

---

## Design System

### Colors
| Variable | Value | Role |
|----------|-------|------|
| `--clr-primary` | `#1A56DB` | Primary blue — CTAs, accents |
| `--clr-accent` | `#0E9F6E` | Teal-green — success, Beginner |
| `--clr-amber` | `#C27803` | Warning — Advanced level |
| `--clr-bg` | `#F8FAFC` | Page background |
| `--clr-card` | `#FFFFFF` | Card surfaces |

### Typography
- **Display/Headings**: Syne (700–800 weight) — editorial, distinctive
- **Body**: DM Sans (300–600 weight) — clean, readable
- **Code/Citations**: DM Mono — technical precision

### Spacing
8px base unit: `8 / 16 / 24 / 32 / 48 / 64 / 96 / 128px`

---

## Cognitive Domains

| Domain | Icon | Color | Coverage |
|--------|------|-------|----------|
| Working Memory | 🧠 | `#3B82F6` | Dual n-back, memory palace, instrument practice, mental arithmetic, map drawing |
| Processing Speed | ⚡ | `#8B5CF6` | Rhythm & drumming, badminton, language sprints, peripheral vision, speed reading |
| Executive Function | ♟️ | `#F59E0B` | Chess, Go, structured debate, recipe improvisation, backward planning |
| Visuospatial Reasoning | 🌐 | `#10B981` | Origami, route variation, observational sketching, memory palace, map drawing |
| Sustained Attention | 🎯 | `#EF4444` | Mindful single-tasking, breath-count meditation, speed reading, peripheral vision |
| Semantic Memory | 💬 | `#EC4899` | Spaced repetition journaling, language sprint, trivia deep dive, collaborative storytelling |

---

## Task Validation Gates

All 25 tasks passed these 5 gates before inclusion:

| Gate | Criterion |
|------|-----------|
| 1 | Evidence Base: at least 1 peer-reviewed study or meta-analysis |
| 2 | Real-World Applicability: no specialist equipment or paid subscriptions required |
| 3 | Accessibility: doable by average adult with no prior expertise at Beginner level |
| 4 | Transfer Transparency: no overclaiming of cognitive transfer |
| 5 | Ethical Framing: no disease-prevention or medical claims |

---

## Difficulty Levels

| Level | Label | Time | Criteria |
|-------|-------|------|----------|
| L1 | Beginner | 5–15 min/day | No prior skill; single cognitive demand |
| L2 | Intermediate | 15–30 min/day | Some familiarity helpful; 2+ cognitive demands |
| L3 | Advanced | 30–60 min/day | Sustained practice; multi-domain integration |
| L4 | Expert | 60+ min/day | High mastery threshold; self-assessment required |

---

## Key Research Citations

- Jaeggi, S.M. et al. (2008). "Improving fluid intelligence with training on working memory." *PNAS.*
- Maguire, E.A. et al. (2000). "Navigation-related structural change in the hippocampi of taxi drivers." *PNAS.*
- Cepeda, N.J. et al. (2006). "Distributed practice in verbal recall tasks: A review and quantitative synthesis." *Psychological Bulletin.*
- Dresler, M. et al. (2017). "Mnemonic training reshapes brain networks to support superior memory." *Neuron.*
- Hölzel, B.K. et al. (2011). "Mindfulness practice leads to increases in regional brain gray matter density." *Psychiatry Research.*
- Bialystok, E. et al. (2012). "Bilingualism: consequences for mind and brain." *Trends in Cognitive Sciences.*
- Hanna-Pladdy, B. & MacKay, A. (2011). "The relation between instrumental musical activity and cognitive aging." *Neuropsychology.*
- Hillman, C.H. et al. (2008). "Be smart, exercise your heart: exercise effects on brain and cognition." *Nature Reviews Neuroscience.*
- Karpicke, J.D. & Blunt, J.R. (2011). "Retrieval practice produces more learning than elaborative studying with concept mapping." *Science.*
- Kim, S. et al. (2014). "Increased cortical thickness in the frontal lobe in professional Go players." *PLOS ONE.*

---

## Ethical Positioning

This project is positioned as **cognitive enrichment only**. We do not:
- Claim to prevent, treat, or cure any neurological condition
- Claim to prevent dementia or Alzheimer's disease
- Overstate transfer effects beyond what the evidence supports
- Cherry-pick weak evidence for compelling-sounding benefits

We do:
- Cite primary sources for every task
- Acknowledge evidence quality variation
- Frame benefits honestly (skill development, not disease prevention)
- Present transfer potential conservatively

---

## Accessibility

- WCAG 2.1 AA target
- Full keyboard navigation with visible focus states
- Skip-to-main-content link
- ARIA roles and labels throughout
- `aria-live` regions for dynamic content (filter results)
- `aria-expanded` on all collapsible elements
- `prefers-reduced-motion` respected — all animations disabled
- Semantic HTML landmarks: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`
- Single `<h1>` with logical heading cascade

---

## Browser Support

Chrome 90+ · Firefox 88+ · Safari 14+ · Edge 90+

---

*Built following the Brain Function Project Intensive Plan. 5 phases, 6 weeks of design and implementation compressed into a focused execution session.*
