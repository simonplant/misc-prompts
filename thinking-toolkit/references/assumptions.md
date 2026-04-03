# Assumptions
*Find the real assumptions, drivers, and logic holding everything together.*

## Job

Take structured input and dig beneath it. Make the invisible visible: unstated assumptions, hidden dependencies, actual drivers behind surface claims, and the logical skeleton.

## Process

### 1. Assumption excavation

For every major claim, ask in order:
1. **What must be true for this to work?** List every precondition — market conditions, behaviours, technical capabilities, timing, resources.
2. **Which are stated vs. unstated?** The unstated ones are your findings.
3. **How testable?** Can you design a test that would prove it wrong? If not, mark as article of faith.
4. **What's the blast radius?** Does one thing break, or does the whole structure collapse? Name the mechanism.

### 2. Driver analysis (3-layer)

For each major theme, trace:
- **Surface**: What's said (the stated reason)
- **Functional**: What it actually does in the logic of the argument
- **Root**: The deepest "why" — the thing that, if changed, changes everything above

Use "Five Whys" but stop at **bedrock**: self-evidently true, article of faith, or testable empirical fact.

**Bedrock examples:**
- "Manual data entry is inherently slow" → BEDROCK (physical constraint)
- "Regulation requires it" → BEDROCK (external fact, testable)
- "Our founder is a domain expert" → BEDROCK (article of faith — may or may not translate)

### 3. Logic chain mapping

Trace the argumentative logic: `Premise A + Premise B → Conclusion C`. For each link, verdict:
- **Valid**: Conclusion follows from premises
- **Unsupported leap**: Conclusion requires something not in the premises
- **Hidden premise**: Unstated assumption bridging the gap
- **Non sequitur**: Conclusion doesn't follow

### 4. Assumption cluster check

After mapping individual assumptions, check for **clusters** — webs of assumptions that reinforce or undermine each other:
- **Reinforcement loops**: Which assumptions strengthen each other? (If both hold, they're very strong; if one falls, does the other weaken?)
- **Cascade vulnerabilities**: If assumption #3 fails, which others collapse with it?
- **Hidden dependencies**: Are two "independent" assumptions actually resting on the same unstated foundation?

Flag any assumption whose failure cascades to 2+ others as a **cluster vulnerability**.

### 5. Power and incentive check (optional)

Skip if the input is purely technical with no stakeholders. Otherwise:
- **Who benefits** from the current framing? Name specific roles or entities.
- **What incentives** are visible? Only flag incentives you can point to evidence for — do not speculate about hidden psychological motives.
- **What would the opposition say?** The most evidence-based counter-argument from someone with skin in the game.

### 6. Silence check

Scan for **strategic silences** — what's conspicuously absent:
- What perspectives or stakeholders are never mentioned?
- What alternative framings are implicitly excluded?
- What would the strongest opponent say is being ignored?

Note silences only when they're load-bearing (hiding a real vulnerability), not just omissions.

## Output

```
## Root Analysis: [Title]

### Assumption Register

| # | Assumption | Stated/Hidden | Testable? | Blast Radius | Test Method |
|---|-----------|---------------|-----------|-------------|-------------|
| 1 | [assumption] | Hidden | Yes | High — collapses [what] | [how to test] |

### Cluster Vulnerabilities
- Assumptions [#2, #4, #5] form a cluster: if [#2] fails, [#4] and [#5] collapse because [mechanism]

### Driver Map

**[Theme/Claim]**
- Surface: [what's said]
- Functional: [what it does in the argument]
- Root: [deepest driver]
- Depth: [levels to bedrock]

### Logic Chain

Premise: [A]
+ Premise: [B]
→ Conclusion: [C] — VALID

Premise: [C]
+ Hidden Premise: [D — never stated but required]
→ Conclusion: [E] — UNSUPPORTED LEAP
  ↳ Gap: [what's missing]

### Power & Incentives
(if applicable)
- Benefits: [who gains from this framing]
- Incentives: [what's shaping the argument — evidence-based only]
- Strongest opposition: [best counter-argument]

### Strategic Silences
- [What's absent and why it matters]

### Root Vulnerabilities — Ranked by Blast Radius
1. **[Most dangerous]**: If wrong, [what collapses]. Test by: [method].
2. ...

### What This Means
[2-3 paragraphs plain language: What is this REALLY about? Where is it standing on air?]
```

## Calibration

**GOOD assumption register entry** (input: "AI startup to automate 80% of insurance claims"):

| # | Assumption | Stated/Hidden | Testable? | Blast Radius | Test Method |
|---|-----------|---------------|-----------|-------------|-------------|
| 1 | Insurance companies will trust AI decisions on claims above $10K | Hidden | Yes | High — collapses revenue model (80% of claims value is in the 20% above $10K) | Interview 5 claims VPs at mid-tier insurers: would they delegate authority to a vendor's AI for claims over $10K? |

*Specific, hidden, blast radius explains the mechanism, test is concrete and cheap.*

**BAD:**

| # | Assumption | Stated/Hidden | Testable? | Blast Radius | Test Method |
|---|-----------|---------------|-----------|-------------|-------------|
| 1 | AI can process claims | Stated | Yes | High | Try it and see |

*Surface-level. Doesn't dig into what kind, at what authority level, what accuracy. "Try it and see" isn't a test method.*

**GOOD driver map:**
- Surface: AI handles most claims automatically
- Functional: This is the unit economics argument — if automation is below ~60%, cost savings don't offset integration cost
- Root: Insurance margins are compressing (loss ratios rising 60% → 70%+), forcing operational cost cuts. The startup isn't selling AI — it's selling margin preservation.
- Depth: 3 levels

**BAD driver map:**
- Surface: They want to automate claims
- Functional: This makes the product useful
- Root: AI is getting better at automation

*Surface and Functional say the same thing. Root is a technology trend, not a driver of THIS claim.*

## Guardrails

- Don't suggest fixes or generate alternatives — that's Evolve's job
- Don't challenge or attack — that's Stress Test's job
- Don't hedge with "it depends" — take a position on what you find

## Self-Check

- [ ] ≥ 3 assumption register entries
- [ ] Every hidden assumption has a test method or is marked "article of faith"
- [ ] Driver map goes deeper than surface for ≥ 2 themes
- [ ] Logic chain identifies ≥ 1 gap, hidden premise, or unsupported leap
- [ ] "What This Means" is plain language a non-expert could follow

## Hand-Off

Add attack surfaces for the next tool:
```
### Suggested Attack Surfaces for Stress Test
1. [Vulnerability]: Attack by [specific angle]
2. [Vulnerability]: Attack by [angle]
3. [Vulnerability]: Attack by [angle]
```

Feeds into: **Stress Test** (attack vulnerabilities), **Evolve** (evolve weak assumptions), **Distill** (summary of what's really going on).
