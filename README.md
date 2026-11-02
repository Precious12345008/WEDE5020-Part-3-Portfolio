# Pre_Luxx Boutique — Website Project

## Project Title
Pre_Luxx Boutique Website — WEDE5020 Portfolio of Evidence (Part 1, Part 2 & Part 3 in progress)

## Student Information
- **Full Name:** [Maki Precious Tostetsi]
- **Student Number:** [ST10520801]
- **Group:** [ 03 ]
- **Module:** WEDE5020 — Web Development

## Project Overview
Pre_Luxx Boutique is a hypothetical retail store founded in 2016 by Nqobile
Tsotetsi, a fashion design graduate of the Cape Peninsula University of
Technology (CPUT) and former stylist. Located on Minner Street in Pretoria
Central, Pre_Luxx specialises in elegant, formal occasion wear — evening
gowns, tailored suits, bridesmaid dresses, and made-to-measure pieces for
weddings, matric dances, and galas.

This repository contains the Part 1 and Part 2 deliverables of the
WEDE5020 Portfolio of Evidence: the project proposal, researched content,
and the HTML/CSS/JS structure of the Pre_Luxx Boutique website, including
CSS styling and responsive design.

## Website Goals and Objectives
The website's primary goal is to let clients browse the collection and
book a fitting online before visiting in person — essential for a
boutique built around personalised, appointment-based service.

- Increase fitting and consultation bookings ahead of key seasons (matric
  dances, wedding season).
- Showcase the full collection with editorial-quality photography.
- Generate enquiries for made-to-measure and alteration services.

**Key Performance Indicators (KPIs):**
- Number of fitting/consultation bookings submitted per month.
- Average time spent browsing the collection pages.
- Newsletter sign-ups ahead of matric and wedding season.
- Growth in repeat visits during peak booking periods.

## Key Features and Functionality
- **Homepage** — hero section, "Book a Fitting" call to action, and a
  preview of the current collection.
- **About Us** — Nqobile Tsotetsi's story, the boutique's mission and
  vision, and the atelier team.
- **Collection (Products)** — categorised listings: Evening Gowns,
  Tailored Suits, Bridal & Wedding, and Accessories.
- **Enquiry** — a fitting/consultation booking form with an occasion
  selector, event date field, and made-to-measure request option.
- **Contact** — two locations (Minner Street boutique and Midrand
  showroom), embedded maps, and a general contact form.
- Responsive, mobile-first layout with a working navigation menu across
  all pages.
- Front-end form validation with success/error feedback (`js/main.js`).

## Timeline and Milestones
| Week | Milestone |
|------|-----------|
| 1–2  | Finalise sitemap, wireframes, and gather/organise researched content |
| 3–4  | Build HTML structure and content for all five pages |
| 5    | Apply CSS styling in line with the design and branding |
| 6    | Add JavaScript interactivity and conduct cross-browser testing |
| 7    | Final review, proofreading, and submission |

## Part 3 Details
This submission covers the **SEO stage** of **Part 3: Enhancing
Functionality and SEO**. (JavaScript interactivity, form upgrades with
AJAX, and deployment are tracked separately — see Known Outstanding
Issues.)

### Keyword research
Primary keywords targeted per page, based on the boutique's services and
location:
- Homepage: "formal wear Pretoria", "evening gowns Pretoria", "made-to-measure boutique"
- About: "boutique atelier Pretoria", "fashion stylist Pretoria"
- Collection: "evening gowns", "tailored suits Pretoria", "bridesmaid dresses South Africa"
- Enquiry: "book a fitting Pretoria", "custom formal wear"
- Contact: "boutique Minner Street Pretoria", "Midrand formal wear showroom"

### On-page SEO implemented
- **Title tags & meta descriptions**: unique, keyword-relevant copy per page (already in place from Part 1, reviewed and kept consistent for Part 3).
- **Header hierarchy**: every page has exactly one `<h1>`, with `<h2>`/`<h3>` used in logical, nested order — verified across all five pages.
- **Image optimisation**: descriptive alt text on every image describing its actual content (not generic "image" text); locally-stored files use descriptive filenames (e.g. `pre luxx.webp`, not `IMG_001.jpg`).
- **Clean URL structure**: flat, descriptive filenames (`index.html`, `about.html`, `products.html`, `enquiry.html`, `contact.html`) with no query strings or unnecessary nesting.
- **Internal linking**: every page links to every other page via the main nav and footer, plus contextual in-content links (e.g. "Read our full story," "Book a group fitting").
- **Mobile-friendliness**: already addressed in Part 2 (responsive breakpoints, mobile-first layout).
- **Canonical tags**: added to every page (`<link rel="canonical">`) to prevent duplicate-content issues.
- **robots meta tag**: `index, follow` added to every page.

### Off-page / social SEO
- **Open Graph and Twitter Card meta tags** added to every page, so links shared on social media (Facebook, Instagram, Pinterest, X) show a proper title, description, and image rather than a bare link.
- **Local SEO**: added `ClothingStore` structured data (JSON-LD, schema.org) to `contact.html`, including both locations, trading hours, and contact details — this is what allows search engines to show rich local-business results (e.g. in Google Maps / local pack results).

### Additional SEO requests
- **`robots.txt`** — added at the project root, allowing all crawlers and pointing to the sitemap.
- **`sitemap.xml`** — added at the project root, listing all five pages with priority and change-frequency hints.
- **Page speed**: added `loading="lazy"` to every below-the-fold image (16 images across the homepage, About Us, and Collection pages), so only the hero logo loads immediately; everything else loads as the user scrolls to it.
- **Security**: a `Referrer-Policy` meta tag is set on every page (browser-enforced). Stronger protections (`X-Content-Type-Options: nosniff`, `X-Frame-Options: DENY`, `Permissions-Policy`) can only be set as real HTTP response headers, so they are defined in a `_headers` file at the project root, which Netlify applies automatically on deployment. GitHub Pages does not support custom headers, so if deploying there these protections would not apply. (An earlier draft set `X-Content-Type-Options` via a `<meta>` tag; this was removed because browsers ignore it there.)

## Part 2 Details
This submission covers **Part 2: Designing the Visuals — CSS Styling and
Responsive Design**.

### CSS styling implemented
- **External stylesheet**: a single `css/style.css`, linked identically
  from all five pages.
- **CSS reset**: added at the top of the stylesheet so the site starts
  from a consistent baseline across browsers.
- **Base styles**: default font family (Jost for body, Cormorant
  Garamond for headings), font size, colour scheme (via CSS custom
  properties in `:root`), and consistent spacing.
- **Typography**: `font-family`, `font-size` (fluid via `clamp()`),
  `font-weight`, `line-height`, and `letter-spacing` applied throughout.
- **Layout structure**: CSS Grid and Flexbox used for the card grid,
  hero, split sections, footer, and form.
- **Visual styles and interactivity**: `color`, `background-color`,
  `border`, and `box-shadow` used for cards, buttons, and form fields;
  interactive states (`:hover`, `:focus-visible`, `:active`) added
  across navigation links, buttons, product cards, form fields, and
  location cards.

### Responsive design implemented
- **Breakpoints**: media queries at 900px, 820px, 760px, 720px, and
  620px, covering desktop, tablet, and mobile layouts.
- **Relative units**: layout spacing (padding, margin, gap, max-width)
  uses `rem` rather than fixed pixels.
- **Testing and iteration**: the site was tested at desktop (1440px),
  tablet (834px), and mobile (390px) widths using browser screenshots
  for every page (see Screenshot Evidence below). This testing process
  found and led to the fix of a hero-section bug where the image and
  text stayed side-by-side below 820px instead of stacking.

### Screenshot Evidence
Screenshots for every page at desktop, tablet, and mobile widths are
included in the `screenshots/` folder of this repository:

| Page | Desktop | Tablet | Mobile |
|------|---------|--------|--------|
| Homepage | `screenshots/index-desktop.png` | `screenshots/index-tablet.png` | `screenshots/index-mobile.png` |
| About Us | `screenshots/about-desktop.png` | `screenshots/about-tablet.png` | `screenshots/about-mobile.png` |
| Collection | `screenshots/products-desktop.png` | `screenshots/products-tablet.png` | `screenshots/products-mobile.png` |
| Book a Fitting | `screenshots/enquiry-desktop.png` | `screenshots/enquiry-tablet.png` | `screenshots/enquiry-mobile.png` |
| Contact | `screenshots/contact-desktop.png` | `screenshots/contact-tablet.png` | `screenshots/contact-mobile.png` |

Two additional screenshots document interactive states:
- `screenshots/card-hover.png` — product card hover state
- `screenshots/nav-open-mobile.png` — mobile navigation menu open

## Known Outstanding Issues
Being tracked honestly here rather than hidden, for transparency with
the marker:

- **Responsive images (`srcset`/`sizes`) are not yet implemented** on
  the real photography — this was present when placeholder images were
  used, but was not carried over when real images were added.
- The homepage hero currently displays the boutique's logo graphic
  rather than a photograph; this works visually but may be worth
  revisiting with a real atelier/product photo.
- **Part 3 is partially complete.** SEO (this section) is done.
  Still outstanding: JavaScript interactive features (gallery/lightbox,
  content filtering), form upgrades (AJAX submission, richer
  validation), and deployment to a live host (Netlify/GitHub Pages).
- `og:image` and the JSON-LD `image` field point to
  `images/hero/pre-luxx-boutique-social-share.jpg`, which does not yet
  exist — a proper 1200×630px social-share image should be created and
  added before relying on social link previews.
- The domain `www.preluxxboutique.co.za` used throughout the canonical
  tags, Open Graph tags, and sitemap is a placeholder — update
  site-wide once a real domain or deployed hosting URL is known.


## Folder Structure
```
pre_luxx-boutique/
├── index.html
├── about.html
├── products.html
├── enquiry.html
├── contact.html
├── robots.txt
├── sitemap.xml
├── _headers
├── css/
│   └── style.css
├── js/
│   └── main.js
├── images/
│   ├── hero/
│   └── products/
├── screenshots/
│   ├── index-desktop.png / index-tablet.png / index-mobile.png
│   ├── about-desktop.png / about-tablet.png / about-mobile.png
│   ├── products-desktop.png / products-tablet.png / products-mobile.png
│   ├── enquiry-desktop.png / enquiry-tablet.png / enquiry-mobile.png
│   ├── contact-desktop.png / contact-tablet.png / contact-mobile.png
│   ├── card-hover.png
│   └── nav-open-mobile.png
└── README.md
```

## Sitemap
```
                    Pre_Luxx Boutique
                    Homepage – index.html
                            │
        ┌───────────┬───────────┬───────────┐
        │            │            │            │
   About Us      Collection    Enquiry      Contact
  about.html   products.html  enquiry.html  contact.html
```
All four pages are reachable from the homepage via the main navigation
menu, and link back to each other consistently across the site.

## Changelog
| Date | Change |
|------|--------|
| [09/08/2026] | Initial project proposal drafted and submitted for approval |
| [09/08/2026] | Retail Store approved as target organisation category |
| [09/08/2026] | Sitemap and folder structure finalised |
| [09/08/2026] | Initial HTML structure built for all five pages (as Aurelle Boutique) |
| [10/08/2026] | CSS styling applied (colour scheme, typography, layout) |
| [11/08/2026] | JavaScript added (navigation toggle, form validation) |
| [14/09/2026] | **Part 2**: CSS reset added for cross-browser consistency |
| [14/09/2026] | **Part 2**: Interactive states audited and expanded (hover, focus, active) across nav, buttons, cards, and forms |
| [15/09/2026] | **Part 2**: Layout spacing converted from px to rem throughout the stylesheet |
| [15/09/2026] | **Part 2**: Bug fix — hero section had no breakpoint below 820px, causing the image/text to stay side-by-side on tablet and mobile instead of stacking; added missing media query |
| [16/09/2026] | Organisation rebranded from Aurelle Boutique to Pre_Luxx Boutique (Pretoria) |
| [16/09/2026] | Real photography added to replace placeholder images across all pages |
| [16/09/2026] | **Bug fix**: corrected broken/duplicated Google Maps iframe markup on the Contact page that was rendering visible garbled text |
| [16/09/2026] | Captured and added screenshot evidence for all five pages at desktop, tablet, and mobile widths, plus hover and mobile-nav states |
| [16/09/2026] | Identified four product images sourced from iStock/Getty without a licence; flagged in README for replacement before final submission |
| [26/10/2026] | **Part 3 (SEO)**: added canonical tags, `robots` meta tag, Open Graph and Twitter Card meta tags to all five pages |
| [26/10/2026] | **Part 3 (SEO)**: added `ClothingStore` JSON-LD structured data to the Contact page for local SEO (both locations, hours, contact details) |
| [27/10/2026] | **Part 3 (SEO)**: added `robots.txt` and `sitemap.xml` at the project root |
| [27/10/2026] | **Part 3 (SEO)**: added `loading="lazy"` to 16 below-the-fold images across the homepage, About Us, and Collection pages for page-speed improvement |
| [30/10/2026] | **Part 3 (SEO)**: added a `Referrer-Policy` meta tag to all pages, and a `_headrs` file (Netlify) for real HTTP security headers |
| [01/11/2026] | README updated with Part 3 SEO section, keyword research notes, changelog entries, and outstanding items for the remainder of Part 3 |

## References
- Baymard Institute (2024) *E-commerce UX best practices for fashion
  retail*. Available at: https://baymard.com (Accessed: 9 August 2026).
- Google (2023) *Think with Google: Mobile-first design principles*.
  Available at: https://www.thinkwithgoogle.com (Accessed: 9 August 2026).
- Western Cape Government (2023) *Small business support and resources*.
  Available at: https://www.westerncape.gov.za (Accessed: 9 August 2026).
- Google Fonts (2026) *Cormorant Garamond* and *Jost*. Available at:
  https://fonts.google.com (Accessed: 9 August 2026).
- Josh W. Comeau (2023) *A Modern CSS Reset*. Available at:
  https://www.joshwcomeau.com/css/custom-css-reset/ (Accessed: 16
  September 2026).
- MDN Web Docs (2024) *Using media queries*. Available at:
  https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries
  (Accessed: 16 September 2026).
- Ghareeb, K. (n.d.) *Woman in black dress* [Photograph]. Unsplash.
  Available at: https://unsplash.com/photos/woman-in-black-dress-QN507MdnxRQ
  (Accessed: 17 September 2026). Used for "The Noir Gown."
- Bellis, T. (n.d.) *Woman in white sleeveless dress standing on gray
  concrete floor during daytime* [Photograph]. Unsplash. Available at:
  https://unsplash.com/photos/woman-in-white-sleeveless-dress-standing-on-gray-concrete-floor-during-daytime-X2qRKqLKtg4
  (Accessed: 17 September 2026). Used for "The Aria Gown."
- Meilhac, H. (n.d.) *Woman wearing pink dress standing next to white
  wall* [Photograph]. Unsplash. Available at:
  https://unsplash.com/photos/woman-wearing-pink-dress-standing-next-to-white-wall-jJ0tLs2ROd4
  (Accessed: 17 September 2026). Used for bridesmaid/wedding wear.
- PRAHANT STUDIO (n.d.) *A bunch of jewelry sitting on top of a table*
  [Photograph]. Unsplash. Available at:
  https://unsplash.com/photos/a-bunch-of-jewelry-sitting-on-top-of-a-table-hVPCnpu1GSs
  (Accessed: 17 September 2026). Used for formal accessories.
- *Note: all Unsplash photographs used under the Unsplash License —
  free for commercial use, no attribution legally required, though
  credited here as good academic practice. Remaining product photos
  (suits, gowns, team portraits) are original/sourced separately and
  do not carry Getty/iStock restrictions, per licensing metadata review
  conducted 17 September 2026.*


