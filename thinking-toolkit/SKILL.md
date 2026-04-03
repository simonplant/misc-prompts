---
name: thinking-toolkit
description: "Structured analysis techniques. Use ONLY when the user explicitly asks to: stress-test or tear apart an idea, analyze or evaluate a business model or strategy, synthesize multiple AI/research sources, generate alternatives to a plan, find hidden assumptions in an argument, or compress an analysis to a decision. Do NOT trigger on general questions, casual thinking, or 'help me with X' requests."
---

# Thinking Toolkit

Six techniques that produce sharper analysis than baseline. Use whichever section fits — don't run everything every time. The calibration examples set your quality bar.

---

## 1. Stress Test

Attack an idea with the strongest case against, then the strongest defence, then a verdict.

**Attack format** (per attack surface, prioritize load-bearing assumptions first):

- **TARGET**: The specific assumption or claim
- **ATTACK**: "This fails because..." + specific failure mechanism + what collapse looks like + a real-world precedent (name a company/event, or say "no precedent — reasoning from [principle]")
- **DEFENCE**: Best counter-argument. Strength: Sufficient / Partial / Insufficient
- **VERDICT**:
  - **SURVIVES** — defence holds, risk to monitor
  - **WOUNDED** — partial defence. Must state: "Survives IF [WHAT changes], [HOW], [WHEN]" — all three dimensions required
  - **FATAL** — no defence. State what would need to be fundamentally different

After individual attacks: **cascade analysis** (do 2-3 attacks combining make things worse?) and **steelman** ("This succeeds if [1], [2], [3] all hold").

**GOOD**: "TARGET: Enterprise adoption in 6 months. ATTACK: Enterprise sales cycles average 9-14 months. Salesforce took 18 months for first 10 accounts. Cash runway model is wrong — need 2-3x. DEFENCE: Start SMB first. Strength: Partial. VERDICT: WOUNDED — survives IF GTM pivots to SMB-first [WHAT] with self-serve onboarding [HOW] within 90 days [WHEN]."

**BAD**: "TARGET: Business model. ATTACK: Competition is fierce. DEFENCE: Good technology. VERDICT: WOUNDED." — No mechanism, no precedent, no condition. "Fierce competition" is a category, not an attack.

---

## 2. Evolve

Generate genuinely different alternatives, not cosmetic variations.

**Decompose** the idea into moveable parts (customer, problem, delivery, revenue, moat, growth — or whatever dimensions define it).

**Mutate** using these operators to produce 4-6 alternatives:
- **SWAP** — replace one component entirely
- **INVERT** — flip a core assumption to its opposite
- **TRANSPLANT** — apply the core insight to a different domain
- **COMBINE** — merge strongest elements of two approaches
- **SUBTRACT** — remove the most complex component; what's the simplest version?
- **LEAPFROG** — start from scratch with same goal, no existing assumptions

**Rules**: Every alternative changes ≥ 2 components. At least one must use INVERT or LEAPFROG. If prior stress test exists, alternatives must fix the WOUNDED/FATAL findings — an alternative with the same fatal flaw is a failure.

**Compare** all options (including original): Strong / Adequate / Weak on each of: solves the problem, defensible, executable, scalable, resilient, upside. One-sentence justification per cell. Pick a winner.

**GOOD**: "The Intelligence Layer. TRANSPLANT (end-user tool → platform API) + SWAP (customer: teams → SaaS vendors). License the engine as API for Zoom/Teams/Webex to embed natively. Fixes: eliminates customer acquisition problem. 3 components changed."

**BAD**: "Enterprise Edition. SWAP customer. Sell same product to bigger companies." — One component changed. Same product, delivery, moat, growth. This is a pricing tier, not an alternative.

---

## 3. Synthesize

Fuse 2+ sources into one unified view, adjudicating disagreements by evidence quality.

**Classify** every claim: CONSENSUS (same substance + evidence), CONTESTED (active disagreement), UNIQUE (one source only — don't dismiss; assess independently).

Watch for **convergent** claims masquerading as consensus: Source A says "12% CAGR" and Source B says "strong growth" — same direction but different rigour. Not consensus.

**Adjudicate** contested claims using these tests in priority order (stop at first clear winner):
1. **Logic** — if one has a logical gap or contradiction, the other wins even with less evidence
2. **Evidence** — specific data beats assertions; primary beats secondary; recent beats dated
3. **Explanatory power** — which explains more facts with fewer assumptions?
4. **Convergence** (tiebreaker only) — majority agreement, but one well-evidenced minority view outweighs unsupported majority

Verdict: **Resolved** (confidence: High/Moderate/Low) or **Genuinely uncertain** (state what evidence would settle it) or **False dichotomy** (disagreement dissolves under reframing).

**Emergent findings** must meet this template or they're speculation — cut them:
> "Source A's [X] combined with Source B's [Y] implies [Z], which neither stated."

Write the unified view in a single voice. Remove "Source A says" / "according to B." Shorter than any single input.

**GOOD**: "CONTESTED: Market growing or stagnant. A cites 12% CAGR from IDC 2025. B says 'mature' with no citation. Evidence test: A wins — specific, dated, third-party. Confidence: High."

**BAD**: "Both make good points. The truth is probably somewhere in between." — No test applied, no verdict.

---

## 4. Distill

Compress to the level of detail the decision requires. Four levels, each preserving the logical spine (core claim + strongest evidence + recommendation + biggest risk).

| Level | Format | Rule |
|-------|--------|------|
| **4: One-Liner** | Single sentence | The one thing worth remembering |
| **3: Elevator Pitch** | 3-4 sentences | Insight + evidence + risk + next step |
| **2: Executive Summary** | ~150 words | Complete logic chain, one paragraph. Start with conclusion, no throat-clearing |
| **1: Full Brief** | 800-1,200 words | Situation, Key Findings (3-5), Tensions & Risks, Recommendation, What We Still Don't Know |

**Critical rule**: Risks must survive to Level 3. If they vanished during compression, add them back. Recommendation gets MORE direct at lower levels, not vaguer.

**Decision Frame** (when comparing options): The choice / the tiebreaker / "if you value X, choose A" / "if you value Y, choose B" / my call / irreversibility check (can this be undone? switching cost?).

**GOOD L4**: "The product solves a real problem but has no defensible moat and will run out of cash before closing enterprise deals at the projected rate."

**BAD L4**: "The startup has potential but faces challenges." — Could describe any company. No specifics.

**GOOD L3**: "The meeting summariser solves a validated pain — teams waste 5+ hrs/week on follow-ups. But no patent or network effect means any incumbent replicates in 12 months. Unless GTM pivots to SMB-first, runway burns before first enterprise contracts close."

**BAD L3**: "Good product, some risks around competition and timelines. Should consider adjusting." — Vague mechanism. "Some risks" strips all signal.

---

## 5. Assumptions

Dig beneath structured ideas to find what's hidden.

**For each major claim, find**:
- What must be true for this to work (preconditions)
- Which preconditions are unstated (these are your findings)
- How testable is each (design a test, or mark "article of faith")
- What's the blast radius if wrong — name the mechanism ("collapses revenue model because 80% of value is in claims above $10K")

**Output as assumption register**:

| # | Assumption | Stated/Hidden | Blast Radius | Test Method |
|---|-----------|---------------|-------------|-------------|
| 1 | [specific] | Hidden | High — [mechanism] | [concrete test] |

**3-layer drivers** — for the 2-3 most important claims, trace: Surface (what's said) → Functional (what it does in the argument) → Root (deepest why — stop at bedrock: physical constraint, external fact, or article of faith).

**Logic chains** — trace `Premise A + Premise B → Conclusion C` and flag each link: Valid / Unsupported Leap / Hidden Premise / Non Sequitur.

**GOOD**: "Insurance companies will trust AI on claims above $10K | Hidden | High — collapses revenue model (80% of claims value in top 20%) | Interview 5 claims VPs: would they delegate to vendor AI above $10K?"

**BAD**: "AI can process claims | Stated | High | Try it and see" — Surface-level, no mechanism, not a test method.

---

## 6. Business Model Framework

When analyzing a business model, decompose to these six bones before applying any other technique:

| Bone | Key questions |
|------|-------------|
| **Problem-Customer Lock** | What pain? Who has it badly enough to pay? Why these two matched? |
| **Value Proposition** | What outcome? Why better than doing nothing? Why credible pre-purchase? |
| **Revenue Engine** | Pricing model? CAC vs LTV? The equation that must be true? Concentration risk? |
| **Moat** | Type? Depth (replication time)? Compounding (stronger or eroding)? |
| **Growth** | Acquisition channels + cost? Retention mechanics? Expansion? Network effects? |
| **Execution** | Critical hard capabilities? Scarcest resource? What breaks at 10x? |

**Quick-check** each bone: Clear / Fuzzy / Missing. If 3+ Missing, you're in ideation, not analysis. If 3+ Clear, go straight to stress test.

Use the bones as your decomposition when running Stress Test (attack per bone) or Evolve (mutate per bone: SWAP customer, INVERT value prop, SUBTRACT most expensive component, etc.).
