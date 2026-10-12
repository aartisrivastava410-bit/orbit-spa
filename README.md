# Orbit SPA

A Single Page Application (SPA) simulation built with plain **HTML, CSS and JavaScript**, with no frameworks. It was created for the Week 5 task of my Frontend Web Development internship at YuvaIntern.

The app loads content dynamically into one page without any full page reload, and the URL and browser Back/Forward buttons stay in sync.

## Features

- Client-side router built on the History API (`pushState` / `popstate`)
- Hash-routing fallback when opened directly from disk (`file://`)
- Dynamic route parameters (for example `/products/3`)
- Animated page transitions and a loading progress bar
- Simulated async data loading for the gadget list and detail pages
- Live search filter on the gadgets page
- Contact form with validation
- 404 page and error handling for failed loads
- Responsive layout with a mobile menu
- Accessibility: skip link, ARIA live region, focus management

## Pages

| Route | View |
|-------|------|
| `/` | Home |
| `/products` | Gadget list |
| `/products/:id` | Gadget details |
| `/about` | About |
| `/contact` | Contact form |
| any other path | 404 page |

## Project Structure

    index.html        main container (#app)
    css/style.css     styles, transitions, responsive layout
    js/data.js        simulated async data source
    js/views.js       view templates
    js/router.js      client-side router
    server.py         optional dev server for clean URLs

## How to Run

**Quick way:** open `index.html` in a browser. It uses hash URLs such as `#/products`.

**Full History API mode:**

    python server.py

Then open http://localhost:8000. Clean URLs like `/products/3` work, and refreshing a deep link works too.

## Technologies

HTML5, CSS3 (custom properties, grid, flexbox, transitions), vanilla JavaScript (ES6+, async/await, History API).

## Author
Aarti Srivastava - Frontend Web Development Intern, YuvaIntern
