# Structure
*Extract the structural skeleton — ideas, dependencies, and gaps.*

## Job

Take messy input and produce a clean map of what's being said. No judgment, no improvement — just structure. Separate IDEAS (claims about what should be done or is true) from CONTEXT (background facts, market data, definitions).

## Process

### 1. Extract distinct ideas
State each claim/proposal/assertion in one clear sentence. Tag source: `(Source A, Section 2)`. Note if explicitly stated or inferred. Deduplicate: same thing in different words → list once, note both sources. Almost the same with meaningful difference → list both, flag divergence.

### 2. Map dependencies
For every idea: What does it depend on? What depends on it? Is it a root idea (depends on nothing) or derived?

### 3. Build hierarchy
- **Level 0 — Foundational Claims**: Root ideas everything builds on
- **Level 1 — Core Framework**: Main structural ideas
- **Level 2 — Supporting Detail**: Evidence, flesh on the framework
- **Level 3 — Specifics**: Implementation details, examples, data

Use indentation. Mark dependencies with `→ depends on (N)`.

### 4. Find gaps
- **MISSING FOUNDATION**: Level 1-3 ideas assuming something at a lower level that was never stated
- **ORPHAN**: Ideas that don't connect to anything else
- **CONTRADICTION**: Two ideas in the tree that conflict
- **IMBALANCE**: Branches heavily developed vs. skeletal

## Output

```
## Structural Map: [Title]

### Source Summary
(skip if single source)

### Idea Tree
0. [Foundational claim]
   1. [Core idea] → depends on (0)
      2. [Supporting detail] → depends on (1)

### Cross-Branch Dependencies
- [Idea X at Branch A] ←→ [Idea Y at Branch B]: [connection]

### Gaps & Tensions
- MISSING FOUNDATION: [assumed but never stated]
- ORPHAN: [connects to nothing]
- CONTRADICTION: [X] vs [Y]
- IMBALANCE: [Branch A: 15 ideas, Branch B: 2]

### Source Agreement Map
(if multi-source)
- CONSENSUS: [ideas all sources agree on]
- DIVERGENCE: [where they disagree — state each position]
- UNIQUE: [only one source raised this]
```

## Calibration

**GOOD** (input: "We're building an AI meeting summariser as a Slack plugin"):
```
0. Users need actionable meeting summaries, not transcripts
   1. Slack is where work conversations happen → depends on (0)
      2. Plugin distribution gives access to existing teams → depends on (1)
   1. Our AI produces structured summaries, not raw transcription → depends on (0)
      2. Action items extracted and assigned automatically → depends on (1)

Background Context: Slack has 750K+ paying orgs. Meeting fatigue is a documented trend.
```

**BAD** (same input):
```
0. Slack is popular
0. AI is advancing rapidly
0. Meetings are bad
   1. People want meeting summaries
```
*"Slack is popular" and "AI is advancing" are context, not ideas. "Meetings are bad" is vague. No dependencies. No ideas-vs-context separation.*

## Guardrails

- Don't evaluate whether ideas are good or bad — that's for other tools
- Don't add your own ideas or suggest improvements
- Don't rewrite the user's language beyond making it clear

## Self-Check

- [ ] Tree depth ≥ 2 levels
- [ ] Every Level 1+ idea has a dependency arrow
- [ ] Ideas and context in separate sections
- [ ] No two tree entries say the same thing differently
- [ ] Gaps section has ≥ 1 entry
- [ ] Questions for Assumptions has ≥ 3 entries

## Hand-Off

Add 3-5 questions pointing the next tool toward hidden assumptions:
```
### Questions for Assumptions
1. [Why does the plan assume X? What must be true?]
2. [The dependency between Y and Z is asserted but not evidenced — what's real?]
3. [This gap suggests an unstated assumption about — what?]
```

Feeds into: **Assumptions** (find what's hidden), **Synthesize** (if multi-source), **Stress Test** (if already well-structured).
