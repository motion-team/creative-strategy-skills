---
name: brand-intake
description: Runs a structured brand intake interview and then conducts web research to build a comprehensive brand context document. Use this whenever the user says they're working on a new client, wants to build brand context, or says "run brand intake", "conduct brand research" or "build brand context for [brand]". Also trigger when the user starts a creative strategy workflow for a brand that doesn't yet have a context document in the project. This must run BEFORE any Creative Strategy Engine, Hook Writing, or other execution work — it is the prerequisite context layer for all downstream creative strategy.
---

# Brand Intake

This does two things in sequence:
1. **Interviews** the user to collect essential seed information about the brand
2. **Researches** the brand using that information to build a comprehensive brand context document

The output is a structured markdown file (`brand-context.md`) that all downstream modules — Creative Strategy Engine, Hook Writing, Creative Mechanics — can reference as the foundational context layer.

---

## PHASE 1: INTAKE INTERVIEW

Before researching anything, ask the user the following questions. Ask them **all at once** in a single message — do not drip them one by one. Group them clearly so the user can answer quickly.

### Questions to Ask

**Brand basics:**
1. What's the brand name?
2. What's the brand website URL?
2. What product(s) are you running paid ads for? If multiple, list them. If all, say "all".
3. Is there a specific product or product line you want this context document to focus on, or should it cover the full brand?

**What you already know:**
4. What do you know about this brand and its audience that is important to use in your workflow? (e.g. Age, gender, lifestyle, pain points, values.)
5. Do you know who their main competitors are?
6. Are there any brand constraints you're already aware of? (e.g., can't make health claims, family-friendly tone, sensitive topic, regulated category)

**Creative context:**
7. Do you have any existing creative or messaging you've already seen from this brand that you want to keep in mind?

---

### After the User Answers

Once you have their answers, confirm before proceeding:

> "Got it — I'll use this as my starting point and go research the rest. I'll come back with a full brand context doc. Give me a moment."

Then proceed to Phase 2.

---

## PHASE 2: RESEARCH

Using the brand name and URL provided, conduct web research to fill out the full brand context document. Use the `web_search` and `web_fetch` tools.

### Research Checklist

Work through each of these areas. For each one, gather what you can from the brand's website, ad library, reviews, press, and competitor sites.

#### 1. Brand Story & Origin
- How did the brand start? What problem did the founder set out to solve?
- Is there a founder story or mission that drives the brand's identity?
- How long have they been around? Are they a startup, scaling, or established?

**Research approach:** Fetch the About page. Search "[brand name] founder story" and "[brand name] how it started."

#### 2. Full Product Catalog
- What products do they sell?
- What are the key SKUs or product lines?
- How are products differentiated from each other (size, use case, formulation, audience)?
- What is the hero product or primary revenue driver (if identifiable)?
- Does the brand offer any bundles?

**Research approach:** Fetch the product/shop pages. Look at site navigation.

#### 3. Product Differentiation & Unique Mechanism
- What makes their product(s) different from alternatives?
- Is there a proprietary ingredient, format, technology, or method?
- How do they explain their point of difference on their website?
- What claims do they make and how do they support them?

**Research approach:** Fetch product detail pages and any "How it works" or FAQ pages. Look for any clinical claims, certifications, or patent language.

#### 4. Competitors
- Who are the 3–5 closest competitors?
- How do competitors position themselves vs. this brand?
- What does this brand do that competitors don't (or vice versa)?

**Research approach:** Search "[brand name] vs [competitor]", "[product category] alternatives", and "[brand name] competitors." Also check if the brand calls out competitors directly in their messaging.

#### 5. The Alternative Solution
- What was the customer doing BEFORE this product existed?
- What is the "old way" this product replaces or improves upon?
- This is not always a direct competitor — sometimes it's a behavior, DIY approach, or doing nothing.

**Research approach:** Look at reviews, the brand's own problem-framing language, and any "vs. traditional methods" content.

#### 6. Core Audience(s)
- Who is the primary audience this brand speaks to on their website and in ads?
- Are there distinct secondary audiences?
- What signals point to who they're targeting? (Imagery, language, pain points surfaced, price point, lifestyle cues)
- Combine what the user told you in Phase 1 with what you find in research.

**Research approach:** Analyze homepage copy, ad creative (Meta Ad Library if accessible), product page language, and review language.

#### 7. Brand Voice & Tone
- How does this brand communicate? (Clinical? Warm? Witty? Direct? Community-driven?)
- What adjectives describe their copy style?
- Are there notable patterns — vocabulary they use, things they avoid, emotional register?
- Does voice shift between product types or audiences?

**Research approach:** Read website copy closely. Look for patterns in headlines, CTAs, email popups, FAQ answers.

#### 8. Inferred Creative Constraints
Based on everything you've found, identify likely constraints that would affect ad creative. Think about:
- Category sensitivities (health claims, before/after restrictions, regulated ingredients)
- Audience constraints (if audience includes older demographics, religious communities, parents, etc.)
- Platform norms (if brand is in a category with known Meta/TikTok ad restrictions)
- Tone constraints (brands that are buttoned-up, family-safe, or community-led often have limits on edginess or provocation)
- Price point constraints (high-AOV brands often can't do price-shock tactics; budget brands can't lean on premium positioning)

Label each constraint as **confirmed** (explicitly stated somewhere) or **inferred** (reasonable assumption based on category/signals).

#### 9. Must-Know Strategic Context
Anything else that a creative strategist needs to know before writing a single hook. This might include:
- Unusual purchase behavior (subscription vs. one-time, bundle-heavy, etc.)
- Seasonal relevance
- Strong community or UGC presence
- Noteworthy press or cultural moments
- Anything the user flagged in Phase 1 that needs to be incorporated

---

## PHASE 3: BUILD THE CONTEXT DOCUMENT

Once research is complete, compile everything into a structured markdown document.

### Output Format

```markdown
# Brand Context: [Brand Name]
*Generated: [Date] | Focus: [Product/Product Line or "Full Brand"]*

---

## Brand Overview
[2–3 sentence summary of who this brand is, what they sell, and where they sit in the market.]

---

## Brand Story & Origin
[Founder story, mission, origin. Keep it factual and concise.]

---

## Product Catalog
[List of products with brief descriptions. Flag the hero product if identifiable.]

| Product | Key Differentiator | Audience |
|---|---|---|
| ... | ... | ... |

---

## What Makes Them Different
[Unique mechanism, proprietary ingredient, format advantage, or positioning edge. Quote their own language where possible.]

---

## Competitor Landscape
[3–5 competitors, how each positions, and how this brand contrasts.]

| Competitor | Their Positioning | How This Brand Differs |
|---|---|---|
| ... | ... | ... |

---

## The Alternative Solution
[What the customer was doing before this product. The "old way."]

---

## Core Audience(s)
**Primary:** [Description]
**Secondary (if applicable):** [Description]

Key signals: [Pain points, lifestyle, language patterns, what they care about]

---

## Brand Voice & Tone
[Adjectives. Patterns. Examples of actual copy that demonstrate the voice. What they avoid.]

---

## Creative Constraints
| Constraint | Type | Notes |
|---|---|---|
| ... | Confirmed / Inferred | ... |

---

## Must-Know Strategic Context
[Anything else a creative strategist must know before writing creative. Bullets OK here.]

---

## Research Notes
*Sources consulted: [list URLs fetched]*
*Gaps / low-confidence areas: [anything you couldn't verify — flag it clearly so the user can fill in or correct]*
```

---

## PHASE 4: DELIVER & CONFIRM

After building the document:

1. **Save** it as `brand-context-[brandname].md`
2. **Present** it to the user using `present_files`
3. **Flag gaps** — call out anything you couldn't verify or are inferring vs. confirming
4. **Ask one closing question:**

> "Does anything here look off, or is there anything important I'm missing? Once you confirm, this becomes the working context for all creative strategy on this brand."

After confirmation, this document should be referenced by all downstream modules (Creative Strategy Engine, Hook Writing, Creative Mechanics) for this brand.

---

## Notes for Downstream Handoff

When handing off to the Creative Strategy Engine or Hook Writing, reference the brand context doc explicitly:

> "Using `brand-context-[brandname].md` as the foundation — the audience, differentiation, constraints, and voice are all defined there."

This prevents downstream modules from making assumptions that conflict with the established brand context.
