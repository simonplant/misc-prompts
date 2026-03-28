# Business Model Lens
*A configuration layer that adapts the core toolkit for business model evaluation and evolution.*

## What This Is

This is NOT a standalone prompt. It's a lens — a set of specific instructions you prepend to any core toolkit prompt when the subject is a business model. It tells the toolkit HOW to decompose, analyse, and evolve business models specifically.

Use it by pasting this lens BEFORE the toolkit prompt you're using, then pasting your business model material after.

## The Business Model Skeleton

Every business model, no matter how complex, rests on these six bones. When using any toolkit prompt on a business model, decompose to these components first:

### 1. The Problem-Customer Lock
- **Problem**: What specific pain exists, and how do people currently cope with it?
- **Customer**: Who has this pain badly enough to pay for relief? (Be specific: demographics, behaviours, psychographics — "SMBs" is not specific enough)
- **Lock**: Why are these two matched? What makes THIS customer segment the right entry point?

### 2. The Value Proposition
- **What you deliver**: The concrete outcome the customer gets
- **Why it's better**: Than the current alternative (including doing nothing)
- **Why they'll believe you**: What proof or signal makes the claim credible before they've tried it

### 3. The Revenue Engine
- **Pricing model**: How you charge (subscription, transaction, usage, licensing, etc.)
- **Unit economics**: What it costs to acquire a customer (CAC) vs. what they're worth (LTV)
- **The equation that must be true**: State the core formula. e.g., "LTV must be >3x CAC within 18 months"
- **Revenue concentration risk**: How dependent is revenue on a few large customers or a single stream?

### 4. The Moat
- **Type**: Network effects, switching costs, proprietary data/IP, brand, regulatory, economies of scale, or process advantage
- **Depth**: How long would it take a well-funded competitor to replicate this?
- **Compounding**: Does the moat get stronger over time, or does it erode?

### 5. The Growth Mechanism
- **Acquisition channels**: How customers find you (and the cost/scalability of each)
- **Retention mechanics**: What keeps them (and the leading indicators of churn)
- **Expansion mechanics**: How revenue per customer grows (upsell, cross-sell, usage growth)
- **Network dynamics**: Does each new customer make the product more valuable to existing ones?

### 6. The Execution Requirements
- **Critical capabilities**: What you must be able to do that's hard (technology, operations, talent)
- **Resource bottleneck**: The single scarcest resource that constrains growth
- **10x stress test**: What breaks first if you need to serve 10x your current volume?

## How To Use This Lens

**Method**: Paste this lens into the conversation BEFORE the toolkit prompt. Then paste your business model material. The lens modifies how the toolkit prompt operates — it doesn't replace it.

**Which prompts benefit most**: Root Finder > Extractor > Challenger > Evolver > Synthesizer > Distiller. For Distiller, the lens just changes compression labels — you can skip it.

### With The Extractor
The lens changes Step 3 (Build the Hierarchy). Instead of finding natural Level 0 categories, use the six bones AS your Level 0 categories. Each bone becomes a branch of the tree. This means your output looks like:

```
0. Problem-Customer Lock
   1. [idea about the problem] → depends on (0)
   1. [idea about the customer] → depends on (0)
0. Value Proposition
   1. [idea about what's delivered]
...
0. [Moat / Revenue Engine / Growth / Execution]
```

Flag which bones are well-developed (3+ Level 2 ideas) and which are skeletal (0-1 ideas).

### With The Root Finder
When finding hidden assumptions, test each bone independently:
- Problem-Customer Lock: "Is the pain real? Is it acute enough to pay for?"
- Value Prop: "Is the advantage durable or temporary?"
- Revenue Engine: "Does the math actually work at realistic assumptions?"
- Moat: "Is this genuinely defensible or just a head start?"
- Growth: "Can the acquisition channel scale without breaking unit economics?"
- Execution: "Do we actually have (or can we get) what's needed?"

### With The Challenger
Attack each bone. The most lethal attacks against business models typically come from:
- **Moat attacks**: "A competitor with [advantage] copies you in 6 months. What now?"
- **Unit economics attacks**: "CAC doubles because [channel saturation]. Does the model survive?"
- **Customer lock attacks**: "The customer segment is too small / too hard to reach / doesn't actually have this pain"
- **Timing attacks**: "This needed to launch 2 years ago / the window closes in 12 months"

### With The Evolver
The mutation operators map directly to the six bones:
- SWAP the customer segment (same product, different market)
- SWAP the revenue model (same product, different pricing)
- INVERT the value proposition (solve the opposite problem)
- SUBTRACT the most expensive component (what's the minimal viable version?)
- TRANSPLANT the core technology to a different industry
- LEAPFROG by asking: "If we were building this today with no legacy, what would we build?"

### With The Synthesizer
When synthesizing multiple analyses of a business model, adjudicate disagreements bone by bone. Sources that disagree about the moat but agree about the value prop are telling you something specific about where the uncertainty lives.

### With The Distiller
The four compression levels for business models follow the Distiller's standard levels:
- **Level 1 (Full Brief, 1-2 pages)**: Situation, findings, risks, and recommendation — structured by the six bones
- **Level 2 (Executive Summary, ~150 words)**: One dense paragraph covering: problem, customer, solution, moat, revenue model, growth mechanism, and the key risk
- **Level 3 (Elevator Pitch, 3-4 sentences)**: "We help [customer] solve [problem] by [mechanism]. We make money through [revenue model] and are protected by [moat]. The main risk is [risk]."
- **Level 4 (One-Liner)**: The core bet: "This works if [the single most important assumption] is true"

## The Viability Quick-Check

Before running any deep analysis, do this 60-second gut check on all six bones:

| Bone | Status |
|------|--------|
| Problem-Customer Lock | Clear / Fuzzy / Missing |
| Value Proposition | Clear / Fuzzy / Missing |
| Revenue Engine | Clear / Fuzzy / Missing |
| Moat | Clear / Fuzzy / Missing |
| Growth Mechanism | Clear / Fuzzy / Missing |
| Execution Requirements | Clear / Fuzzy / Missing |

If 3+ bones are "Missing," you're not ready for deep analysis — you're still in ideation. Use the Evolver to generate options before testing them.

If 3+ bones are "Clear," go straight to Challenger.

If it's mixed, use Root Finder to clarify the "Fuzzy" bones before challenging.
