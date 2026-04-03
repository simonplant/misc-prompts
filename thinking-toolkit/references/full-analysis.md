# Full Analysis
*Run the complete pipeline in one pass — from raw input to decision-ready output.*

## When To Use

Use this when you want Structure → Assumptions → Stress Test → Evolve → Distill in a single conversation. Faster than individual tools but slightly less depth per stage.

**Use individual tools instead** when: you need maximum depth at one stage, you're doing multi-model synthesis, or you want multiple Stress Test → Evolve rounds.

## Process

Execute five stages in order. Each builds on the previous. **Keep each stage lean** — depth comes from the chain, not from any stage being exhaustive.

### Stage 1: Structure
- Idea tree: Level 0 → Level 1 → Level 2 with dependencies
- Separate ideas from context
- Gaps: missing, contradictory, imbalanced
- 3 questions about what's hiding beneath

**Target**: Tree + gaps + 3 questions. No more.

### Stage 2: Assumptions
- Assumption register: 3-5 hidden assumptions with blast radius + test method
- Driver map: 2-3 most important claims traced surface → functional → root
- Logic chain: core argument's reasoning with gap flags
- Cluster check: which assumptions cascade together (flag any whose failure takes 2+ others with it)
- Silence check: what's conspicuously absent

**Target**: Register + cluster vulnerabilities + driver map + 2-paragraph plain-language summary.

### Stage 3: Stress Test
- 3-4 strongest attacks, each with: TARGET → ATTACK (mechanism + precedent) → DEFENCE (strength rating) → VERDICT
- WOUNDED verdicts specify WHAT/HOW/WHEN
- Cascade analysis: which attacks combine dangerously
- Steelman: conditions for success

**Target**: 3-4 attacks + cascade + steelman. Don't mount more than 4 — deep, not wide.

### Stage 4: Evolve
- 3-4 genuinely different alternatives addressing WOUNDED/FATAL findings
- Each: name, concept (2-3 sentences), mutations applied, which weakness it fixes
- Comparative assessment: Strong/Adequate/Weak on 6 dimensions
- Clear recommendation: primary, fallback, kill list

**Rules**: Every alternative changes ≥ 2 components. ≥ 1 uses INVERT or LEAPFROG.

### Stage 5: Distill
- **Level 4**: Single most important finding (one sentence)
- **Level 3**: 3-4 sentences — insight, evidence, risk, next step
- **Level 2**: One paragraph, ~150 words, with evidence
- **Level 1**: 800-1,200 words — Situation, Key Findings, Tensions & Risks, Recommendation, What We Still Don't Know

## Output

```
# Analysis: [Title]

## 1. Structure
### Idea Tree
[tree with dependencies]
### Background Context
[facts, not claims]
### Gaps
[missing foundations, contradictions, imbalances]
### Questions for Deeper Analysis
1-3 questions

## 2. Root Analysis
### Assumption Register
| # | Assumption | Stated/Hidden | Blast Radius | Test Method |
### Driver Map
[2-3 claims: surface → functional → root]
### What This Is Really About
[2 paragraphs plain language]

## 3. Stress Test
### Attack 1-4: [Name]
Target / Attack / Defence / Verdict
### Cascade Analysis
### Steelman
### Scorecard
Survived: [N] | Wounded: [N] | Fatal: [N]

## 4. Evolution
### Alternatives 1-4
Name / Concept / Mutations / Fixes
### Comparative Assessment
[6-dimension table]
### Recommendation
Primary / Fallback / Kill list

## 5. Decision Ready
### One-Liner
### Elevator Pitch
### Executive Summary
### Full Brief
Situation / Key Findings / Tensions & Risks / Recommendation / What We Still Don't Know
```

## Self-Check

- [ ] Stage 1 separates ideas from context and maps dependencies
- [ ] Stage 2 has ≥ 3 hidden assumptions with test methods
- [ ] Stage 3 has ≥ 3 attacks with specific mechanisms and precedents
- [ ] Stage 3 WOUNDED verdicts specify WHAT/HOW/WHEN
- [ ] Stage 4 has ≥ 3 alternatives, each changing ≥ 2 components, ≥ 1 radical
- [ ] Stage 4 makes a clear recommendation
- [ ] Stage 5 Level 4 captures the most important finding, not a generic summary
- [ ] Stage 5 preserves risks through Level 3
- [ ] Full document tells a coherent story from structure to decision
