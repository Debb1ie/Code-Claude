# Claude — Intelligent Thinking Partner

A fully static, single-file landing page for Claude, the AI assistant built by Anthropic. This project presents Claude's purpose, architecture, services, and design principles through a production-grade editorial web experience

---

## Overview

This repository contains a self-contained HTML landing page (`claude-webapp.html`) designed to communicate what Claude is, how it works, and why it was built. No frameworks, no build tools, no dependencies beyond two Google Fonts imports.

---

## Features

- Fixed navigation with blur backdrop and smooth scroll anchors
- Animated hero section with rotating ornamental rings and staggered fade-in
- Purpose section with key statistics on a dark background
- Architecture grid detailing six core AI systems
- Services section with four capability cards
- Live chat window mockup demonstrating Claude's conversational style
- Core principles section covering helpfulness, honesty, safety, and nuance
- Four-step "How It Works" flow
- Testimonials from representative user archetypes
- Call-to-action section with pricing note
- Scroll-triggered fade-in animations via IntersectionObserver
- Fully responsive down to mobile viewports

---

## Tech Stack

| Layer | Choice |
|---|---|
| Markup | HTML5, semantic structure |
| Styling | Vanilla CSS with custom properties |
| Typography | Fraunces (display serif) + DM Sans (body) via Google Fonts |
| Animation | CSS keyframes + IntersectionObserver API |
| Dependencies | None (zero npm packages, zero bundler) |

---

## File Structure

```
claude-webapp/
├── claude-webapp.html    # Complete single-file application
└── README.md             # This file
```

---

## Getting Started

Clone the repository and open the file directly in any modern browser. No server required.

```bash
git clone https://github.com/your-username/claude-webapp.git
cd claude-webapp
open claude-webapp.html
```

Or serve it locally if you prefer:

```bash
npx serve .
# or
python3 -m http.server 8080
```

---

## Design System

The visual language is built around a warm editorial palette with two typefaces and a set of CSS custom properties.

### Color Tokens

```css
--cream:       #F7F4EE   /* page background */
--ink:         #1A1714   /* primary text and dark surfaces */
--ink-light:   #4A4540   /* secondary text */
--ink-muted:   #8A847D   /* tertiary text, labels */
--terra:       #C4632A   /* accent, hover states, highlights */
--terra-light: #E8A070   /* accent on dark backgrounds */
--sage:        #3D6B4F   /* status indicators, success states */
--gold:        #B8962E   /* tertiary accent */
```

### Typography

- Display headings: `Fraunces`, weight 300-400, optical size 9-144
- Body and UI: `DM Sans`, weight 300-500, optical size 9-40
- Base size: 16px, line-height 1.6-1.75

---

## Sections

| Anchor | Section | Description |
|---|---|---|
| `#purpose` | Purpose | Mission statement and key capability statistics |
| `#architecture` | Architecture | Six-card grid of Claude's technical systems |
| `#services` | Services | Writing, Code, Research, and Learning capabilities |
| — | Chat Demo | Illustrative chat window with sample exchange |
| `#principles` | Principles | Helpful, Honest, Harmless, Nuanced |
| `#how` | How It Works | Four-step user journey |
| — | Testimonials | Quotes from researcher, engineer, and strategist |

---

## Customization

All colors are defined as CSS custom properties on `:root` and can be overridden globally. Section content is plain HTML with no templating engine or component abstraction, making edits straightforward.

To change the accent color throughout:

```css
:root {
  --terra: #your-color;
  --terra-light: #your-lighter-color;
}
```

To add a new service card, copy any `.service-card` block inside `.services-grid` and update the number, heading, description, and list items.

---

## Browser Support

Tested and functional in all evergreen browsers. The IntersectionObserver animation degrades gracefully in older environments — content remains visible, animations simply do not trigger.

---

## License

MIT. Use freely for personal and commercial projects. Attribution appreciated but not required.

---

## Resources

For the live product, visit [claude.ai](https://claude.ai).  
For API access and documentation, visit [docs.anthropic.com](https://docs.anthropic.com).
