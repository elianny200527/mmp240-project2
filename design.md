---
version: 2
project: 3
name: "NYC Landmarks"
description: "This design system supports the responsive NYC Landmarks Project 3 website, helping tourists and visitors explore six New York City landmarks. The design uses clean typography, balanced spacing, and a welcoming green-and-cream palette."
tokensFile: "tokens.css"
colors:
  defaultText: "var(--primary-text)"
  defaultBackground: "var(--primary-background)"
  action: "var(--action)"
  hover: "var(--action-hover)"
  buttonText: "var(--button-text)"
  alternateText: "var(--alternate-text)"
  alternateBackground: "var(--alternate-background)"
  alternateAction: "var(--alternate-action)"
  alternateHover: "var(--alternate-action-hover)"
  alternateButtonText: "var(--alternate-button-text)"
typography:
  rootSizeSource: "html font-size in tokens.css"
  bodyFamily: "var(--base-family)"
  headingFamily: "var(--headings-family)"
  bodySize: "var(--text-size-md)"
  smallSize: "var(--text-size-sm)"
  bodyLineHeight: "var(--line-height-base)"
  headingLineHeight: "var(--line-height-headings)"
textScale:
  xs: "var(--text-size-xs)"
  sm: "var(--text-size-sm)"
  md: "var(--text-size-md)"
  lg: "var(--text-size-lg)"
  xl: "var(--text-size-xl)"
  2xl: "var(--text-size-2xl)"
  3xl: "var(--text-size-3xl)"
headingSizes:
  h1: "var(--text-size-3xl)"
  h2: "var(--text-size-2xl)"
  h3: "var(--text-size-xl)"
  h4: "var(--text-size-lg)"
  h5: "var(--text-size-md)"
  h6: "var(--text-size-sm)"
spacing:
  base: "var(--space-unit)"
  space-1: "var(--space-1)"
  space-2: "var(--space-2)"
  space-3: "var(--space-3)"
  space-4: "var(--space-4)"
  space-6: "var(--space-6)"
  space-8: "var(--space-8)"
  space-12: "var(--space-12)"
  space-16: "var(--space-16)"
  space-24: "var(--space-24)"
  space-32: "var(--space-32)"
layout:
  pageWidth: "var(--page-width)"
  gridGap: "var(--grid-gap)"
  sectionSpacing: "var(--section-spacing)"
  contentPadding: "var(--content-padding)"
---

# Design system

## Overview

This design system is for NYC Landmarks Project 3, a responsive website with one home page and six landmark detail pages. The visual system uses a green-and-cream palette, Montserrat headings, Open Sans body text, and token-based spacing.

This guide describes the choices in tokens.css. Use the CSS variables above rather than copying their values. Keep design.md and tokens.css in your project folder, and link tokens.css before your own stylesheet on every page. Add page-specific styling in your own stylesheet.

## Colors

Use `var(--primary-text)` on `var(--primary-background)` for the default palette. Add the alternate class to use `var(--alternate-text)` on `var(--alternate-background)`.

The token values are `--primary-text: #24352D`, `--primary-background: #F8F7F1`, `--action: #38594A`, `--action-hover: #243F32`, and `--button-text: #FFFFFF`. Alternate colors are `--alternate-text: #F8F7F1`, `--alternate-background: #38594A`, `--alternate-action: #FFFFFF`, `--alternate-action-hover: #DDEBDD`, and `--alternate-button-text: #38594A`. Gallery cards use white surfaces in `style.css`.

Default links are underlined. The primary navigation, pagination buttons, and landmark-card title links intentionally remove underlines and use other visual styling; the current navigation item uses `aria-current="page"`.

### Contrast targets

Aim for WCAG AAA contrast for normal text; WCAG AA is the minimum. Check these text/background pairings, including hover states:

- `var(--primary-text)` on `var(--primary-background)`
- `var(--action)` on `var(--primary-background)`
- `var(--action-hover)` on `var(--primary-background)`
- `var(--button-text)` on `var(--action)`
- `var(--button-text)` on `var(--action-hover)`
- `var(--alternate-text)` on `var(--alternate-background)`
- `var(--alternate-action)` on `var(--alternate-background)`
- `var(--alternate-action-hover)` on `var(--alternate-background)`
- `var(--alternate-button-text)` on `var(--alternate-action)`
- `var(--alternate-button-text)` on `var(--alternate-action-hover)`

These are contrast targets, not documented test results. No complete contrast or accessibility audit is claimed here.

## Typography

Use `var(--base-family)` (Open Sans) for body text and `var(--headings-family)` (Montserrat) for headings. Body text uses `var(--text-size-md)`, small text uses `var(--text-size-sm)`, and headings use the sizes in headingSizes above.

Use `var(--line-height-base)` for body line height and `var(--line-height-headings)` for heading line height. The html rule in tokens.css sets the root size; rem-based sizes scale from it. The 2xl and 3xl text-scale labels correspond to `--text-size-2xl` and `--text-size-3xl`.

## Spacing and layout

Use the spacing variables listed above. Each --space-N token is a multiplier of `var(--space-unit)`.

- `var(--page-width)`: maximum page width.
- `var(--grid-gap)`: space between grid items, not around the grid.
- `var(--section-spacing)`: space between sections.
- `var(--content-padding)`: padding inside sections, outside a nested grid.

Read tokens.css to see which spacing step each layout variable uses. Text wraps within its containing element; there is no separate line-length variable.

## Responsive behavior and imagery

The responsive CSS is mobile-first. At 645px and wider, the homepage landmark grid and Wonder Wheel gallery change to two columns; at 1024px and wider, they change to three columns. At widths up to 600px, header, main, and footer padding is adjusted for mobile. Desktop layouts also apply wider page padding and constrain selected landmark content.

Each of the six landmark detail pages uses a `<picture>` hero: the matching square image in `images/square/` is selected up to 644px, while the original full-size image remains the `<img>` fallback for larger screens. The homepage featured image also has mobile and desktop `<source>` entries. The Wonder Wheel gallery references three additional square images that are currently absent from the project folder; those paths are not verified.

The primary navigation is a seven-link flexbox list that wraps on smaller screens. There is no hamburger menu or navigation JavaScript.

## Deployment

- GitHub Pages: [https://elianny200527.github.io/mmp240-project2/](https://elianny200527.github.io/mmp240-project2/)
- Netlify: [https://project3mmp240.netlify.app/](https://project3mmp240.netlify.app/)

Both URLs were reachable when this documentation was updated.

## Do and Don't

### Do

- Use the same tokens.css on every page to keep the design consistent.
- Reuse the CSS variables for colors, typography, spacing, and layout.
- Use headings in order, beginning with one page-title h1.
- Keep underlined links and visible keyboard focus.

### Don't

- Add one-off design values when an existing variable fits.
- Rely on color alone to communicate meaning.
- Change a design choice in only one project file. Keep this guide and `tokens.css` in sync when the design changes.
