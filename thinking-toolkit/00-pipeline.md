# The Thinking Toolkit — Pipeline Map v1

## What This Is

Six prompts that chain together to process information, find structure, test ideas, and produce decisions. Each prompt does one job. No overlap. Explicit hand-offs.

## The Six Prompts

| # | Prompt | Job | Input | Output |
|---|--------|-----|-------|--------|
| 01 | **Extractor** | Map the structure | Raw mess of any kind | Idea tree with dependencies and gaps |
| 02 | **Root Finder** | Find what's hidden | Structured ideas | Assumption register, driver map, logic chains |
| 03 | **Challenger** | Break it | Any idea or plan | Stress test with verdicts (survives/wounded/fatal) |
| 04 | **Synthesizer** | Fuse multiple sources | 2+ sources on same topic | Unified view with adjudicated disagreements |
| 05 | **Evolver** | Generate better options | Idea + its weaknesses | Ranked alternatives with recommendation |
| 06 | **Distiller** | Compress to decision | Any analysis output | Four levels: brief → summary → pitch → one-liner |

## Common Workflows

### "I have a messy pile of notes and need to make sense of it"
```
Notes → EXTRACTOR → ROOT FINDER → DISTILLER
```

### "I have a business idea and need to know if it's good"
```
Idea → EXTRACTOR → ROOT FINDER → CHALLENGER → DISTILLER
```

### "I have a business idea and need to make it better"
```
Idea → EXTRACTOR → ROOT FINDER → CHALLENGER → EVOLVER → CHALLENGER (again) → DISTILLER
```

### "I queried 4 AI models and need one answer"
```
4 responses → SYNTHESIZER → ROOT FINDER → DISTILLER
```
See **Multi-Model Workflow** section below for the exact prompts and formatting.

### "I have research from multiple sources and need a strategy"
```
Sources → SYNTHESIZER → EXTRACTOR → ROOT FINDER → CHALLENGER → EVOLVER → DISTILLER
```

### "I need to choose between Option A and Option B"
```
Both options → EXTRACTOR (on each) → CHALLENGER (on each) → EVOLVER (with both as inputs) → DISTILLER (Decision mode)
```

### "I need to deeply understand a complex document"
```
Document → EXTRACTOR → ROOT FINDER → DISTILLER
```

### "I need to iterate on a plan through multiple rounds"
```
Plan → EXTRACTOR → CHALLENGER → EVOLVER → [take Evolver's recommended option] → CHALLENGER → EVOLVER → ... → DISTILLER
```
The Evolver's "Evolution Directive" output is designed for this loop. Each round feeds back with a new baseline and a focused mutation target.

## Rules of Thumb

**Start with the Extractor** when your input is messy, long, or comes from your own head. You need structure before analysis.

**Start with the Synthesizer** when you have multiple sources on the same topic. Get to one view first, then analyse it.

**Start with the Challenger** when you already have a clear, structured idea and just need to know if it holds up.

**Start with the Root Finder** when you have a structured plan but feel like something is off and can't name what.

**Skip the Extractor** when your input is already well-structured (a formal business plan, a clear argument with stated premises).

**Skip the Synthesizer** when you only have one source.

**Always end with the Distiller** when the output goes to a decision-maker (including yourself). Analysis that doesn't compress to a clear recommendation is analysis that isn't finished.

## Using These Prompts

### Portable (any LLM)
Paste the prompt at the start of a conversation, then paste your input material after it. For chains, start a new conversation for each prompt and paste the previous output as the new input.

### Claude Skills (if using Cowork/Claude Code)
Each prompt can be installed as a skill. The hand-off instructions at the bottom of each prompt tell you which skill to invoke next.

## Multi-Model Workflow (Detailed)

This is the exact process for querying multiple AI models and synthesising their responses.

### Step 1: Craft Your Research Prompt

Write one clear research prompt. Use this template:

```
I need a thorough analysis of [TOPIC].

Specifically address:
1. [Key question 1]
2. [Key question 2]
3. [Key question 3]

For each point:
- State your position clearly
- Cite specific evidence, data, or examples (not vague assertions)
- Flag where you're uncertain vs. confident
- Note any important caveats or counterarguments

Be direct. Take positions. Don't hedge.
```

### Step 2: Send to 3-4 Models

Send the identical prompt to each model. Recommended set: Claude, GPT-4, Gemini, Grok. Use whichever you have access to — 3 is the minimum for useful synthesis, 4+ adds diminishing returns.

### Step 3: Format for the Synthesizer

Paste each response into the Synthesizer conversation using this exact format:

```
=== SOURCE: [Model Name] ===

[Paste full response here]

=== END SOURCE ===

=== SOURCE: [Model Name] ===

[Paste full response here]

=== END SOURCE ===

(repeat for each model)
```

Then add the Synthesizer prompt ABOVE the sources. The Synthesizer will extract claims, adjudicate disagreements, and produce a unified view.

### Step 4: Continue the Pipeline

Feed the Synthesizer output to Root Finder, Challenger, or Distiller depending on your goal.

### When This Is Worth Doing

**Worth it**: Strategic decisions, business model evaluation, complex research questions where you're not sure of the answer, high-stakes analysis where you need confidence.

**Not worth it**: Factual lookups, coding questions, creative tasks, anything where one model's answer is obviously sufficient.

## When To Stop Iterating

If you're in a Challenger → Evolver → Challenger loop, stop when ANY of these are true:

**You've converged**: The Evolver's recommended option survives all Challenger attacks. You're done — go to Distiller.

**You've hit diminishing returns**: Round N's recommended option isn't meaningfully better than Round N-1's. Two rounds with no improvement means the problem is input quality, not iteration count. Go back to research or Root Finder.

**You've found a fatal flaw with no fix**: If the Challenger returns FATAL verdicts that the Evolver can't address across two attempts, the idea may be genuinely unviable. Distill what you've learned and start from a different premise.

**You're out of time**: Most decisions have deadlines. After 2-3 rounds, you have enough signal to decide. Perfect is the enemy of shipped.

**Rule of thumb**: 2 rounds is typical. 3 rounds is thorough. More than 3 rounds usually means you're avoiding the decision, not improving the analysis.

## Troubleshooting

**"The Extractor output is a mess"**: Your input was probably too unstructured. Try writing 5-10 bullet points summarising your key ideas BEFORE running Extractor. It maps structure — it can't create structure from stream-of-consciousness.

**"The Challenger attacks feel generic"**: Run Root Finder first. Challenger is much sharper when it has specific assumptions to target rather than finding its own.

**"The Evolver alternatives all look similar"**: Check if it changed 2+ components per alternative. If not, re-run with the instruction: "The current alternatives are too similar. Use INVERT and LEAPFROG operators. Change at least 3 components per alternative."

**"The Synthesizer hedges everything"**: Your sources probably all said similar things in different words. If there's no real disagreement, skip Synthesizer and go straight to Extractor on the best single source.

**"The Distiller can't compress to a one-liner"**: The analysis isn't finished. If the core argument doesn't reduce to one sentence, the spine isn't clear yet. Go back to Root Finder.

## Design Principles

**One job per prompt.** The Extractor doesn't evaluate. The Challenger doesn't fix. The Evolver doesn't compress. This prevents any single prompt from trying to do everything and doing nothing well.

**Concrete methods over abstract frameworks.** Every prompt specifies HOW to do the analysis, not just what categories to fill in. "Ask these questions in order" beats "consider the epistemological foundations."

**Evidence over scoring.** No numerical confidence scores that LLMs hallucinate. Assessments are expressed as verdicts (SURVIVES/WOUNDED/FATAL), ratings (Strong/Adequate/Weak), or plain-language justifications. The reasoning IS the assessment.

**Explicit hand-offs.** Every prompt says what feeds into it and what it feeds into. The pipeline is visible, not implied.

**Compression is a first-class operation.** The Distiller isn't an afterthought — it's how you know your analysis actually holds together. If you can't compress it to a one-liner, you don't understand it yet.
