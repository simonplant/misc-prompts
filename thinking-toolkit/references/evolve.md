# Evolve
*Generate genuinely different alternatives — mutate, compare, recommend.*

## Job

Take an idea that's been mapped and stress-tested, and generate alternatives that address its weaknesses while preserving its strengths. Every alternative must be meaningfully different — not a cosmetic variation. Then compare all options and make a clear recommendation.

If Stress Test output is provided, alternatives MUST address the WOUNDED and FATAL findings. An alternative with the same fatal flaw as the original is a failure.

## Process

### 1. Decompose into moveable parts

Break the input into independently changeable components.

**Business model**: who you serve, what problem you solve, how you deliver, how you make money, why you win, how you grow.

**Strategy/argument**: core thesis, key evidence, mechanism, scope, timing.

**Anything else**: identify 4-6 fundamental dimensions.

### 2. Generate alternatives (4-6) via mutation operators

**SWAP**: Replace one component entirely (different customer, different revenue model)

**INVERT**: Flip a core assumption. If original assumes "customers want X," what if they want the opposite?

**TRANSPLANT**: Take the core insight and apply to a completely different domain or market

**COMBINE**: Merge strongest elements of two different approaches

**SUBTRACT**: Remove the most complex/expensive component. What's the simplest version that works?

**LEAPFROG**: Skip the current plan. Starting from scratch with the same goal but no existing assumptions, what would you build?

**Rules:**
- Every alternative changes ≥ 2 components. Changing only pricing is a variation, not an alternative.
- ≥ 1 alternative must use INVERT or LEAPFROG (the radical option).

For each alternative: name it, state core concept (2-3 sentences), list mutations applied + components changed, explain which original weakness it addresses.

### 3. Comparative assessment

Evaluate original + all alternatives:

| Dimension | Definition |
|-----------|-----------|
| **Solves the problem** | Actually addresses the core need? |
| **Defensible** | Can competitors easily copy this? |
| **Executable** | Buildable with available resources? |
| **Scalable** | Gets better or worse as it grows? |
| **Resilient** | How many Stress Test attacks does it survive? |
| **Upside** | Best case if everything goes right? |

Rate: **Strong / Adequate / Weak** with a one-sentence justification per cell. The justification IS the assessment.

### 4. Recommendation

1. **Primary**: Strongest overall option (may be original). Why?
2. **Fallback**: Best if primary fails. Why second?
3. **Hybrid opportunity**: Can elements of 2+ options combine into something stronger? Describe, or "None."
4. **Kill list**: Which to abandon, and why.

### 5. Evolution directive (for iterative use)

- **New baseline**: The recommended option
- **Biggest remaining weakness**: What
- **Next mutation focus**: Which operator, which component
- **Key question**: What needs answering before next round

## Output

```
## Evolution Report: [Title]

### Original Decomposition
- [Component 1]: [current state]
- [Component 2]: [current state]

### Weaknesses Being Addressed
(from Stress Test if provided — otherwise identify the original's top 2-3 weaknesses yourself)
1. [Weakness]: [FATAL/WOUNDED]

### Alternative 1: [Name]
**Core concept**: [2-3 sentences]
**Mutations**: [SWAP/INVERT/etc. — which components changed]
**Addresses**: [which weakness]

(repeat for 4-6 alternatives)

### Comparative Assessment

| Dimension | Original | Alt 1 | Alt 2 | Alt 3 | Alt 4 |
|-----------|----------|-------|-------|-------|-------|
| Solves the problem | [S/A/W] | ... | ... | ... | ... |
| Defensible | ... | ... | ... | ... | ... |
| Executable | ... | ... | ... | ... | ... |
| Scalable | ... | ... | ... | ... | ... |
| Resilient | ... | ... | ... | ... | ... |
| Upside | ... | ... | ... | ... | ... |

### Justifications
[One sentence per cell]

### Recommendation
**Primary**: [option] — [why]
**Fallback**: [option] — [why second]
**Hybrid**: [description or "None"]
**Kill list**: [what to abandon + why]

### Evolution Directive
- New baseline: [option]
- Biggest remaining weakness: [what]
- Next mutation focus: [operator + component]
- Key question: [what to resolve]
```

## Calibration

**GOOD alternative** (from B2B SaaS meeting summariser):
"Name: The Intelligence Layer. Mutations: TRANSPLANT (end-user tool → platform API) + SWAP (customer: team leads → SaaS vendors). Core concept: License the summarisation engine as an API that Zoom, Teams, and Webex embed natively. Addresses: eliminates customer acquisition problem — distribution through existing platforms. Components changed: customer, delivery model, growth mechanism."

**BAD alternative** (same input):
"Name: Enterprise Edition. Mutations: SWAP customer. Core concept: Sell the same product to larger companies. Addresses: larger deal sizes improve unit economics."
*Changed only one component (customer segment). Product, delivery, revenue, moat, growth all identical. This is a pricing tier, not an alternative.*

## Guardrails

- Don't generate "alternatives" that are trivially different from the original
- At least one alternative should feel uncomfortable — if they're all safe, push harder

## Self-Check

- [ ] ≥ 4 alternatives generated
- [ ] Every alternative changes ≥ 2 components
- [ ] ≥ 1 uses INVERT or LEAPFROG
- [ ] No alternative shares a FATAL flaw from previous Stress Test
- [ ] Recommendation picks a winner — no "it depends"
- [ ] Every assessment cell has a justification

## Hand-Off

Feeds into: **Stress Test** (stress-test the recommendation), **Distill** (compress to decision), **Evolve again** (use Evolution Directive as input for next round).
