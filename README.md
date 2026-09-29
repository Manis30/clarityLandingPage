# Clarity — Digital Agency Landing Page

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Owl Carousel](https://img.shields.io/badge/Owl_Carousel-2.3.4-blue?style=for-the-badge)](https://owlcarousel2.github.io/OwlCarousel2/)
[![AOS](https://img.shields.io/badge/AOS-2.3.1-orange?style=for-the-badge)](https://michalsnik.github.io/aos/)
[![Responsive](https://img.shields.io/badge/Responsive-Mobile%20%7C%20Tablet%20%7C%20Desktop-success?style=for-the-badge)](#responsive-design--breakpoints)

**Clarity** is a modern, responsive digital-agency landing page engineered with semantic HTML5, pure CSS3, and vanilla JavaScript. Featuring a curated dark theme, fluid glassmorphism aesthetics, scroll-triggered animations, dynamic client-side portfolio filtering, and a responsive team carousel, Clarity delivers a premier web presence for technology studios, creative agencies, and digital consulting firms.

---

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Page Architecture](#page-architecture)
- [Tech Stack & Dependencies](#tech-stack--dependencies)
- [Project Structure](#project-structure)
- [Quick Start & Local Setup](#quick-start--local-setup)
- [Responsive Design & Breakpoints](#responsive-design--breakpoints)
- [Customization Guide](#customization-guide)
  - [Color Palette](#color-palette)
  - [Portfolio Filter Setup](#portfolio-filter-setup)
  - [Carousel Configuration](#carousel-configuration)
  - [Form Integration](#form-integration)
- [SEO & Accessibility](#seo--accessibility)
- [Browser Compatibility](#browser-compatibility)
- [License](#license)

---

## Overview

Clarity is built from the ground up without heavy frontend frameworks or build tools. It offers:
- **Instant load times**: Pure static files delivered with CDN-based assets.
- **Flawless responsiveness**: Tailored layout adaptations from 320px mobile screens to ultra-wide 4K monitors.
- **Fluid interactions**: Micro-interactions, hover elevations, scroll-spy active link tracking, and subtle animations via AOS (Animate On Scroll).
- **Clean dark aesthetic**: Built with a deep navy palette (`#05071e`), vibrant indigo accents (`#524dd3`), and glassmorphism overlays.

---

## Key Features

- **Sticky Glassmorphism Navbar**: Floating pill header with scroll-spy navigation that dynamically highlights the active section.
- **Mobile Drawer Navigation**: Full-screen backdrop-blurred overlay menu with smooth open/close triggers and touch-friendly targets.
- **Hero / Value Proposition**: Strong headline messaging, dual call-to-action buttons, key business metrics, and hero graphic.
- **About Showcase**: Layered, overlapping imagery with floating statistics badge and bulleted capability highlights.
- **Service Offerings**: 6 distinct service cards with custom icons, badge ribbons, hover lift animations, and conversion banner.
- **Client-Side Filterable Portfolio**: Real-time category filtering (`All`, `Web Design`, `Mobile Apps`, `Branding`, `UI/UX`) without page reloads, accompanied by review ratings and technology tags.
- **Business Proof & Statistics**: ROI benchmarks, client satisfaction metrics, and brand differentiators.
- **Touch-Ready Team Carousel**: Owl Carousel slider displaying team members with social links, responsive card margins, and autoplay.
- **Interactive Contact Section**: Multi-channel communication cards, SLA response metrics, and an integrated project inquiry form.
- **Comprehensive Global Footer**: Multi-column site links, contact info, social handles, and branding.
- **Edge-to-Edge Layout**: Integrated cross-browser scrollbar refinement that maintains native scrollability without distracting desktop scrollbars.

---

## Page Architecture

The landing page is organized into semantic, self-contained sections:

| Section | Anchor ID | Purpose |
| :--- | :--- | :--- |
| **Header** | — | Sticky pill navbar, brand logo, navigation links, CTA, and mobile hamburger button |
| **Mobile Menu** | — | Fixed overlay drawer with backdrop blur and animated navigation links |
| **Hero** | `#home` | Primary headline, introduction, conversion buttons, and metric counters |
| **About** | `#about` | Company narrative, capability checklist, overlapping imagery, and experience badges |
| **Services** | `#service` | Service grid, icon headers, feature summaries, and call-to-action banner |
| **Portfolio** | `#portfolio` | Dynamic category tabs and responsive project cards with tech stack badges |
| **Stats & Why Us** | `#stats` | Performance highlights, satisfaction ratings, and feature checkmarks |
| **Team** | `#team` | Responsive Owl Carousel featuring leadership profiles and social handles |
| **Contact** | `#contact` | Project inquiry form, direct contact cards, response time stats, and social links |
| **Footer** | `#footer` | Brand recap, address info, categorized site links, and legal placeholders |

---

## Tech Stack & Dependencies

### Core Technologies
- **HTML5**: Semantic tags (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`) for structural integrity and SEO.
- **CSS3**: Custom design tokens (CSS variables), Flexbox, CSS Grid, media queries, and transition effects.
- **JavaScript (ES6+)**: Vanilla DOM scripting for mobile navigation, scroll-spy tracking, and portfolio filtering.

### Third-Party Libraries (Loaded via CDN)
| Library | Version | Purpose |
| :--- | :--- | :--- |
| **[jQuery](https://jquery.com/)** | 3.7.1 | Core dependency required by Owl Carousel |
| **[Owl Carousel](https://owlcarousel2.github.io/OwlCarousel2/)** | 2.3.4 | Touch-enabled responsive team carousel |
| **[AOS](https://michalsnik.github.io/aos/)** | 2.3.1 | Scroll-reveal animation triggers (`fade-up`, `fade-right`, `fade-left`) |
| **[Font Awesome](https://fontawesome.com/)** | 7.0.1 | Modern SVG vector icons for UI and social platforms |
| **[Google Fonts](https://fonts.google.com/)** | — | Typographic pairings: **Outfit** and **Poppins** |

---

## Project Structure

```text
.
├── index.html          # Main HTML structure, section markup, and inline scripts
├── style.css           # Global design system, layout rules, and media queries
├── favicon.svg         # SVG favicon matching the Clarity brand identity
├── README.md           # Project documentation and developer reference
└── image/              # Optimized web imagery
    ├── main.webp       # Hero banner illustration
    ├── about1.webp     # Primary about image
    ├── about2.webp     # Overlapping about accent image
    ├── stats.webp      # Results and metrics graphic
    ├── portfolio-7.webp to portfolio-12.webp # Portfolio project mockups
    └── person-5.webp to person-8.webp       # Team member portraits
```

---

## Quick Start & Local Setup

Because Clarity is a 100% static project, no build step, compiler, or package manager installation is required.

### Option 1: Python HTTP Server (Recommended)
Run the built-in HTTP server directly from the project directory:

```bash
# Python 3
python -m http.server 8080
```
Open [http://localhost:8080](http://localhost:8080) in your browser.

### Option 2: Node.js `npx serve`
```bash
npx serve -l 8080
```
Open [http://localhost:8080](http://localhost:8080) in your browser.

### Option 3: VS Code Live Server Extension
1. Open the project folder in **Visual Studio Code**.
2. Install the **Live Server** extension (`ritwickdey.liveserver`).
3. Right-click [`index.html`](file:///d:/LearningTask/week1/index.html) and select **Open with Live Server**.

### Option 4: Direct Browser Execution
Double-click [`index.html`](file:///d:/LearningTask/week1/index.html) to open the file directly in any modern browser using the `file://` protocol.

---

## Responsive Design & Breakpoints

The responsive architecture is implemented via progressive `max-width` cascading breakpoints in [`style.css`](file:///d:/LearningTask/week1/style.css):

| Device / Viewport | Breakpoint | Layout Adaptations |
| :--- | :--- | :--- |
| **Large Desktop** | `> 1200px` | 3-column team carousel, 3-column portfolio, 3-column stats, 5-column footer, side-by-side hero and contact layouts |
| **Small Desktop / Laptop** | `≤ 1200px` | Proportional container paddings, auto-fit card grids, balanced footer spacing |
| **Tablet (Landscape & Portrait)** | `≤ 991px` | Full navigation switches to mobile hamburger menu; hero, about, stats, and contact stack vertically; 2-column service & portfolio grids; 2-column footer |
| **Large Mobile / Phablets** | `≤ 767px` | 1-column service cards, 1-column portfolio cards, 1-column stats cards; compact stats pill |
| **Standard Mobile** | `≤ 480px` | Full-width stacked CTA buttons, stacked form inputs ("Your Name" / "Email"), compact typography, 1-column footer |
| **Extra-Small Mobile** | `≤ 360px` | Stacked metric items, streamlined about imagery to prevent micro-screen visual clutter |

---

## Customization Guide

### Color Palette
Global color tokens are declared in the `:root` pseudo-class at the top of [`style.css`](file:///d:/LearningTask/week1/style.css):

```css
:root {
    --background: #05071e;    /* Deep navy background */
    --text: #ffffff;          /* Pure white body and headline text */
    --nav-bg: #1b1933;        /* Pill navbar background */
    --primary-light: #c8c6e3;  /* Subdued lavender body text */
    --primary: #524dd3;        /* Vibrant brand indigo accent */
    --primary-hover: #3e39db;  /* Hover state for buttons and links */
}
```

### Portfolio Filter Setup
To add or modify portfolio items, ensure the button's `data-filter` value matches the card's `data-card` value:

```html
<!-- Filter Button -->
<button type="button" data-filter="mobile">Mobile Apps</button>

<!-- Matching Card -->
<div class="portfolio-cards" data-card="mobile">
    <!-- Card content -->
</div>
```
To show a card under all categories, setting `data-filter="all"` displays every card regardless of its individual `data-card` attribute.

### Carousel Configuration
The team carousel is configured via Owl Carousel options in the script block of [`index.html`](file:///d:/LearningTask/week1/index.html):

```javascript
var owl = $('.owl-carousel');
owl.owlCarousel({
    items: 4,
    loop: true,
    margin: 30,
    autoplay: true,
    autoplayTimeout: 2000,
    autoplayHoverPause: true,
    responsive: {
        0:    { items: 1, margin: 15 },
        576:  { items: 1, margin: 20 },
        768:  { items: 2, margin: 25 },
        992:  { items: 2, margin: 30 },
        1200: { items: 3, margin: 30 }
    }
});
```

### Form Integration
The contact form in [`index.html`](file:///d:/LearningTask/week1/index.html#L487-L496) is structured for easy integration with form-handling backends or third-party services (such as [Formspree](https://formspree.io/), [FormKeep](https://formkeep.com/), or custom REST endpoints):

```html
<form class="contact-form" action="https://formspree.io/f/{your_id}" method="POST">
    <div>
        <input type="text" name="name" placeholder="Your Name" required class="contact-input" />
        <input type="email" name="email" placeholder="Email Address" required class="contact-input" />
    </div>
    <input type="text" name="subject" placeholder="What's This About" required />
    <textarea name="message" placeholder="Tell Us More About Your Project" required></textarea>
    <button type="submit">Send Message <i class="fa-solid fa-paper-plane"></i></button>
</form>
```

---

## SEO & Accessibility

- **Semantic HTML**: Proper heading hierarchy (`<h1>` through `<h6>`) and landmark roles (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`).
- **Responsive Viewport**: Configured with `<meta name="viewport" content="width=device-width, initial-scale=1.0">`.
- **Keyboard & Touch Accessible**: Interactive buttons, mobile menu toggle, and focusable form controls.
- **Asset Optimization**: High-efficiency modern `.webp` imagery utilized throughout all sections.
- **Scroll Refinement**: Seamless hidden scrollbar styling using `scrollbar-width: none` and `::-webkit-scrollbar` while fully preserving standard mouse, keyboard, and touch navigation.

---

## Browser Compatibility

Tested and supported on the latest stable versions of:
- **Google Chrome** (Windows, macOS, Android, iOS)
- **Mozilla Firefox** (Windows, macOS, Linux, Android)
- **Apple Safari** (macOS, iOS, iPadOS)
- **Microsoft Edge** (Windows, macOS)
- **Opera & Brave**

---

## License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT). Feel free to adapt and customize it for personal or commercial projects.
