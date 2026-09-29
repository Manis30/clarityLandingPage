# Clarity

Clarity is a responsive digital-agency landing page built with semantic HTML, custom CSS, and lightweight client-side JavaScript. It presents a polished dark UI for a creative technology studio, with sections for services, work, business results, the team, and contact information.

## Highlights

- Responsive navigation with a mobile menu
- Hero section with calls to action and business metrics
- About section with supporting imagery and company statistics
- Six service cards:
  - Brand identity design
  - UI/UX design
  - Web development
  - Mobile app design
  - Digital marketing
  - SEO optimization
- Filterable portfolio cards for web, mobile, branding, and UI/UX work
- Animated team carousel with responsive breakpoints
- Scroll-aware navigation that highlights the active section
- Scroll-reveal animations powered by AOS
- Responsive layout for mobile, tablet, and desktop screens
- Local SVG favicon matching the Clarity brand
- No build step or package installation required

## Tech stack

| Technology | Purpose |
| --- | --- |
| HTML5 | Page structure and content |
| CSS3 | Responsive layout, theme, components, and animations |
| JavaScript | Portfolio filtering, mobile navigation, active-section tracking, and integrations |
| jQuery 3.7.1 | Owl Carousel initialization |
| Owl Carousel 2.3.4 | Responsive team carousel |
| AOS 2.3.1 | Scroll-reveal animations |
| Font Awesome 7.0.1 | Interface and social icons |
| Google Fonts | Outfit and Poppins typography |

The external libraries are loaded through CDN links in `index.html`. An internet connection is required for those libraries and fonts to load as designed.

## Project structure

```text
.
├── index.html          # Main page markup and inline JavaScript
├── style.css           # Theme, layout, responsive rules, and components
├── favicon.svg         # Local Clarity browser-tab icon
└── image/
    ├── about1.webp     # About section image
    ├── about2.webp     # About section image
    ├── main.webp       # Hero image
    ├── stats.webp      # Results section image
    ├── portfolio-*.webp
    └── person-*.webp   # Portfolio and team imagery
```

## Run locally

Because this is a static site, it can be opened directly in a browser. A local HTTP server is recommended so asset paths and browser behavior match a deployed site.

### Option 1: Python

From the project directory:

```bash
python -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000).

### Option 2: VS Code Live Server

1. Install the **Live Server** extension.
2. Open `index.html`.
3. Select **Go Live**.

### Option 3: Any static web server

Serve the project root as the web root. No compilation or bundling is needed.

## Customization

### Update the brand theme

The main color tokens are defined near the top of `style.css`:

```css
:root {
    --background: #05071e;
    --text: #ffffff;
    --nav-bg: #1b1933;
    --primary-light: #c8c6e3;
    --primary: #524dd3;
    --primary-hover: #3e39db;
}
```

Change these variables to update the page palette consistently.

### Update page content

Edit the relevant section in `index.html`:

- `#home` — hero messaging, CTAs, and headline metrics
- `#about` — company story, highlights, and expertise
- `#service` — service cards and service CTA
- `#portfolio` — project cards and filter categories
- `#stats` — business results and value proposition
- `#team` — team members and carousel content
- `#contact` — contact details and form area
- `#footer` — footer navigation and social links

### Add or replace images

Place new optimized images in `image/` and update the matching `src` and `alt` attributes in `index.html`. Keep descriptive alt text for accessibility.

### Change portfolio categories

Each portfolio card uses a `data-card` value, while each filter button uses a matching `data-filter` value:

```html
<button data-filter="web">Web Design</button>
<div class="portfolio-cards" data-card="web">...</div>
```

Use the same value in both places for the filter to work.

## Deployment

The project can be deployed to any static hosting provider, including:

- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages
- Azure Static Web Apps
- Any Nginx, Apache, or object-storage static website host

Upload or connect the project root and use `index.html` as the entry point. No server-side runtime is needed.

## Accessibility and content checklist

Before publishing, replace placeholder copy and empty links with production content:

- Update the lorem ipsum descriptions and placeholder footer labels.
- Replace empty `href=""` values with real destinations.
- Add real URLs for LinkedIn, X, Facebook, and Instagram.
- Confirm every image has accurate, descriptive alt text.
- Add a real contact form endpoint or connect the contact CTA to an email/contact workflow.
- Test keyboard navigation, focus states, and mobile menu behavior.
- Test the page with JavaScript disabled if a progressively enhanced experience is required.

## Browser support

The page is intended for current versions of Chrome, Edge, Firefox, and Safari on desktop and mobile. JavaScript is required for portfolio filtering, the mobile menu, active navigation state, animations, and the team carousel.

## License

No license has been included yet. Add a license file before distributing the project or reusing it commercially.

