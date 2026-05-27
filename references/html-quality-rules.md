# HTML Quality Rules

## Required Standards

- Single HTML file — CSS and simple JS included inside
- Mobile-first responsive design
- Free web font for the chosen language (see `fonts-and-design.md`)
- No heavy external libraries (no Bootstrap, no jQuery)
- Image positions clearly marked with descriptive placeholders
- Section comments in plain language so the user can find and edit each part
- Button text is clear and action-oriented
- Simple enough structure to paste into Cafe24, Smart Store, or Shopify

---

## Section Comments

Add a comment before every section so non-technical users can find what they need.

```html
<!-- ===== HERO SECTION: Main product image and headline ===== -->
<!-- ===== BENEFITS SECTION: Key product advantages ===== -->
<!-- ===== USAGE SCENE SECTION: Product in real life ===== -->
<!-- ===== TRUST SECTION: Patents, certifications, awards ===== -->
<!-- ===== FAQ SECTION: Common questions ===== -->
<!-- ===== CTA SECTION: Buy or inquiry button ===== -->
```

---

## Image Placeholder Convention

Use descriptive file names, not `image1.jpg` or `img.png`.

Examples:
- `product-main.jpg` — main product photo
- `product-angle-2.jpg` — secondary angle
- `product-in-use.jpg` — lifestyle / usage scene
- `patent-certificate.jpg` — patent document image
- `certification-logo.png` — certification badge
- `company-logo.png` — company logo
- `review-screenshot.jpg` — customer review
- `before-after.jpg` — comparison image

Add an `alt` attribute in plain language:
```html
<img src="product-main.jpg" alt="Main product photo — replace with your file">
```

---

## Section Selection Rules

Do not include every possible section. Choose sections that fit the product and brand.

**Always include:**
- Hero section (product visible immediately on first screen)
- At least one benefits or features section
- A buy or inquiry button

**Include if relevant:**
- Usage scenes (especially for lifestyle or B2C products)
- Problem and solution (good for products that solve a specific pain point)
- Specifications (for technical or B2B products)
- Patents, certifications, awards (only if the user provided these)
- Reviews / trust elements (only if the user provided real content)
- FAQ (include 2-3 questions if the product is complex or niche)

**Never include by default:**
- Fake reviews or placeholder testimonials
- Invented sales numbers ("Over 10,000 sold!")
- Price sections unless the user provided a price

---

## Mobile-First CSS Pattern

Write styles for mobile first, then add `@media (min-width: 768px)` for desktop.

```css
/* Mobile default */
.section { padding: 40px 20px; }

/* Desktop override */
@media (min-width: 768px) {
  .section { padding: 80px 60px; }
}
```

---

## What to Avoid

- Copying website copy verbatim
- Pasting in heavy frameworks
- Making nested code structures that are hard to edit
- Generating placeholder review text ("This product changed my life!")
- Using inline styles excessively — use a `<style>` block instead
- Making it platform-specific (avoid Shopify Liquid syntax, Cafe24 tags, etc.)
