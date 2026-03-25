---
name: review-audit
description: 'Analyzes positive customer reviews to surface deep customer insights for ad copy. Use this whenever a user provides customer reviews and wants to understand their customers better, extract VOC (voice of customer), find ad-ready language, or build messaging strategy from real customer language. Trigger for any request involving "analyze these reviews," "what are customers saying," "find insights in these reviews," "VOC analysis," or any variation of wanting to mine customer reviews for creative strategy inputs. Output is always organized by product (if multiple), and surfaces five buckets of insight: pain points, trigger moments, objections, transformations, and standout language.'
---

# Review Audit

This system mines positive customer reviews to extract the insights that make ad copy actually work — the real language, real pain, real moments, and real transformations that customers experienced. The output feeds directly into creative strategy and hook writing.

**The goal is not to summarize reviews. The goal is to find the raw material for ads.**

---

## What You Need Before Starting

Reviews can be provided in any format:
- Pasted directly into the chat
- CSV or spreadsheet upload
- Copy/pasted from a document

If multiple products are present in the review set, identify them before beginning. All output is separated by product.

If the format is unclear or product attribution is ambiguous, ask before proceeding.

---

## Step 1: Group by Product

If the brand sells multiple products, sort all reviews by product first. Every subsequent step runs separately per product.

If all reviews are for a single product, skip grouping and proceed.

---

## Step 2: Score Review Quality (1–5)

Before analysis, score every review for quality. This determines what gets analyzed and what gets discarded.

| Score | What it looks like |
|---|---|
| **1** | Garbage — gibberish, swear words, 2–3 meaningless words, zero signal ("great product", "love it", "👍") |
| **2** | Low signal — very short, vague, no specific detail or emotion |
| **3** | Moderate — mentions the product, some specificity, but no vivid detail or emotional depth |
| **4** | High quality — specific, describes a real experience, references a before/after or a feeling |
| **5** | Gold — long, emotional, vivid, paragraph-level detail; the customer was so moved they wrote an essay about it |

**Score 5 reviews are the priority.** They contain the most usable language and the deepest insight.

---

## Step 3: Filter

Discard all reviews scored **1**. Do not include them in analysis.

Analyze scores **2–5**, with emphasis on 4s and 5s. Low-scoring reviews (2–3) can contribute to pattern identification but should not be the source of pulled quotes.

---

## Step 4: Extract Insights by Bucket

Run this analysis separately for each product. Within each bucket, group similar insights together and write a brief summary of the pattern. Then pull the best word-for-word quotes that exemplify it.

Do not editorialize the quotes. Pull them exactly as written.

---

### Bucket 1: Pain Points
*What problem were they experiencing before they found this product?*

Look for: descriptions of the problem they had, how long they'd had it, what they'd tried before, how it affected their life, the emotional weight of living with it.

For each pain theme identified:
- Name the theme
- Write a 2–3 sentence summary of the pattern across reviews
- Flag the strongest quotes for the swipe file

---

### Bucket 2: Trigger Moments
*What finally made them buy?*

Look for: the specific moment, event, or realization that pushed them over the edge. This is the thing that turned a maybe into an add-to-cart. It could be a life event (wedding, diagnosis, vacation), a recommendation (friend, doctor, TikTok), hitting a breaking point, or running out of patience with other solutions.

For each trigger theme identified:
- Name the theme
- Write a 2–3 sentence summary of the pattern
- Flag the strongest quotes for the swipe file

---

### Bucket 3: Objections Before Purchasing
*What almost stopped them from buying?*

Look for: skepticism they mention having had, comparisons to other products they'd tried, price hesitation, disbelief that this would actually work, fear of wasting money again.

Note: In positive reviews, objections are almost always mentioned in past tense — "I was skeptical but..." or "I almost didn't try it because..." These are gold for objection-handling ad copy.

For each objection theme identified:
- Name the theme
- Write a 2–3 sentence summary of the pattern
- Flag the strongest quotes for the swipe file

---

### Bucket 4: Transformations
*What changed for them after using the product?*

Look for: the specific result they experienced, how their life is different now, the emotional shift (confidence, relief, freedom, pride), and — most importantly — how they describe the transformation in their own words. The more specific and visceral, the better.

For each transformation theme identified:
- Name the theme
- Write a 2–3 sentence summary of the pattern
- Flag the strongest quotes for the swipe file

---

### Bucket 5: Standout Language & Ad-Ready Phrases
*Exact language worth stealing for ads.*

This bucket is different from the others. It is not organized by theme — it is a curated collection of the most vivid, emotionally charged, specific, and scroll-stopping phrases pulled from across all buckets. These are the lines that made you stop while reading. The ones that don't need to be rewritten. The ones a copywriter would highlight and build an ad around.

Pull these verbatim. Note which product they're from.

What to look for:
- Unusually specific descriptions of pain or transformation
- Phrases that capture an emotion in a way you couldn't have written yourself
- Before/after language that is visceral and concrete
- Lines that could work as a hook with zero editing
- Anything that made you feel something while reading it

---

## Output Format

Produce a separate full output for each product. Structure:

```
─────────────────────────────────────
PRODUCT: [Product Name]
Reviews analyzed: [X] | Discarded (score 1): [X]
─────────────────────────────────────

BUCKET 1: PAIN POINTS

[Theme Name]
Summary: [2–3 sentences on the pattern]

[Theme Name]
Summary: [2–3 sentences on the pattern]

---

BUCKET 2: TRIGGER MOMENTS

[Theme Name]
Summary: [2–3 sentences on the pattern]

---

BUCKET 3: OBJECTIONS BEFORE PURCHASING

[Theme Name]
Summary: [2–3 sentences on the pattern]

---

BUCKET 4: TRANSFORMATIONS

[Theme Name]
Summary: [2–3 sentences on the pattern]

---

BUCKET 5: STANDOUT LANGUAGE & AD-READY PHRASES

"[Exact quote]"
"[Exact quote]"
"[Exact quote]"
[etc.]

─────────────────────────────────────
```

All word-for-word quotes are collected in Bucket 5. Do not scatter quotes throughout buckets 1–4 — keep the summaries clean and let the swipe file be the dedicated place for raw language.

---

## How This Feeds the Rest of the Stack

The output of this analysis plugs directly into creative strategy and execution:

- **Pain Points → Creative Strategy Engine** — pain buckets map directly to the pain/desire anchor layer
- **Trigger Moments → Hook Writing** — trigger moments are often the most powerful hook material; they capture the exact moment of emotional readiness
- **Objections → Hook Writing / Creative Mechanics** — objections inform Borrowed Enemy, Reframe, and Risk Reversal mechanics and hook tactics
- **Transformations → Hook Writing** — transformation language feeds aspirational and social proof hooks
- **Standout Language → Hook Voice Patterns** — the best phrases can be added directly to the swipe file as native voice patterns pulled from real customers

---

## Notes on Quality

- Score 5 reviews should be read in full and treated as primary sources
- Score 2–3 reviews are useful for pattern confirmation but not quote sourcing
- If the review set is small (under 20 reviews), note this — patterns may not be statistically meaningful but language is still usable
- If a product has too few quality reviews to surface meaningful patterns, flag it rather than manufacturing themes that aren't there
