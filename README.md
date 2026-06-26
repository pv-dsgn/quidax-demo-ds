# Quidax Design System

A comprehensive, production-ready design system for the **Quidax cryptocurrency trading platform**. This repository contains the complete design specifications, reusable components, design tokens, and composition patterns that power the Quidax product experience.

## Overview

The Quidax Design System is built on **design tokens**, **atomic elements**, **composed components**, and **composition patterns** — a structured approach to creating consistent, scalable, and maintainable user interfaces for financial applications.

**Live Demo:** [quidax-demo-ds.vercel.app](https://quidax-demo-ds.vercel.app)

## Tech Stack

- **Framework:** React 18.3 with TypeScript
- **Build Tool:** Vite 5
- **Animation:** Motion (v11)
- **Routing:** React Router v7
- **Design Source:** Pencil (`.pen` design file)
- **Styling:** CSS custom properties (tokens) + semantic utility classes

## Repository Structure

```
quidax-demo-ds/
├── DESIGN-SYSTEM.md          ← Full specifications & governance rules
├── dsm-design.pen            ← Source of truth (open in Pencil editor)
├── src/
│   ├── styles/
│   │   ├── tokens.css        ← Design tokens (colors, spacing, typography)
│   │   ├── typography.css    ← Semantic text utility classes
│   │   ├── global.css        ← Resets and base styles
│   │   └── fonts.css         ← Uncut Sans Variable font-face
│   ├── components/
│   │   └── ui/               ← Reusable component implementations
│   └── App.tsx               ← Main entry point
├── public/                   ← Assets and fonts
├── index.html                ← HTML template
└── package.json              ← Dependencies & scripts
```

## Key Sections

### Design Tokens
All colors, spacing, typography, and sizing follow a strict token system:
- **Colors:** Brand purple, semantic status colors (success, error, warning, info), neutral palette
- **Spacing:** 4px base grid (`--space-*` tokens)
- **Typography:** Uncut Sans Variable typeface with 11 semantic styles (Display XL → Caption)
- **Radius:** 4 prescriptive values (sm, md, lg, full)

See [Design Tokens Reference](DESIGN-SYSTEM.md#variables-design-tokens) for full list.

### Elements (Atomic Primitives)
Low-level, reusable UI building blocks:
- **Buttons** (Primary, Secondary, Ghost)
- **Input** (text field with label)
- **Badges** (4 semantic variants)
- **Avatar**, **Toggle**, **Chip**, **Tab**, **Divider**

### Components (Composed Patterns)
Higher-order UI patterns built from elements:
- **Card** — Container with header, content, and action slots
- **Alert** — Status notification (Info, Success, Warning, Error)
- **CoinRow** — Cryptocurrency display with price and change
- **StatCard** — Metric display with trend indicator
- **TransactionRow** — Financial transaction row
- **NavBar** — Top navigation with logo, links, and CTA
- **MarketTableRow** — Full-width market data table row

### Compositions
Complete UI sections and screens assembled from components:
- **Market Table** — Full market data display with search and filter
- **Design System Showcase** — Interactive documentation frame

## Getting Started

### Installation

```bash
npm install
```

### Development

```bash
npm run dev
```

Starts the Vite dev server at `http://localhost:5173`.

### Build for Production

```bash
npm run build
```

Compiles TypeScript and builds optimized assets to `dist/`.

### Preview

```bash
npm run preview
```

Serves the production build locally.

## Design System Governance

### For Design Consumers
- **Always use design tokens** — never hardcode hex values or custom spacing
- **Use the component library first** — check if an existing component fits before building new
- **Override responsibly** — only customize descendants that differ from defaults

### For Design Contributors
- **Add variables before components** — new tokens must be defined in the token system first
- **Build reusable components** — use Pencil `ref` mechanism, not copies
- **Document your work** — add specifications to this document before merging
- **Follow naming conventions:**
  - Colors: `--color-{category}-{variant}` (e.g., `--color-success-bg`)
  - Spacing: `--space-{4px-grid-step}` (e.g., `--space-4`, `--space-8`)
  - Typography: `.text-{style}` (e.g., `.text-h1`, `.text-body-sm`)

## Deprecation & Updates

See [Update Rules](DESIGN-SYSTEM.md#update-rules) and [Deprecation Rules](DESIGN-SYSTEM.md#deprecation-rules) for how to modify and retire design system items.

## Component Inventory

| Category | Count |
|----------|-------|
| Elements | 15 |
| Components | 11 |
| Compositions | 2 |
| **Total** | **28** |

## Design Files

| File | Purpose |
|------|---------|
| `dsm-design.pen` | Source of truth — open in Pencil for visual editor |
| `DESIGN-SYSTEM.md` | Complete specifications and governance |
| `src/styles/tokens.css` | CSS custom properties (code equivalent of tokens) |
| `src/components/ui/` | React component implementations |

## Resources

- **Full Specification:** See [DESIGN-SYSTEM.md](DESIGN-SYSTEM.md)
- **Visual Reference:** Open `dsm-design.pen` in Pencil editor
- **Live Demo:** [quidax-demo-ds.vercel.app](https://quidax-demo-ds.vercel.app)
- **Font:** Uncut Sans Variable (included in `public/fonts/`)

## License

MIT — See [LICENSE](LICENSE) for details.

---

**Maintained by:** [@pv-dsgn](https://github.com/pv-dsgn)
