# NYC Landmarks — Site Map

## Pages

All HTML pages are in the same folder. The home page links to each landmark page.

| Page | Filename |
| --- | --- |
| Home | `index.html` |
| Statue of Liberty | `landmark-liberty.html` |
| Empire State Building | `landmark-empire.html` |
| Staten Island Ferry | `landmark-ferry.html` |
| Wonder Wheel | `landmark-wonder.html` |
| Yankee Stadium | `landmark-yankee.html` |
| Roosevelt Island Tramway | `landmark-tram.html` |

## Page content

- **Home:** 
    - Introduction
    - embedded video
    - featured Empire State Building image and description
    - six credited landmark cards linking to their pages.
- **Landmark pages:** 
    - Landmark name
    - introduction
    - credited hero image, with an art-directed square mobile crop
    - About section with Built and Today text
    - Directions with Google Maps and Apple Maps links
    - More Info links
    - optional additional images where applicable
    - Previous/Next links.
- **Every page:** 
    - Shared header element with site name and navigation
    - seven-link primary navigation, with the current page marked using `aria-current="page"`
    - main element with page-specific content
    - Shared footer element.

## Navigation

Primary navigation links to all seven pages in the order listed above.

Previous/Next links follow this loop, with Home outside the sequence:

Statue of Liberty → Empire State Building → Staten Island Ferry → Wonder Wheel → Yankee Stadium → Roosevelt Island Tramway → Statue of Liberty

Use the filenames above as relative link destinations.

## Responsive behavior

- The CSS uses a mobile-first layout. The homepage landmark grid and Wonder Wheel gallery use one column by default, two columns at 645px and wider, and three columns at 1024px and wider.
- At viewport widths up to 600px, the header, main content, and footer use the mobile padding adjustment.
- The seven-link primary navigation is a flexbox list that wraps to additional lines as needed; it does not use a hamburger menu or JavaScript.
- Landmark hero `<picture>` elements use the matching file under `images/square/` at widths up to 644px. The existing original image in each `<img>` is the tablet/desktop fallback.

## Published sites

- GitHub Pages: [https://elianny200527.github.io/mmp240-project2/](https://elianny200527.github.io/mmp240-project2/)
- Netlify: [https://project3mmp240.netlify.app/](https://project3mmp240.netlify.app/)

The Wonder Wheel gallery markup references three image files that are currently missing from `images/square/`: `pexels-kyle-miller-169884138-27462439_sq.jpg`, `pexels-clement-proust-363898785-24730360_sq.jpg`, and `pexels-dimitry-mak-1310041547-30911091_sq.jpg`. Other image paths should not be assumed verified without checking the assets.
