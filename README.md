# NYC Landmarks — Project 3

## Project Overview

NYC Landmarks is a responsive seven-page website that helps visitors explore six famous New York City landmarks. Its green-and-cream palette, Montserrat headings, Open Sans body text, and flexible layouts support visitors using phones, tablets, and desktop screens. The home page links to six landmark detail pages with history, visitor information, photo credits, and directions.

## Target Audience

People who want information about some of New York City's major landmarks. They may be comparing places to visit while planning at home or looking up information on a phone while traveling around the city. The site should help them quickly understand what each landmark offers and find links to visitor information and directions.

## Goals

### User Goals

- Pick landmarks of interest by browsing images, short introductions, and more detailed landmark pages.
- Find links to directions, transportation, and visitor information to help plan a trip to a landmark.
- Scan headings, text, and navigation easily while using the site on the go.

### Creator Goals

- Improve my HTML and CSS skills by creating a responsive website that works well on mobile phones, tablets, and desktop computers.
- Learn how to use media queries and responsive navigation to make the website easier to use on different screen sizes.
- Create a professional and visually consistent multi-page website that I can include in my web design portfolio.
 

## Scope of Work

A responsive NYC landmarks website with **seven pages total**:

- One home page, `index.html`.
- Six individual landmark pages, with landmark text, images, and links.

The site architecture is defined in the `site-map.md` file.

Reuse a consistent header, responsive seven-link navigation, and footer across all pages. The homepage landmark cards link to their detail pages, and Previous/Next links follow the six-landmark loop. Fluid layouts, flexible media, art-directed hero images, and media queries support mobile, tablet, and desktop screens. The current visual system is documented in `design.md`.

The site is an informational guide. Ticket booking, accounts, live transit data, and a custom trip planner are outside this project's scope; link to appropriate visitor-information sources instead.

## Deployment

- **GitHub Pages:** [https://elianny200527.github.io/mmp240-project2/](https://elianny200527.github.io/mmp240-project2/)
- **Netlify:** [https://project3mmp240.netlify.app/](https://project3mmp240.netlify.app/)

Both deployment URLs were reachable when this document was updated.

## Content Summary

| Page | Content |
| --- | --- |
| Home | Introduction to NYC landmarks, embedded video, featured Empire State Building image and text, and six credited landmark cards linking to their pages. |
| Statue of Liberty | Introduction, hero image, About text covering its history and present use, and More Info links including visitor information and directions. |
| Empire State Building | Introduction, hero image, About text covering its history and present use, and More Info links including visitor information. |
| Staten Island Ferry | Introduction, hero image, About text covering its history and present use, and More Info links including schedules and directions. |
| Wonder Wheel | Introduction, hero image, About text covering its history and present use, More Info links, a gallery with three credited images, and Previous/Next links. |
| Yankee Stadium | Introduction, hero image, About text covering its history and present use, and More Info links including the visitor reference guide. |
| Roosevelt Island Tramway | Introduction, hero image, About text covering its history and present use, and More Info links including riding information and directions. |

Preserve the landmark text, links, and photo credits.

**Known image-path issue:** The Wonder Wheel gallery in `landmark-wonder.html` references three square image files that are not currently present in `images/square/`: `pexels-kyle-miller-169884138-27462439_sq.jpg`, `pexels-clement-proust-363898785-24730360_sq.jpg`, and `pexels-dimitry-mak-1310041547-30911091_sq.jpg`. The matching photos have not been found in the project assets; do not treat all image paths as verified.

## Success Criteria

Use this checklist to distinguish implemented structure from checks that still need manual verification.

- [x] Seven HTML pages are present: one home page and six landmark detail pages; homepage cards and landmark navigation link to the detail pages.
- [x] Fluid image/video rules and responsive layouts are implemented in `style.css`.
- [x] Mobile, tablet, and desktop breakpoints are implemented at 600px, 645px, and 1024px.
- [x] All pages include the same seven-link navigation, with the current page identified using `aria-current="page"`.
- [x] Each landmark detail page includes a page-title `h1`, hero image, landmark content, and Previous/Next navigation.
- [x] Pages use shared `header`, `nav`, `main`, and `footer` elements and load `tokens.css` before `style.css`.
- [x] Hero images use `<picture>` to select square mobile crops through 644px and retain the original image as the fallback.
- [ ] Confirm every local image path works; the three Wonder Wheel gallery image files listed above are currently missing.
- [ ] Test keyboard access, focus visibility, color contrast, and other accessibility requirements; no full accessibility audit is documented.
- [ ] Check the rendered pages at narrow, tablet, and wide widths and validate the HTML/CSS.
- [ ] Confirm all published internal paths and images, then commit the final project.

## Documentation

- **[README.md](README.md)** — This project's overview, audience, goals, scope, content summary, and success criteria. Keep it current as project decisions change.
- **[site-map.md](site-map.md)** — The page list, exact filenames, shared page structure, and navigation relationships.
- **[design.md](design.md)** — The site's typography, colors, spacing, and other visual design decisions.
- **[.github/copilot-instructions.md](.github/copilot-instructions.md)** — Project-specific instructions for GitHub Copilot, including content preservation, development standards, and verification. The planning documents also support work without AI.
