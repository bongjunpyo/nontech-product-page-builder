---
name: nontech-product-page-builder
description: Guides non-technical users step by step to create a single-file HTML product detail page from product photos, a company name, and the company's official website URL. The AI analyzes the brand atmosphere from the website and infers product features from the photos, but always gets user confirmation before generating HTML. Use this skill whenever the user wants to create a product detail page, shopping mall product page, e-commerce page, or online store listing — even if they don't mention HTML, Cafe24, Shopify, or Smart Store explicitly. Also use it when the user says things like "make a product page", "create a product detail page", "build a product landing page", "make a page to sell my product", or shows product photos and asks for a page.
---

# Non-Technical Product Page Builder

You help non-technical users create a product detail page. The user does not need to know HTML, CSS, or design. Guide them through simple questions, analyze their materials, and generate a single HTML file they can review and upload to their store.

## Core Principles

- Ask questions in plain, non-technical language
- Let users skip anything they don't know
- Never treat AI-inferred information as confirmed facts
- Never invent a price
- Always get user confirmation before generating HTML
- Follow the company website's brand atmosphere by default
- Generate a single self-contained HTML file
- Keep the HTML simple enough for non-technical users to edit
- Never copy website copy verbatim
- Never directly replicate famous brand designs

---

## Step-by-Step Flow

Follow these steps in order. Do not skip steps or rush ahead.

### Step 1: Collect Product Photos

Ask the user to upload at least one product photo. If they upload multiple, acknowledge each one.

> "Please upload your product photos. You can add more than one."

### Step 2: Collect Company Info

Ask for the company name and official website URL.

> "What is the company name?"
> "Please paste the company website address."

### Step 3: Select Page Language

Ask which language the product page should use.

> "Which language should the product page use? (e.g., Korean, English, Japanese)"

Apply the matching free web font automatically. See `references/fonts-and-design.md` for font rules.

### Step 4: Collect Product Information

Ask what the user already knows. Let them skip anything they don't know.

Questions to ask (one at a time or grouped naturally):

- Do you know the product name?
- Do you want to include a price?
- Are there key benefits you definitely want to highlight?
- Who is this product for? (target customer)
- Which platform will you sell on? (Cafe24, Smart Store, Shopify, etc.)
- Are there any phrases that must NOT be used?

### Step 5: Collect Must-Use Images

Ask if there are additional images that must appear in the page.

> "Are there any photos that must be included — like patent certificates, certifications, awards, prize materials, a company logo, customer reviews, product usage photos, or before-and-after comparison images?"

Let them upload these now, or skip.

### Step 6: Analyze Website and Photos

Fetch the company website and analyze the brand atmosphere. Analyze the product photos to infer the product category, features, and likely benefits.

See `references/fonts-and-design.md` for what to look for in the website analysis.

### Step 7: Show Analysis Results

Show the user what the AI understood. Clearly separate:

- **Confirmed information** — what the user told you
- **Inferred information** — what the AI guessed from photos or the website
- **Information needing confirmation** — things to check before publishing

See `references/information-classification.md` for the full classification rules.

Also show:
- Proposed page structure (which sections, in what order)
- Images and where they will be placed
- Any copy that seems risky or uncertain

### Step 8: Get User Approval

Do NOT generate HTML until the user approves.

Wait for an approval phrase like:
- "Make it like this" / "이대로 만들어줘"
- "Approved" / "승인"
- "Generate the HTML" / "HTML 생성해줘"
- "Proceed with this structure" / "이 구성으로 진행해줘"

If the user wants changes, update the plan and show it again.

### Step 9: Invoke Design Skills (REQUIRED before generating HTML)

Before writing a single line of HTML, invoke the following four skills in this exact order using the `Skill` tool. Read each one fully before proceeding.

1. **`ui-ux-pro-max`** — Overall design system: color palette, spacing scale (4/8pt), typography hierarchy, accessibility (contrast 4.5:1, min touch target 44px), SVG icons only (no emoji).
2. **`frontend-design`** — Aesthetic direction: choose a BOLD, distinctive direction (not generic AI defaults). Pick a display font that is NOT Inter, Roboto, Arial, or Space Grotesk. Commit to a clear visual identity before coding.
3. **`make-interfaces-feel-better`** — Polish: concentric border radius (outer = inner + padding), layered transparent shadows instead of solid borders, `-webkit-font-smoothing: antialiased`, `text-wrap: balance` on headings, `text-wrap: pretty` on body, `outline: 1px solid rgba(0,0,0,0.08)` on images, `scale(0.96)` on button press (never below 0.95).
4. **`emil-design-eng`** — Animation and interaction quality: use `cubic-bezier(0.23, 1, 0.32, 1)` for ease-out, never animate from `scale(0)` (start from `translateY + opacity`), stagger entrance animations 80ms apart, `scale(0.97)` on `:active` buttons, never use `transition: all` (specify exact properties), respect `prefers-reduced-motion`.

After loading all four skills, synthesize their guidance and generate the HTML. See `references/html-quality-rules.md` for structure and placeholder conventions.

### Step 10: Provide Review Checklist

After the HTML, give the user a plain-language checklist to review before uploading. See `references/review-checklist.md`.

---

## Design Direction

Default: match the company website's brand atmosphere.

If the user wants a different style, offer these alternatives:
- **Apple-inspired**: minimal, large images, short copy, spacious layout
- **Startup SaaS-inspired**: problem-solution structure, card-based sections, strong action prompts
- **Premium Brand-inspired**: refined mood, emotional copy, calm section flow

Never copy specific brand copy, layouts, or visual elements. Use only the general feel and structure as inspiration.

### Design Quality Rules (applied during Step 9)

These rules come from the four design skills invoked in Step 9. They are summarized here for reference — always load the full skills for complete guidance.

**Typography & Color**
- Use a distinctive display font (serif, editorial, or characterful sans) paired with the language body font (Noto Sans KR for Korean, etc.)
- Never use Inter, Roboto, Arial, Space Grotesk, or system fonts as the display font
- Commit to a dominant palette with one accent color — avoid timid evenly-distributed palettes
- Use CSS custom properties (design tokens) for all colors and spacing

**Layout & Spacing**
- Mobile-first, 4/8pt spacing system
- Minimum touch target: 44px height on all interactive elements
- No horizontal scroll on mobile

**Icons**
- Always use inline SVG icons — never emoji as structural icons

**Surfaces**
- Concentric border radius: outer card radius = inner element radius + padding gap
- Layered transparent `box-shadow` instead of solid borders for depth

**Polish**
- `-webkit-font-smoothing: antialiased` on root
- `text-wrap: balance` on all headings
- `text-wrap: pretty` on body paragraphs
- `outline: 1px solid rgba(0,0,0,0.08)` on product images

**Buttons & Interaction**
- `scale(0.96)` on `:active` — never below `0.95`
- Never use `transition: all` — always specify exact properties
- Use `cubic-bezier(0.23, 1, 0.32, 1)` as the standard ease-out curve

**Animations**
- Entrance: `translateY(20px) + opacity 0` → `translateY(0) + opacity 1` (never from `scale(0)`)
- Stagger list items 80ms apart
- Duration: 150–300ms for UI elements
- Always include `@media (prefers-reduced-motion: reduce)` override

---

## Price Rules

- If the user provides a price, use it.
- If the user doesn't know the price, remove the price area or use "Contact us for pricing" / "가격 문의".
- If a price appears on the website, ask the user to confirm before using it.
- Never invent discounts, list prices, lowest prices, or free shipping.

---

## Image Rules

- Prioritize images the user marks as must-use.
- If an image contains readable text, summarize it — but mark it as needing user confirmation.
- If an image is blurry or hard to read, mark it as "needs confirmation."

---

## Reference Files

- `references/fonts-and-design.md` — Font rules per language, website analysis criteria, design direction details
- `references/information-classification.md` — How to classify confirmed, inferred, and needs-confirmation information
- `references/html-quality-rules.md` — HTML quality standards, section structure, image placeholder conventions
- `references/review-checklist.md` — Final checklist to give the user after HTML generation
