# Synthesize
*Fuse multiple sources into a single unified view — weighted by evidence, not volume.*

## Job

Take 2+ sources (AI model outputs, research documents, competing analyses) and produce one unified document. Adjudicate disagreements based on evidence quality and logical coherence. When sources disagree, determine which position is better supported and say so.

## Process

### 1. Extract and classify claims

From each source, extract every distinct claim as a clear sentence. Classify each:

**CONSENSUS** — Sources agree on the substance (not just the wording).
- Calibration: Two claims count as consensus ONLY if they cite the same evidence or reach the same conclusion through independent reasoning. Source A says "market growing at 12%" and Source B says "market expansion is strong" — these are NOT consensus. They're **CONVERGENT** (same direction, different rigour). Mark them separately.

**CONTESTED** — Sources actively disagree on substance.
- State each position clearly.
- Name the crux: Different evidence? Different logic from same evidence? Different values/priorities?

**UNIQUE** — Only one source raises this.
- Don't dismiss for being an outlier. Assess evidence independently. Unique claims with strong evidence are often the most valuable findings.

### 2. Adjudicate contested claims

Apply these tests in priority order. Stop at the first that produces a clear winner:

1. **Logic test** (highest priority): Trace reasoning chains. If one contains a logical gap, unsupported leap, or internal contradiction — the other wins, even with less evidence. Broken logic can't be rescued by more data.

2. **Evidence test**: Which cites more concrete, verifiable evidence? Specific data beats general assertions. Primary beats secondary. Recent beats dated.

3. **Explanatory power test**: Which explains more observed facts with fewer assumptions?

4. **Convergence test** (tiebreaker only): If tests 1-3 are inconclusive, majority agreement matters — but one well-evidenced minority view still outweighs unsupported majority consensus.

**Verdict for each contested claim:**
- **Resolved**: Position X stronger because [reason from tests above]. Confidence: High / Moderate / Low.
- **Genuinely uncertain**: Tests conflict or inconclusive. What evidence would settle it: [specific investigation].
- **False dichotomy**: Disagreement dissolves when you realise [reframing].

### 3. Identify emergent findings

Insights that exist in no single source but become visible in combination. Every emergent finding must meet this template:

> "Source A's finding that [X] combined with Source B's evidence for [Y] implies [Z], which neither source stated."

If you can't fill that template with specific references, it's speculation. Cut it.

### 4. Write the unified view

Produce a coherent narrative structured by topic, not by source. Single voice — search for and remove "Source A says" or "according to B" from final prose. Must be shorter than any single input.

## Output

```
## Synthesis: [Title]

### Sources
- Source A: [one-line description]
- Source B: [one-line description]

### The Unified View
[Coherent prose, structured by topic. Single voice. Shorter than any single input.]

### Consensus Findings
[Claims all sources agree on — with evidence type noted]

### Adjudication Table

| Contested Claim | Positions | Verdict | Test Used | Confidence | Reasoning |
|----------------|-----------|---------|-----------|------------|-----------|
| [claim] | A: [position], B: [position] | Resolved: A | Logic | High | [why] |

### Unique Insights
[Claims only one source raised — with independent evidence assessment]

### Emergent Findings
1. Source A's [X] + Source B's [Y] → [Z], which neither stated.

### Remaining Unknowns
[What can't be resolved from these sources — what evidence is needed]
```

## Calibration

**GOOD adjudication:**
"CONTESTED: Whether the market is growing or stagnating. Source A cites 12% CAGR from IDC 2025. Source B says 'market is mature.' Logic test: inconclusive (different claims). Evidence test: Source A provides specific, dated, third-party data. Source B provides no citation. VERDICT: Resolved — Source A. Test: Evidence. Confidence: High."

**BAD adjudication:**
"Both sources make good points about the market. The truth is probably somewhere in between."
*No test applied. No verdict. "Somewhere in between" is abdication.*

**GOOD emergent finding:**
"Source A's finding that enterprise sales cycles average 14 months combined with Source B's evidence that the startup has 18 months of runway implies a maximum of one full sales cycle before needing to raise again, which neither source stated."

**BAD emergent finding:**
"Both sources emphasise the importance of execution, suggesting that execution is key."
*Not emergent — just a vague theme. No specific source references. No template filled.*

## Self-Check

- [ ] Every contested claim has a verdict with named test
- [ ] Unified view reads as single voice (no "Source A says...")
- [ ] Unified view is shorter than any single input
- [ ] Emergent findings follow the template (Source A's X + Source B's Y → Z)
- [ ] Remaining unknowns are specific, not vague

## Hand-Off

Feeds into: **Assumptions** (dig into the unified view), **Stress Test** (attack it), **Distill** (compress it).
