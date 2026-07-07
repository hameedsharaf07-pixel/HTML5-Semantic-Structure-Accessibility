# Semantic HTML5 & Accessibility Demo

A single-page HTML5 template demonstrating semantic markup and accessibility (a11y) best practices. Use it as a reference or starting point for building accessible web pages.

## Files

- `semantic-accessibility-demo.html` — self-contained HTML file (inline CSS, no dependencies)

## Features

### Semantic structure
- `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`, `<footer>` used for their intended purpose instead of generic `<div>`s
- `<figure>` / `<figcaption>` for images with captions
- Proper heading hierarchy (`h1` → `h2` → `h3`)

### Accessibility
- **Skip link** — hidden off-screen until keyboard focus, lets users bypass repeated navigation
- **Landmark labeling** — `aria-label` on `<nav>`, `aria-labelledby` on sections/aside tied to their headings
- **Form accessibility** — every input has a matching `<label for>`, plus `aria-required` and `aria-describedby` for extra context
- **Descriptive alt text** on images (not just filenames)
- **Visible focus states** — keyboard focus outlines on links, buttons, and inputs
- **`.sr-only` utility class** — hides content visually while keeping it available to screen readers
- **Responsive layout** — two-column grid collapses to one column under 700px

## How to use

1. Open `semantic-accessibility-demo.html` directly in a browser, or
2. Copy the relevant sections (skip link, form pattern, `.sr-only` class) into your own project

## Testing accessibility

- **Keyboard only**: Tab through the page — the skip link and all interactive elements should get a visible focus outline
- **Screen reader**: Test with VoiceOver (Mac), NVDA (Windows), or a browser extension
- **Automated checks**: Run [axe DevTools](https://www.deque.com/axe/devtools/) or Lighthouse's Accessibility audit in Chrome DevTools

## Customization notes

- Colors are defined as CSS custom properties (`--text`, `--bg`, `--accent`, `--muted`) at the top of the `<style>` block — change them there to retheme
- Replace the placeholder image URL with your own asset (update `alt` text accordingly)
- Add real form handling (JS validation or a backend endpoint) — the current form has no submit logic

## Reference

- [W3C: Intro to Web Accessibility](https://www.w3.org/WAI/fundamentals/accessibility-intro/)
- [MDN: HTML Elements Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
