# CoPaw UI/UX Pro Max

🎨 Professional UI/UX design intelligence for CoPaw agents.

## Overview

This is a CoPaw-adapted version of [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) (⭐ 56.7k).

A comprehensive design intelligence skill that provides:
- **Design system generation** for any product type
- **Multi-platform support** (Web / iOS / Android / React Native / Flutter)
- **Component design** guidance
- **UX/UI best practices** and checklists
- **Design knowledge base** with 15+ stacks

## Features

| Feature | Description |
|---------|-------------|
| Design System Generator | Generate complete design systems with colors, typography, layout, animation |
| Multi-Platform | Web, iOS, Android, React Native, Flutter, SwiftUI, Jetpack Compose |
| 10 Priority Rules | CRITICAL → HIGH → MEDIUM → LOW |
| 100+ Quick References | Instant access to design patterns and anti-patterns |
| 15+ Stack Guides | React, Vue, Next.js, Flutter, SwiftUI, etc. |

## Quick Start

### Prerequisites

```bash
python --version
```

**Windows (if needed):**
```powershell
winget install Python.Python.3.12
```

### Generate Design System

```bash
# Generate a complete design system
python skills/ui-ux-pro-max/scripts/search.py "fintech crypto modern" --design-system

# Search for specific styles
python skills/ui-ux-pro-max/scripts/search.py "glassmorphism dark" --domain style

# Get UX best practices
python skills/ui-ux-pro-max/scripts/search.py "animation accessibility" --domain ux

# Search colors
python skills/ui-ux-pro-max/scripts/search.py "saas fintech" --domain color

# Typography
python skills/ui-ux-pro-max/scripts/search.py "modern professional" --domain typography
```

### Output Formats

```bash
# ASCII box (default) - Terminal display
python skills/ui-ux-pro-max/scripts/search.py "fintech crypto" --design-system

# Markdown - For documentation
python skills/ui-ux-pro-max/scripts/search.py "fintech crypto" --design-system -f markdown
```

## Available Domains

| Domain | Use For | Example Keywords |
|--------|---------|----------------|
| `product` | Product type recommendations | SaaS, e-commerce, healthcare, beauty |
| `style` | UI styles, colors, effects | glassmorphism, minimalism, dark mode |
| `typography` | Font pairings, Google Fonts | elegant, playful, professional |
| `color` | Color palettes by product | saas, ecommerce, fintech |
| `landing` | Page structure, CTA | hero, testimonial, pricing |
| `chart` | Chart types, libraries | trend, comparison, funnel |
| `ux` | Best practices, anti-patterns | animation, accessibility |
| `react` | React/Next.js performance | waterfall, memo, rerender |
| `web` | App interface guidelines | accessibilityLabel, safe areas |
| `prompt` | AI prompts, CSS keywords | (style name) |

## Available Stacks

| Stack | Focus |
|-------|-------|
| `react-native` | Components, Navigation, Lists |
| `react` | React performance |
| `nextjs` | Next.js SSR/SSG |
| `vue` | Vue 3 Composition API |
| `flutter` | Flutter widgets |
| `swiftui` | SwiftUI native |
| `jetpack-compose` | Jetpack Compose |
| `html-tailwind` | HTML + Tailwind CSS |
| `shadcn` | shadcn/ui components |

## Priority Rules

### CRITICAL
- **Accessibility**: Contrast 4.5:1, Focus states, Alt text, ARIA labels
- **Touch & Interaction**: 44×44pt minimum, 8px spacing, Loading feedback
- **Performance**: WebP/AVIF, Lazy loading, Virtualize lists

### HIGH
- **Style Selection**: Match product type, Consistency, SVG icons (no emoji)
- **Layout & Responsive**: Mobile-first, Breakpoints, No horizontal scroll
- **Navigation**: Bottom nav ≤5 items, Predictable back, Deep linking

### MEDIUM
- **Typography & Color**: Line-height 1.5, Semantic tokens, Font scale
- **Animation**: 150–300ms, ease-out/ease-in, Exit faster than enter
- **Forms**: Visible labels, Error placement, Inline validation

### LOW
- **Charts**: Chart type match data, Accessible colors, Legend visible

## Directory Structure

```
ui-ux-pro-max/
├── SKILL.md                  # CoPaw skill documentation
├── README.md                 # This file
├── data/                     # Design knowledge base
│   ├── colors.csv            # Color palettes
│   ├── styles.csv            # Visual styles
│   ├── typography.csv        # Typography systems
│   ├── ux-guidelines.csv     # UX best practices
│   ├── ux-reasoning.csv      # UX decision logic
│   ├── ui-reasoning.csv      # UI decision logic
│   └── stacks/               # Stack-specific guidelines
│       ├── react.csv
│       ├── vue.csv
│       ├── flutter.csv
│       └── ... (15+ stacks)
├── scripts/
│   ├── search.py             # Main search script
│   ├── core.py               # Core functions
│   └── design_system.py      # Design system generator
└── templates/
    ├── base/                 # Base templates
    │   ├── skill-content.md
    │   └── quick-reference.md
    └── platforms/            # Other platform configs
```

## License

Based on [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) under MIT License.

See [LICENSE](./LICENSE) for details.

## Contributing

Issues and pull requests are welcome! Please feel free to submit improvements or adaptations for other agent platforms.
