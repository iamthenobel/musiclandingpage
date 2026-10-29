# HASHEE Promo Recreation — Implementation Plan

## Product scope
A single-page responsive React/TypeScript recreation of `https://dittomusic.com/en/promo`, with the original Ditto branding replaced by HASHEE and the identifier `#@$#££`. The page keeps the reference's long-form landing-page sequence: cookie notice, sticky navigation, hero, feature marquee, benefits grid, package cards, process section, testimonials, advice carousel, FAQ accordion, editorial content, final CTA, and footer.

## Design direction
The reference establishes the visual system: maximalist indie-music campaign energy, high-contrast hot pink and near-black surfaces, acid-green details, pale blush cards, condensed all-caps display typography, oversized headings, rounded image panels, and playful sticker-like pills.

### Core principles
- Loud, editorial, and music-first rather than corporate.
- Strong contrast with hot-pink canvas sections against deep ink content bands.
- Information arranged as a sequence of bold cards, marquees, and oversized typographic moments.
- Motion is tactile but restrained: marquee drift, hover lift, reveal-on-scroll, and accordion expansion.

### Typography system
Use `Barlow Condensed` for display headlines and labels, with `DM Sans` for body copy. Headlines are heavy, uppercase, tightly tracked, and responsive with `clamp()` sizing. Body copy stays readable at 16–18px with generous line-height.

### Brand treatment
HASHEE appears as a compact white wordmark with a lime `#@$#££` identifier tucked into the lockup. The mark sits where the reference places Ditto's white logo and uses a hand-built inline SVG-like text treatment rather than leaving original branding in the UI.

## Technical structure
- `index.html`: Vite entry document and font preconnects.
- `src/main.tsx`: React page, reusable components, interaction state, and semantic content.
- `src/styles.css`: centralized tokens, responsive layout, keyframes, reduced-motion support.
- `public/manus-routes.json`: route manifest for `/`.
- `app.config.ts`: project logo metadata.
- `TODO.md`: acceptance outcomes and progress.

The implementation is static-only: no server or database is needed. External behavior that would require Ditto's account system is represented by safe anchor links and simulated inline form feedback, without claiming a real transaction.

## Reference notes captured
- Desktop hero is a hot-pink field with a dark top nav, large black/white condensed headline, white outlined CTA, and a cutout musician image on the right.
- A dark horizontal feature ticker separates hero from the pink benefits section.
- Benefits use a 2-column desktop card grid with rounded pale-pink surfaces and collage-style imagery.
- Packages are presented as two contrasting rounded cards, with Promo Plus visually emphasized in lime/black.
- Process content shifts to an ink section with a diagram-like step rail and four editorial explanations.
- Testimonials are a horizontal pink-card carousel; advice is a dark editorial list with arrows.
- FAQ uses native disclosure-style rows; lower editorial copy is dark ink with lime underlined links.
- Footer is near-black with three link columns and a centered pink/lime CTA capsule.

## Validation approach
Run TypeScript/CSS diagnostics, start the Vite server on port 3000, verify `/manus-routes.json`, capture desktop/tablet/mobile screenshots with Webdev, then refine the most visible spacing and responsive issues before checkpointing.
