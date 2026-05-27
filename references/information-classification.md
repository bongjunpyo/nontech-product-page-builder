# Information Classification Reference

Before showing the analysis results to the user, classify every piece of information into one of three groups.

---

## Confirmed Information

Information the user directly provided. Present this without any qualification.

Examples:
- Product name the user typed
- Price the user entered
- Official specifications the user shared
- Phrases the user said not to use
- Images the user said must be included

---

## Inferred Information

Information the AI guessed from the product photos, website, or context. Always label it clearly as inferred. Never present inferred information as fact.

Examples:
- Product category (e.g., "This looks like a skincare product")
- Likely use situations (e.g., "Appears suitable for outdoor use")
- Likely benefits (e.g., "May appeal to users who value portability")
- Brand atmosphere (e.g., "The website feels modern and minimal")
- Page structure direction (e.g., "A problem-solution layout may work well here")

When showing inferred information to the user, use softening language:
- "This appears to be..."
- "Based on the photos, this might be..."
- "The website gives the impression of..."
- "I'm guessing this could appeal to..."

---

## Information Needing Confirmation

Information that could be wrong, legally sensitive, or financially significant. These must be checked by the user before appearing in a published sales page.

Examples:
- Exact product specifications (dimensions, weight, capacity)
- Price (especially if found on the website — ask the user to confirm)
- Certification status and certificate numbers
- Patent name and patent number
- Award name and the awarding organization
- Performance numbers or test results
- Country of origin
- Materials and ingredients
- Shipping conditions
- Exchange and return policy

When showing this group, be explicit:
> "These need your confirmation before I can include them in the page."

---

## How to Present the Three Groups

Show all three groups clearly in the confirmation step, before generating HTML.

Suggested format:

```
✅ Confirmed information (provided by you)
- [list items]

🔍 Inferred information (AI's best guess — please check)
- [list items]

⚠️ Needs confirmation before publishing
- [list items]
```

The user should be able to look at this and quickly understand what is safe to use and what still needs their attention.
