# Frontend Mentor - Digitalbank landing page solution

This is a solution to the [Digitalbank landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/digital-bank-landing-page-WaUhkoDN). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot

![Desktop](./screenshots/Screenshot%20Desktop.png)
![Mobile](./screenshots/Screenshot%20Mobile.png)

### Links

- Solution URL: https://github.com/Yahyaball/digitalbank-landing-page
- Live Site URL: https://digitalbank-landing-page-sigma.vercel.app

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- SCSS
- TypeScript
- [Vite](https://vite.dev/)
- [Vue](https://vuejs.org/) - JavaScript framework

### What I learned

#### Vue 3 & Composition API

- **Biggest win:** Understanding `nextTick()` for focus management — the DOM doesn't update synchronously when refs change
- **Pattern I'll reuse:** `ref<HTMLElement | null>(null)` + `onMounted` for DOM access
- **Still fuzzy:** When to use `computed` vs `watch` vs `watchEffect`

#### Accessibility

- **Proud of:** Building a fully keyboard-accessible mobile nav with focus trap + restoration
- **Hard lesson:** `inert` on `<body>` breaks everything inside — must scope to content wrapper
- **New habit:** Always test with keyboard only (Tab, Shift+Tab, Escape, Enter, Space)

#### Responsive Design

- **Mobile-first mindset:** Start at 375px, layer complexity at 48rem/64rem
- **Fluid typography:** `clamp(2rem, 1.5rem + 2vw, 3.5rem)` beats fixed breakpoints
- **CLS prevention:** `aspect-ratio` + `width/height` on all images

### Continued development

#### Patterns I'll Reuse

- **Composables for reusable logic** — extracted `useMediaQuery`, `useFocusTrap` from this project
- **Accessibility-first component APIs** — required props for labels, sensible defaults
- **SCSS variable system** — single source of truth for spacing, z-index, breakpoints

#### Habits I'm Building

- A11y checklist before writing any component code
- Extract composables when logic appears twice
- Keyboard-only testing as part of dev workflow
- Document "why" in code comments for future reference

#### Tools for Next Project

- Vitest + @vue/test-utils for unit tests
- Playwright + axe-playwright for e2e + a11y testing
- ESLint + Prettier + Husky for code quality
- GitHub Actions for CI/CD

#### Anti-Patterns I'll Avoid

- Direct DOM queries in components
- Module-level side effects
- Magic numbers in CSS
- `href="#"` on non-links
- Scoping accessibility attributes too broadly

### AI Collaboration

**Tool:** OpenCode (Nemotron 3 Ultra)

**How we worked:**

- I drove design decisions; AI implemented patterns I described
- AI caught bugs I couldn't see (inert scope, top-level side effects)
- AI taught me _why_ patterns work (render cycle, focus management)

**Best prompts I used:**

1. "How do I toggle `inert` only on page content, not header?"
2. "Fix 'nav is possibly null' TypeScript error"
3. "Why does my close button stop working when nav opens?"

**What I'd change:** Start with a11y checklist, extract composables earlier, add tests from day one.

## Author

- Frontend Mentor - [@Yahyaball](https://www.frontendmentor.io/profile/Yahyaball)
