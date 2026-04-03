---
name: thinking-toolkit
description: "Strategic analysis tools for structuring ideas, finding hidden assumptions, stress-testing plans, synthesizing multi-source data, evolving alternatives, and compressing analysis to decisions. TRIGGERS: analyze/evaluate/stress-test a business idea, plan, or strategy; synthesize research from multiple sources; find hidden assumptions; generate alternatives; compress analysis to a decision; 'what am I missing'; 'is this idea good'; 'tear this apart'; 'help me think through this'; 'what should I do'; root cause analysis; adversarial testing; decision distillation; multi-model synthesis."
---

# Thinking Toolkit

Seven analysis tools, one multi-model workflow, and one full-analysis chain. Each tool does one job. They chain via hand-off sections.

## Tool Reference

| Tool | File | Job |
|------|------|-----|
| **Structure** | `references/structure.md` | Extract idea tree, dependencies, gaps from messy input |
| **Assumptions** | `references/assumptions.md` | Find hidden assumptions, root drivers, logic chain gaps |
| **Stress Test** | `references/stress-test.md` | Adversarial attacks with verdicts, cascades, steelman |
| **Synthesize** | `references/synthesize.md` | Fuse 2+ sources: classify claims, adjudicate conflicts |
| **Evolve** | `references/evolve.md` | Generate alternatives via 6 mutation operators |
| **Distill** | `references/distill.md` | Compress to 4 levels: one-liner → full brief |
| **Business Model** | `references/business-model.md` | End-to-end business model analysis (6-bone skeleton) |
| **Peer Review** | `references/peer-review.md` | Multi-model research collection + ranking workflow |
| **Full Analysis** | `references/full-analysis.md` | All 5 stages in one pass with depth constraints |

## Routing

**Read the relevant tool file and follow its instructions exactly.** The calibration examples and output formats are the value — don't improvise.

### Entry points

- **"Analyze this idea/plan/strategy"** → Structure → Assumptions → Stress Test → Distill
- **"Make this better"** → Structure → Assumptions → Stress Test → Evolve → Stress Test again → Distill
- **"What am I missing?"** → Assumptions → Distill
- **"Is this viable?"** → Stress Test → Distill
- **"I have multiple sources/responses"** → Synthesize → Assumptions → Distill
- **"Just give me the summary"** → Distill only
- **"Tear this apart"** → Stress Test only (or Structure → Stress Test for unstructured input)
- **"Evaluate this business model"** → Business Model (self-contained)
- **"Run the full pipeline"** → Full Analysis

### Iteration

Stress Test → Evolve → Stress Test can loop. Stop when: the recommended option survives all attacks, or round N isn't meaningfully better than N-1. Typical: 2 rounds. Max: 3. More is procrastination.

### Rules

1. Follow tool instructions exactly — the specificity is the value
2. Run self-checks before delivering
3. Use hand-off sections to accelerate the next tool
4. Ask before long chains (4+ tools): offer Full Analysis as alternative
