# Portfolio — Agentic Coding Guide

## Project Structure
```
portfolio/
├── index.html   # Single-file portfolio (HTML + inline CSS + inline JS)
├── AGENTS.md    # This file
└── .git/
```

## Tech Stack
- Vanilla HTML5, CSS3, JavaScript (no framework, no build tools)
- Dark/light theme via CSS custom properties (`data-theme` attribute)
- IntersectionObserver for scroll animations
- localStorage for theme persistence

## Key Conventions
- **BEM naming**: `.block__element--modifier` for all CSS classes
- **No external dependencies**: everything is self-contained in `index.html`
- **CSS custom props**: theme colors use `--clr-*`, spacing uses `--space-*`, typography uses `--ff-*` / `--fw-*`
- **Inline SVG icons**: all icons are inline `<svg>` elements
- **Forms**: contact form validates on blur + submit, shows inline errors via `.form__error` spans
- **Modal**: project details rendered dynamically from `projectsData` array in JS

## Commands
- **Open in browser**: `start index.html`
- **Lint**: none (vanilla project)

## Project Data
- Projects array lives in the inline `<script>` at the bottom of `index.html`
- Skill percentages use `data-width` attributes on `.skill__fill` elements
- Stats use `data-count` attributes for counter animation
