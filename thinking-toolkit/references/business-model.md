# Business Model Analysis
*Self-contained business model evaluation using the 6-bone skeleton.*

## Job

Analyse a business model end-to-end: decompose it, find hidden assumptions, stress-test it, and produce a decision-ready assessment. This tool integrates Structure, Assumptions, Stress Test, and Distill into a single business-model-specific flow.

## The 6-Bone Skeleton

Every business model rests on these six bones:

### 1. Problem-Customer Lock
- **Problem**: What specific pain exists? How do people currently cope?
- **Customer**: Who has this pain badly enough to pay? (Be specific — demographics, behaviours, psychographics. "SMBs" is not specific enough.)
- **Lock**: Why are these two matched? Why is THIS segment the right entry point?

### 2. Value Proposition
- **What you deliver**: Concrete outcome the customer gets
- **Why it's better**: Than the current alternative (including doing nothing)
- **Why they'll believe you**: Proof or signal that makes the claim credible pre-purchase

### 3. Revenue Engine
- **Pricing model**: How you charge (subscription, transaction, usage, licensing, etc.)
- **Unit economics**: CAC vs. LTV
- **The equation that must be true**: e.g., "LTV must be >3x CAC within 18 months"
- **Revenue concentration risk**: Dependent on a few large customers or single stream?

### 4. Moat
- **Type**: Network effects / switching costs / proprietary data-IP / brand / regulatory / economies of scale / process advantage
- **Depth**: How long for a well-funded competitor to replicate?
- **Compounding**: Gets stronger over time, or erodes?

### 5. Growth Mechanism
- **Acquisition channels**: How customers find you (cost + scalability of each)
- **Retention mechanics**: What keeps them (leading indicators of churn)
- **Expansion mechanics**: How revenue per customer grows (upsell, cross-sell, usage)
- **Network dynamics**: Does each new customer make the product more valuable?

### 6. Execution Requirements
- **Critical capabilities**: What you must be able to do that's hard
- **Resource bottleneck**: Single scarcest resource constraining growth
- **10x stress test**: What breaks first at 10x current volume?

## Process

### Step 1: Viability quick-check (60 seconds)

| Bone | Status |
|------|--------|
| Problem-Customer Lock | Clear / Fuzzy / Missing |
| Value Proposition | Clear / Fuzzy / Missing |
| Revenue Engine | Clear / Fuzzy / Missing |
| Moat | Clear / Fuzzy / Missing |
| Growth Mechanism | Clear / Fuzzy / Missing |
| Execution Requirements | Clear / Fuzzy / Missing |

- **3+ Missing** → Not ready for deep analysis. Still in ideation. Note what's missing and stop, or use Evolve to generate options.
- **3+ Clear** → Go straight to Step 3 (stress test).
- **Mixed** → Step 2 first (dig into Fuzzy bones).

### Step 2: Assumption dig (per bone)

For each Fuzzy or Missing bone, find what's hidden:
- Problem-Customer Lock: "Is the pain real? Acute enough to pay for?"
- Value Prop: "Is the advantage durable or temporary?"
- Revenue Engine: "Does the math work at realistic assumptions?"
- Moat: "Genuinely defensible or just a head start?"
- Growth: "Can acquisition scale without breaking unit economics?"
- Execution: "Do we actually have (or can we get) what's needed?"

Produce an assumption register (see `assumptions.md` format) focused on the weakest bones.

### Step 3: Stress test (bone by bone)

Attack each bone. The most lethal attacks typically come from:
- **Moat attacks**: "A competitor with [advantage] copies you in 6 months. What now?"
- **Unit economics attacks**: "CAC doubles because [channel saturation]. Does the model survive?"
- **Customer lock attacks**: "Segment is too small / too hard to reach / doesn't actually have this pain"
- **Timing attacks**: "Needed to launch 2 years ago / window closes in 12 months"

Use Stress Test format: ATTACK → DEFENCE → VERDICT (SURVIVES/WOUNDED/FATAL).

### Step 4: Distill

Compress to four levels using the business model frame:
- **Level 4**: "This works if [single most important assumption] is true"
- **Level 3**: "We help [customer] solve [problem] by [mechanism]. We make money through [revenue model] and are protected by [moat]. The main risk is [risk]."
- **Level 2**: One paragraph covering all six bones + key risk (~150 words)
- **Level 1**: Full brief structured by the six bones (800-1,200 words)

## Output

```
## Business Model Analysis: [Title]

### Viability Quick-Check
[Table: 6 bones × Clear/Fuzzy/Missing]

### Skeleton Breakdown
[Each bone filled in with available detail. Flag what's thin.]

### Assumption Register
[Table: hidden assumptions per bone, with blast radius + test method]

### Stress Test
[3-4 attacks in ATTACK/DEFENCE/VERDICT format, prioritising weakest bones]

### Scorecard
Survived: [N] | Wounded: [N] | Fatal: [N]

### Distilled

**Level 4**: [One sentence — the core bet]
**Level 3**: [3-4 sentences]
**Level 2**: [~150 word paragraph]
**Level 1**: [Full brief, 800-1,200 words, structured by 6 bones]
```

## Calibration

**GOOD viability quick-check:**

| Bone | Status |
|------|--------|
| Problem-Customer Lock | Clear — validated pain: teams lose 5+ hrs/week to meeting follow-up |
| Value Proposition | Clear — AI extracts action items, assigns owners automatically |
| Revenue Engine | Fuzzy — says "SaaS pricing" but no CAC/LTV estimate |
| Moat | Missing — no proprietary data, no network effects mentioned |
| Growth Mechanism | Fuzzy — "viral adoption" with no mechanic described |
| Execution Requirements | Clear — team has NLP background, prototype built |

*3 bones Clear, 2 Fuzzy, 1 Missing → mixed profile → dig into Revenue Engine, Moat, Growth before stress testing.*

**GOOD Level 4:**
"This works if meeting summarisation can't be commoditised by Zoom, Teams, or Otter.ai within 18 months — and right now, nothing prevents them."

**BAD Level 4:**
"An interesting opportunity with strong product-market fit potential."
*No specific assumption named. Could describe any startup.*

## Hand-Off

If the user wants alternatives after analysis, use **Evolve** with bone-specific mutations:
- SWAP the customer segment (same product, different market)
- SWAP the revenue model (same product, different pricing)
- INVERT the value proposition (solve the opposite problem)
- SUBTRACT the most expensive component (minimal viable version?)
- TRANSPLANT the core technology to a different industry
- LEAPFROG: "If building this today with no legacy, what would we build?"

## Self-Check

- [ ] All 6 bones addressed (even if some are "Missing — not enough data")
- [ ] Viability quick-check completed before deep analysis
- [ ] Assumption register has ≥ 1 hidden assumption per Fuzzy/Missing bone
- [ ] Stress test has ≥ 3 attacks with specific mechanisms and precedents
- [ ] Level 4 names the single most important assumption, not a generic summary
- [ ] Moat bone is assessed for type, depth, AND compounding direction
