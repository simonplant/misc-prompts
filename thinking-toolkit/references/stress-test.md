# Stress Test
*Find the breaking points before reality does.*

## Job

Mount the strongest possible attacks against an idea, plan, or strategy. For every attack, state the strongest defence. Produce verdicts. Then construct the steelman — the strongest surviving version.

## Process

### 1. Identify and prioritise attack surfaces (3-5)

Search in this priority order:
1. **Load-bearing assumptions**: If these break, everything collapses. (High blast-radius items from Assumptions tool, if provided.)
2. **Single points of failure**: No backup or fallback.
3. **Market and timing risks**: Conditions outside anyone's control.
4. **Execution risks**: Required capabilities or resources that may not exist.

Skip peripheral details. If the foundation is cracked, the paint colour doesn't matter.

### 2. Mount attacks (debate protocol)

For each attack surface:

**THE ATTACK** (strongest case against)
- Thesis: "This fails because..."
- Evidence: What specifically goes wrong
- Failure scenario: What collapse looks like in practice
- Precedent: Specific company, project, or event where this happened. If none: "No direct precedent — reasoning from [principle]."

**THE DEFENCE** (strongest rebuttal)
- Best counter-argument + evidence
- Strength: **Sufficient** (fully neutralises) / **Partial** (weakens but doesn't eliminate) / **Insufficient** (doesn't address core mechanism)

**VERDICT**
- **SURVIVES**: Defence holds. Risk to monitor, not a flaw to fix.
- **WOUNDED**: Defence is partial. State the condition — specific on three dimensions:
  - **WHAT** must change
  - **HOW** (mechanism)
  - **WHEN** (timeline)
  - Format: "Survives IF [WHAT], [HOW], [WHEN]"
- **FATAL**: No adequate defence. State what would need to be fundamentally different.

### 3. Cascade analysis

Consider 2-3 scenarios where attacks combine:
- Two highest-damage attacks landing simultaneously — combined effect worse than either alone?
- Which attacks reinforce each other? (e.g., moat attack + pricing attack = copied AND undercut)
- Do multiple WOUNDED attacks combine into FATAL?

### 4. Steelman construction

Build the strongest surviving version:
- Keep everything that SURVIVED unchanged
- Make best-case assumptions explicit for WOUNDED items
- Remove only FATAL elements
- Add nothing new — steelman uses only original material

State: "This succeeds if [condition 1], [condition 2], and [condition 3] all hold."

## Output

```
## Stress Test Report: [Title]

### Attack Surface Summary
| # | Target | Type | Damage Potential |
|---|--------|------|-----------------|
| 1 | [what] | [load-bearing/SPOF/timing/execution] | [High/Medium/Low] |

### Attack 1: [Name]
**TARGET**: [specific assumption or claim]
**THE ATTACK**
Thesis: [fails because...]
Evidence: [what goes wrong]
Failure scenario: [what collapse looks like]
Precedent: [specific case]
**THE DEFENCE**
[counter-argument + evidence]
Strength: [Sufficient/Partial/Insufficient]
**VERDICT**: [SURVIVES/WOUNDED/FATAL]
[One sentence. If WOUNDED: "Survives IF [WHAT], [HOW], [WHEN]"]

(repeat for each attack)

### Cascade Analysis
- [Attack X] + [Attack Y]: [combined effect]
- Combined survivability: [assessment]

### The Steelman
[2-3 paragraphs: strongest version + explicit conditions for success]

### Summary Scorecard
Survived: [N] | Wounded: [N] | Fatal: [N]
[One paragraph: viable? What needs to change?]
```

## Calibration

**GOOD attack:**
"TARGET: Enterprise customers will adopt within 6 months. ATTACK: Enterprise sales cycles average 9-14 months for new vendor categories. Salesforce took 18 months for its first 10 enterprise accounts. The 6-month assumption means the cash runway model is wrong — need 2-3x projected runway. DEFENCE: Could start SMB for faster cycles. Strength: Partial — addresses timeline but not revenue gap. VERDICT: WOUNDED — survives IF GTM pivots to SMB-first [WHAT] with self-serve onboarding [HOW] within 90 days [WHEN]."

**BAD attack:**
"TARGET: The business model. ATTACK: Competition is fierce. DEFENCE: They have good technology. VERDICT: WOUNDED."
*No mechanism. No precedent. No condition. "Fierce competition" is a category, not an attack.*

## Guardrails

- Don't invent attacks requiring implausible scenarios ("what if an asteroid hits")
- Don't nitpick peripheral details when the foundations are the real issue
- Don't generate solutions — that's Evolve's job

## Self-Check

- [ ] ≥ 3 attacks mounted
- [ ] Every attack has a specific failure mechanism, not just a category
- [ ] Every WOUNDED verdict has a WHAT/HOW/WHEN condition
- [ ] Every attack has a real precedent or explicit "no precedent — reasoning from [principle]"
- [ ] Steelman states explicit conditions: "succeeds if [1], [2], [3]"
- [ ] Cascade analysis covers ≥ 1 multi-attack scenario

## Hand-Off

Add mutation targets for Evolve:
```
### Mutation Targets for Evolve
1. [WOUNDED verdict]: Consider [SWAP/INVERT/TRANSPLANT] on [component]
2. [FATAL verdict]: Consider [operator] on [component]
```

Feeds into: **Evolve** (fix wounds/fatals), **Distill** (go/no-go summary), **Stress Test again** (after Evolve produces new option — compare: did Evolve fix the wounds, or introduce new ones?).
