# Distill
*Compress any analysis to the level of detail the decision requires.*

## Job

Take complex analysis and reduce it to what the decision-maker needs. Four compression levels. Preserve the logical spine and kill the padding.

## The Four Levels

### Level 1: The Full Brief (800-1,200 words)
A senior decision-maker reads this in 5 minutes and has everything to act.
- **Situation**: 2-3 sentences. No background the reader already knows.
- **Key Findings**: 3-5 most important. Each one paragraph: finding + evidence + why it matters.
- **Tensions & Risks**: Specific — name the risk AND its mechanism.
- **Recommendation**: Direct. "We should X because Y. Main risk is Z, mitigated by W."
- **What We Still Don't Know**: 2-3 things needing investigation before full commitment.

### Level 2: The Executive Summary (150-200 words)
One dense paragraph. Complete logic chain: situation → analysis → finding → recommendation → risk. Every sentence carries load. No throat-clearing ("This analysis examines..."). Start with the conclusion.

### Level 3: The Elevator Pitch (3-4 sentences)
First: key insight or recommendation. Second: primary evidence. Third: main risk or caveat. Optional fourth: ask or next step.

### Level 4: The One-Liner
Single sentence. If someone remembered one thing from the entire analysis, this is the right thing.

## Process

### 1. Identify the spine
Before compressing, find the minimal reasoning chain:
- Core claim
- Single strongest evidence
- Recommendation
- Biggest risk

The spine survives at every level.

### 2. Triage supporting material
- **Essential context**: Needed to understand spine (keep at L1, cut at L2+)
- **Important nuance**: Makes argument more precise (keep at L1-2, cut at L3+)
- **Supporting evidence**: Additional data (keep at L1, summarise at L2, cut at L3+)
- **Caveats**: Keep most important one, cut rest
- **Process artifacts**: How analysis was done (cut at all levels)

### 3. Compress
At each level verify:
- Contains full spine?
- Cut padding, not substance?
- Someone could act on this level alone? (Yes for L1-3)
- Compression is honest? (Not cherry-picking or hiding risks)

**Critical rule**: Risks must survive to Level 3. If risks disappeared during compression, add them back.

## Special Mode: Decision Frame

When input contains a comparison (e.g., from Evolve), add:
```
### Decision Frame
**The choice**: [Option A] vs [Option B]
**The tiebreaker**: [single factor that separates them]
**If you value [X]**: Choose [A] because [reason]
**If you value [Y]**: Choose [B] because [reason]
**My call**: [Option] — [one sentence]
**Irreversibility check**: Can this be undone if wrong? What's the cost of switching later?
```

## Output

```
## Distilled: [Title]

### Level 4: The One-Liner
[Single sentence]

### Level 3: The Elevator Pitch
[3-4 sentences]

### Level 2: The Executive Summary
[~150 word paragraph]

### Level 1: The Full Brief

**Situation**
[2-3 sentences]

**Key Findings**
1. [Finding + evidence + significance]
2. [Finding + evidence + significance]
3. [Finding + evidence + significance]

**Tensions & Risks**
- [Risk: mechanism and severity]

**Recommendation**
[Direct statement]

**What We Still Don't Know**
- [Open question 1]
- [Open question 2]
```

## Calibration

**GOOD Level 4:**
"The product solves a real problem but has no defensible moat and will run out of cash before closing enterprise deals at the projected rate."

**BAD Level 4:**
"The startup has potential but faces challenges."
*No specifics. Doesn't name the actual problem. Could describe literally any company.*

**GOOD Level 3:**
"The meeting summariser solves a validated pain point — teams waste 5+ hours/week on meeting follow-ups. But the technology has no patent or network effect, meaning any incumbent can replicate within 12 months. Unless the GTM pivots from enterprise to SMB-first, the company burns through runway before the first enterprise contracts close."

**BAD Level 3:**
"The company has a good product that solves meeting fatigue. There are some risks around competition and sales timelines. They should consider adjusting their strategy."
*Vague mechanism. "Some risks" and "consider adjusting" strip all signal.*

**GOOD Level 2 (~150 words):**
"Stress testing confirms the core value proposition — AI meeting summarisation eliminates 5+ hours of weekly meeting overhead per team, and three of four AI sources independently validated the demand signal. However, two structural flaws threaten viability. First, the moat is fatally weak: no proprietary data, no network effects, and the core NLP capability is commoditising rapidly — Zoom, Teams, and Otter.ai all ship comparable features. Second, the business plan assumes a 6-month enterprise sales cycle when category averages run 9-14 months, creating a cash flow gap the current runway can't cover. The strongest path forward is an SMB-first GTM motion with self-serve onboarding, buying time to develop a defensible advantage through integration depth or proprietary workflow data. Without a moat pivot, this is a feature, not a company."

**BAD Level 2:**
"The analysis found several strengths and weaknesses. The product is good but faces competition. Sales might take longer than expected. The recommendation is to consider alternative approaches."
*Could describe any business. No specifics, evidence, or mechanism.*

## Self-Check

- [ ] Level 4 contains the single most important finding — not a generic summary
- [ ] Level 3 names risks by mechanism, not category
- [ ] Level 2 is ≤ 200 words with evidence, not just assertions
- [ ] Level 1 is 800-1,200 words
- [ ] Recommendation gets MORE direct at lower levels, not vaguer
- [ ] Risks survive to Level 3

## Hand-Off

Distill is typically the last tool. Output goes to the decision-maker.

If distillation reveals the analysis is incomplete (spine doesn't hold up stripped of detail), flag it and recommend: spine weak → **Assumptions**, evidence weak → **Stress Test**, options unclear → **Evolve**.
