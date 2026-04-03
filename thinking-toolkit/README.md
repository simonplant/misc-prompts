# Thinking Toolkit

A set of analysis tools for Claude Code that take messy ideas, plans, and strategies and produce decision-ready output. Each tool does one job well. They chain together for deeper analysis.

---

## Quick Start

The toolkit activates automatically in Claude Code when you say things like:

- "Analyze this business idea"
- "What am I missing?"
- "Tear this apart"
- "Help me think through this"
- "Is this viable?"
- "I have responses from multiple AI models — synthesize them"

You can also invoke it directly: `/thinking-toolkit`

---

## The Tools

### Core Analysis Tools

These six tools form the analysis backbone. Each can run standalone or chain into the next.

#### Structure

**What it does**: Takes messy input — notes, documents, brainstorms, research — and extracts a clean structural map. Ideas separated from background context, organized into a dependency tree, with gaps identified.

**When to use**: Your input is unstructured or you need to see what's actually being said before analyzing it.

**Key output**:
- Idea tree with four levels (foundational claims → core framework → supporting detail → specifics)
- Dependency arrows showing what rests on what
- Gap detection: missing foundations, orphan ideas, contradictions, density imbalances
- Source agreement map (when working with multiple inputs)

**Example prompt**: "Here are my rough notes on a product idea. Structure this so I can see what I'm actually proposing."

---

#### Assumptions

**What it does**: Digs beneath structured ideas to find what's hidden — unstated assumptions, real drivers behind surface claims, logic chain gaps, and interconnected vulnerability clusters.

**When to use**: You have a clear plan or argument and want to know what it's really standing on.

**Key techniques**:

- **Assumption excavation**: For every major claim, asks: what must be true? Which preconditions are unstated? How testable? What's the blast radius if wrong?

- **3-layer driver analysis**: Traces each theme from surface reason → functional reason → root reason, stopping at bedrock (self-evident truth, article of faith, or testable fact). Prevents lazy single-layer answers.

- **Logic chain mapping**: Traces argumentative logic (`Premise A + Premise B → Conclusion C`) and flags each link as Valid, Unsupported Leap, Hidden Premise, or Non Sequitur.

- **Cluster check**: Tests whether assumptions reinforce or undermine each other as a system. Identifies cascade vulnerabilities where one failure takes others with it.

- **Silence check**: Scans for what's conspicuously absent — missing perspectives, excluded framings, ignored stakeholders.

- **Power and incentive mapping** (optional): Who benefits from the current framing? What evidence-based incentives are shaping the argument? Constrained to evidence only — no speculation about hidden motives.

**Key output**: Assumption register (table with blast radius and test methods), cluster vulnerabilities, driver map, logic chain with gap flags, root vulnerabilities ranked by blast radius, plain-language summary.

**Example prompt**: "I've got a structured plan for entering the European market. What assumptions am I standing on?"

---

#### Stress Test

**What it does**: Mounts the strongest possible adversarial attacks against an idea, provides the strongest possible defence for each, and produces clear verdicts. Then builds the steelman — the strongest surviving version.

**When to use**: You need to know where something breaks before committing to it.

**Key techniques**:

- **Attack prioritization**: Searches in order — load-bearing assumptions first, then single points of failure, then market/timing risks, then execution risks. Skips peripheral details.

- **Debate protocol**: Each attack follows a structured format: thesis ("this fails because..."), evidence, failure scenario, and a real-world precedent (specific company or event).

- **Three-tier verdicts**:
  - **SURVIVES**: Defence holds. Risk to monitor, not fix.
  - **WOUNDED**: Defence is partial. Includes a specific repair condition on three dimensions — WHAT must change, HOW, and by WHEN. Example: "Survives IF GTM pivots to SMB-first [WHAT] with self-serve onboarding [HOW] within 90 days [WHEN]."
  - **FATAL**: No adequate defence exists.

- **Cascade analysis**: Checks whether 2-3 attacks landing simultaneously produce worse combined effects, or whether multiple WOUNDED verdicts combine into something FATAL.

- **Steelman construction**: Builds the strongest surviving version using only original material. States explicit conditions for success.

**Key output**: Attack surface summary, full attack/defence/verdict for each, cascade analysis, steelman, summary scorecard (survived/wounded/fatal counts).

**Example prompt**: "Stress-test this product strategy. I want to know what kills it."

---

#### Synthesize

**What it does**: Takes 2+ sources on the same topic and fuses them into a single unified document, adjudicating disagreements based on evidence quality rather than just averaging opinions.

**When to use**: You have responses from multiple AI models, competing analyses, or several research documents on the same question.

**Key techniques**:

- **Claim classification**: Every claim is categorized as CONSENSUS (genuine agreement on substance), CONTESTED (active disagreement), or UNIQUE (only one source raises this). Includes a critical distinction: two sources saying the same thing in different words with different rigour levels are CONVERGENT, not consensus.

- **4-test adjudication hierarchy** (applied in priority order, stops at first clear winner):
  1. **Logic test**: If one position has a logical gap or internal contradiction, the other wins — even with less evidence
  2. **Evidence test**: Specific data beats general assertions; primary beats secondary; recent beats dated
  3. **Explanatory power test**: Which explains more facts with fewer assumptions?
  4. **Convergence test** (tiebreaker only): Majority agreement, but one well-evidenced minority view outweighs unsupported majority

- **Emergent findings**: Insights visible only in combination. Must meet a strict template: "Source A's finding that [X] combined with Source B's evidence for [Y] implies [Z], which neither source stated." If you can't fill the template, it's speculation.

- **Verdict types**: Resolved (with confidence level), Genuinely Uncertain (with what evidence would settle it), or False Dichotomy (disagreement dissolves under reframing).

**Key output**: Unified view (single voice, shorter than any single input), consensus findings, adjudication table, unique insights, emergent findings, remaining unknowns.

**Example prompt**: "I asked Claude, GPT-4, and Gemini about our market positioning. Here are all three responses — synthesize them."

---

#### Evolve

**What it does**: Takes an idea that's been analyzed and generates genuinely different alternatives that address its weaknesses, then compares all options and makes a clear recommendation.

**When to use**: After stress-testing reveals wounds or fatal flaws, or when you want to explore the solution space before committing.

**Key techniques**:

- **Decomposition**: Breaks the input into independently changeable components (for business models: customer, problem, delivery, revenue, moat, growth).

- **Six mutation operators**:
  - **SWAP**: Replace one component entirely
  - **INVERT**: Flip a core assumption — if original assumes "customers want X," what if they want the opposite?
  - **TRANSPLANT**: Apply the core insight to a completely different domain
  - **COMBINE**: Merge strongest elements of two approaches
  - **SUBTRACT**: Remove the most complex/expensive component — what's the simplest version?
  - **LEAPFROG**: Start from scratch with the same goal but no existing assumptions

- **Minimum difference threshold**: Every alternative must change ≥ 2 components (changing only pricing is a variation, not an alternative). At least one alternative must use INVERT or LEAPFROG to force a radical option.

- **Comparative assessment**: Original + all alternatives rated Strong/Adequate/Weak across six dimensions (solves the problem, defensible, executable, scalable, resilient, upside) with one-sentence justifications per cell.

**Key output**: Original decomposition, alternatives with mutations listed, comparative assessment table with justifications, recommendation (primary + fallback + hybrid opportunity + kill list), evolution directive for iterative use.

**Example prompt**: "The stress test found two fatal flaws. Generate alternatives that fix them."

---

#### Distill

**What it does**: Compresses any analysis to the level of detail the decision requires. Four compression levels, each preserving the logical spine while cutting padding.

**When to use**: As the final step in any analysis chain, or standalone when you need to compress a long document.

**The four levels**:

| Level | Name | Size | What it contains |
|-------|------|------|-----------------|
| **4** | The One-Liner | 1 sentence | The single most important finding |
| **3** | The Elevator Pitch | 3-4 sentences | Key insight + evidence + risk + next step |
| **2** | The Executive Summary | ~150 words | Complete logic chain in one paragraph |
| **1** | The Full Brief | 800-1,200 words | Situation, findings, risks, recommendation, unknowns |

**Key techniques**:

- **Spine identification**: Before compressing, identifies the minimal reasoning chain (core claim + strongest evidence + recommendation + biggest risk). The spine survives at every level.

- **Triage**: Supporting material sorted into essential context, important nuance, supporting evidence, caveats, and process artifacts — each with a clear cut point.

- **Risk preservation**: Risks must survive to Level 3. If they disappear during compression, they get added back.

- **Decision Frame** (special mode): When input contains a comparison, adds: the choice, the tiebreaker, value-based recommendations, a direct call, and an irreversibility check.

**Example prompt**: "Distill this entire analysis. I need all four levels."

---

### Specialized Tools

#### Business Model Analysis

**What it does**: End-to-end business model evaluation in a single tool. Decomposes using the 6-bone skeleton, finds hidden assumptions per bone, stress-tests the weakest bones, and compresses to four levels.

**When to use**: Evaluating a business model, startup pitch, or business plan.

**The 6-bone skeleton**:

| Bone | Key questions |
|------|--------------|
| **Problem-Customer Lock** | What pain? Who has it badly enough to pay? Why these two matched? |
| **Value Proposition** | What outcome? Why better than alternatives? Why credible? |
| **Revenue Engine** | Pricing model? Unit economics (CAC vs LTV)? The equation that must be true? |
| **Moat** | Type (network effects, switching costs, IP, etc.)? Depth (replication time)? Compounding direction? |
| **Growth Mechanism** | Acquisition channels? Retention mechanics? Expansion? Network dynamics? |
| **Execution Requirements** | Critical capabilities? Resource bottleneck? What breaks at 10x? |

**Process**:

1. **Viability quick-check**: Rate each bone Clear / Fuzzy / Missing. This determines routing — 3+ Missing means you're still in ideation; 3+ Clear means go straight to stress test; mixed means dig into the Fuzzy bones first.

2. **Assumption dig**: For each weak bone, find what's hidden.

3. **Stress test**: Attack each bone with business-model-specific attacks (moat attacks, unit economics attacks, customer lock attacks, timing attacks).

4. **Distill**: Compress using the business model frame. Level 4 becomes: "This works if [single most important assumption] is true."

**Example prompt**: "Here's our pitch deck. Run a full business model analysis."

---

#### Peer Review Workflow

**What it does**: A structured protocol for collecting research from multiple AI models, running anonymous peer review across them, and synthesizing the results with ranking data.

**When to use**: High-stakes decisions, irreversible choices, or situations where you want quantitative validation across multiple AI models.

**The protocol** (4 rounds):

1. **Collect**: Submit your question to 3-4 AI models (Claude, GPT-4, Gemini, Grok). Save each response.

2. **Peer review**: Send all responses (anonymized as Response A/B/C/D) back to each model with a ranking prompt. Randomize which response is A/B/C/D each time so models can't identify their own output.

3. **Extract rankings**: Build a table of how each model ranked each response. Calculate averages. Identify consensus picks (ranked top by ≥75% of reviewers), controversial positions (ranked #1 by some, #4 by others), and rejected positions.

4. **Synthesize**: Feed everything to the Synthesize tool with peer ranking data as an additional signal. Mine the peer rationales for specific evidence challenges, reasoning flaws, and unique insights.

**Decision guide**:
- Can't undo it? → Use peer review
- Client will see it? → Use peer review
- Just exploring? → Skip it
- Models disagree? → Strongly consider it

**Example prompt**: "I collected responses from four AI models and ran peer review. Here are the responses, rankings, and rationales — synthesize with peer data."

---

### Full Analysis

**What it does**: Runs the complete pipeline — Structure → Assumptions → Stress Test → Evolve → Distill — in a single pass with depth constraints per stage.

**When to use**: You want a complete analysis of an idea, plan, or strategy in one conversation without manually chaining tools.

**When to use individual tools instead**: When you need maximum depth at one stage, when you're doing multi-model synthesis, or when you want multiple rounds of Stress Test → Evolve iteration.

**Depth targets per stage**:

| Stage | Produces | Constraint |
|-------|----------|-----------|
| 1. Structure | Idea tree + gaps + 3 questions | Tree + gaps only, no analysis |
| 2. Assumptions | Register + cluster vulnerabilities + driver map + 2-paragraph summary | 3-5 assumptions, 2-3 driver maps |
| 3. Stress Test | 3-4 attacks + cascade + steelman | No more than 4 attacks — deep, not wide |
| 4. Evolve | 3-4 alternatives + comparative table + recommendation | ≥ 2 components changed each, ≥ 1 radical |
| 5. Distill | All four compression levels | One-liner captures THE finding, risks survive to Level 3 |

**Example prompt**: "Run a full analysis on this product strategy."

---

## Workflows

These are the most common ways to use the toolkit, with step-by-step guidance.

### 1. "Is this idea any good?"

The most common use case. You have a business idea, product concept, or strategy and want an honest assessment.

**Quick version** — paste your idea and say:

> "Run a full analysis on this."

This triggers Full Analysis, which runs all five stages automatically. You'll get a complete document from structure through to a decision-ready recommendation.

**Deep version** — when the stakes are high enough for maximum depth:

> **Step 1**: Paste your idea/notes/pitch and say: "Structure this."
> You'll get an idea tree showing what you're actually proposing, with gaps flagged.
>
> **Step 2**: "Now find the hidden assumptions."
> You'll get an assumption register with blast radius and test methods — the things that must be true for this to work.
>
> **Step 3**: "Stress-test this."
> You'll get 3-5 attacks with verdicts. Pay attention to WOUNDED verdicts — the conditions tell you exactly what needs to change.
>
> **Step 4**: "Distill this to all four levels."
> You'll get the one-liner, elevator pitch, executive summary, and full brief.

**For business models specifically**: Say "Evaluate this business model" to trigger the Business Model tool, which runs the 6-bone skeleton analysis in a single pass.

**What to paste**: Anything works — rough notes, a pitch deck summary, a strategy doc, even a rambling voice-note transcript. Structure will sort it out.

**How to read the output**: Start from the bottom. Level 4 (the one-liner) tells you the core truth. Level 3 adds the key risk. Work upward for more detail. The stress test scorecard (survived/wounded/fatal) is your viability signal.

---

### 2. "Make this better" (iterative improvement)

You have something that's OK but not great — a strategy with known gaps, a plan that survived initial scrutiny but feels vulnerable, a product concept that needs refinement.

**The loop**:

> **Step 1**: "Stress-test this plan."
> The stress test produces verdicts. WOUNDED items have specific repair conditions (WHAT/HOW/WHEN). FATAL items need fundamental rethinking.
>
> **Step 2**: "The stress test found [N] wounds and [N] fatals. Evolve alternatives that fix them."
> Evolve generates 4-6 alternatives using mutation operators. Each one explicitly addresses a weakness. The comparative table shows trade-offs.
>
> **Step 3**: "Stress-test the recommended alternative."
> On re-entry, the stress test explicitly checks: did the evolution fix the original wounds, or introduce new ones?
>
> **Repeat** if needed. Stop when the recommendation survives all attacks, or when a round isn't meaningfully better than the previous one.

**What makes this powerful**: The hand-offs between tools are typed. Stress Test produces specific "Mutation Targets for Evolve" (e.g., "SWAP competitive advantage from data moat to integration switching costs"). Evolve produces an "Evolution Directive" with the remaining weakness and next mutation focus. Each round starts from where the last one left off, not from scratch.

**When to stop**: 2 rounds is typical. 3 is thorough. More than 3 means you're optimizing rather than deciding — pick the best option and commit.

---

### 3. "Help me decide" (choosing between options)

You have 2-3 options and need to pick one. Could be product directions, strategic approaches, vendor choices, architecture decisions, or anything where you're weighing trade-offs.

**If you already have the options clearly defined:**

> "I'm choosing between [Option A] and [Option B]. Here's what I know about each: [details]. Stress-test both and distill with a decision frame."

The stress test runs on each option. Distill's **Decision Frame** mode produces:
- The choice and the tiebreaker (single factor that separates them)
- Value-based recommendations ("If you value X, choose A because...")
- A direct call with reasoning
- An irreversibility check (can you undo this if wrong? What's the switching cost?)

**If your options are fuzzy or you're not sure you've considered all of them:**

> **Step 1**: "Here's my current plan: [details]. Evolve alternatives."
> Evolve generates 4-6 genuinely different options, including at least one radical alternative (INVERT or LEAPFROG). You might discover options you hadn't considered.
>
> **Step 2**: "Stress-test the top 2-3 options."
> Side-by-side verdicts show which survives better and where each is vulnerable.
>
> **Step 3**: "Distill with a decision frame."
> Forces a direct call, not "it depends."

**Key insight**: The Decision Frame's irreversibility check is often the most valuable output. A slightly worse option that's reversible may beat a slightly better option that locks you in.

---

### 4. "What am I missing?" (blind spot detection)

You're mid-project, already committed, and want to know what you're not seeing. Different from "is this idea good" because you're not evaluating from scratch — you're stress-testing something in flight.

**Quick version:**

> "Here's my current plan/strategy/approach: [details]. What am I missing?"

This triggers Assumptions, which digs for unstated assumptions, cluster vulnerabilities (where one failure cascades), and strategic silences (what's conspicuously absent).

**Deep version:**

> **Step 1**: "Find the hidden assumptions in this plan."
> Focus on the assumption register — especially Hidden + High Blast Radius items. These are the things that could hurt you.
>
> **Step 2**: "Which of these assumptions should I be most worried about?"
> The Root Vulnerabilities section ranks by blast radius. The cluster check shows which assumptions cascade together.
>
> **Step 3** (optional): "Stress-test the top 3 vulnerabilities."
> Targeted stress testing on the specific weaknesses, not the whole plan.

**What to watch for in the output**:
- **Cluster vulnerabilities**: If assumptions #2, #4, and #5 form a cluster where one failure takes the others, that's your biggest risk — even if each individually seems moderate.
- **Strategic silences**: What stakeholders, competitors, or failure modes are never mentioned in your plan? Absence is a signal.
- **Articles of faith**: Assumptions marked "not testable" are the ones you're taking on trust. Make sure you know which ones they are.

**When this is most valuable**: Right before a major commitment — launching, hiring, raising money, signing a contract. The cost of pausing to check is low; the cost of a hidden assumption exploding is high.

---

### 5. "Synthesize these AI responses"

You asked the same question to multiple AI models and want one unified answer.

**Basic version:**

> "Here are responses from Claude, GPT-4, and Gemini on [topic]. Synthesize them."

The Synthesize tool classifies every claim as consensus, contested, or unique, adjudicates disagreements using the 4-test hierarchy, and produces a unified view in a single voice.

**High-stakes version** (using Peer Review):

> **Step 1**: Collect responses from 3-4 AI models.
>
> **Step 2**: Send all responses (anonymized) back to each model for ranking. The peer-review.md file has the exact prompt to use.
>
> **Step 3**: Paste the original responses, rankings, and rationales into Claude: "Synthesize with peer review data."

The peer review adds quantitative validation: consensus picks (ranked top by ≥75% of reviewers), controversial positions, and rejected positions. Mining the rationales often surfaces evidence challenges and reasoning flaws that the original responses didn't catch.

**When to use basic vs. peer review:**
- Routine research question → basic
- Irreversible decision → peer review
- Significant disagreement between models → peer review
- Client deliverable → peer review
- Time-sensitive → basic

---

### 6. "Organize my thinking"

You have scattered notes, a long conversation transcript, research from multiple places, or a brain dump that needs structure before you can do anything with it.

> "Here are my notes on [topic]. Structure this so I can see what I'm actually saying."

Structure extracts the idea tree, separates claims from background context, maps dependencies, and flags gaps. The output shows you what you're proposing vs. what you're assuming.

**What to do next**: The gaps section usually reveals the most important next step. Missing foundations mean you're building on unstated assumptions — go to Assumptions. Contradictions mean you need to resolve a tension before proceeding. Imbalances mean one part of your plan is over-developed relative to others.

---

### 7. "Give me the short version"

You have a long analysis, report, or document and need it compressed for stakeholders.

> "Distill this to all four levels."

Distill produces the one-liner, elevator pitch, executive summary, and full brief. Each level preserves the logical spine and the key risks.

**Tips**:
- If you only need one level, ask for it: "Give me the elevator pitch version of this."
- If you're comparing options, ask for the Decision Frame: "Distill with a decision frame."
- Start by reading Level 4 (one-liner). If it sounds generic ("has potential but faces challenges"), the analysis itself may be too vague — go back and sharpen it.

---

## Chaining Tools

The tools are designed to chain. Each tool's hand-off section produces structured output that accelerates the next tool in the chain.

### Common Chains

| Goal | Chain |
|------|-------|
| Deep analysis | Structure → Assumptions → Stress Test → Distill |
| Improve an idea | Structure → Assumptions → Stress Test → Evolve → Stress Test → Distill |
| Quick gap check | Assumptions → Distill |
| Viability check | Stress Test → Distill |
| Multi-source research | Synthesize → Assumptions → Distill |
| Business evaluation | Business Model (self-contained) |
| High-stakes research | Peer Review → Synthesize → Assumptions → Distill |
| Complete pipeline | Full Analysis (self-contained) |

### Hand-Off Mechanics

Each tool produces specific hand-off artifacts for the next:

- **Structure** → produces "Questions for Assumptions" (3-5 signposts for where to dig)
- **Assumptions** → produces "Suggested Attack Surfaces for Stress Test" (vulnerabilities with attack angles)
- **Stress Test** → produces "Mutation Targets for Evolve" (which components to change, which operators to use, per verdict)
- **Evolve** → produces "Evolution Directive" (new baseline, remaining weakness, next mutation focus)

These hand-offs are what make chaining more powerful than running tools independently — each tool pre-loads the next one with targeted starting points.

### Iteration

The **Stress Test → Evolve → Stress Test** loop can run multiple rounds. On re-entry, Stress Test explicitly compares: did Evolve's recommendation fix the previous wounds, or introduce new vulnerabilities?

**Stopping conditions**:
- The recommended option survives all attacks
- Round N isn't meaningfully better than N-1
- Typical: 2 rounds. Maximum: 3. More than 3 is usually procrastination.

---

## How Quality Is Enforced

Every tool uses three mechanisms to ensure output quality:

### 1. Calibration Examples (GOOD/BAD pairs)

Each tool includes concrete examples of what good and bad output looks like for that tool. These are the primary behavior-steering mechanism — they show the model exactly what level of specificity is expected.

For example, a GOOD stress test attack names a specific failure mechanism, cites a real precedent (e.g., "Salesforce took 18 months for its first 10 enterprise accounts"), and includes a WOUNDED condition specific on WHAT/HOW/WHEN. A BAD attack says "competition is fierce" with no mechanism, no precedent, and no condition.

### 2. Self-Checks

Every tool ends with a checklist that must pass before delivering output. These catch common failures:
- Assumptions tool: ≥ 3 register entries, every hidden assumption has a test method
- Stress Test: every WOUNDED verdict has a WHAT/HOW/WHEN condition
- Evolve: every alternative changes ≥ 2 components, ≥ 1 uses INVERT or LEAPFROG
- Distill: risks survive to Level 3, recommendation gets MORE direct at lower levels

### 3. Guardrails

Each tool has explicit boundaries preventing scope creep:
- Structure doesn't judge — it maps
- Assumptions doesn't fix — it reveals
- Stress Test doesn't solve — it breaks
- Evolve doesn't polish — it mutates

This separation ensures each tool does its job without drifting into another tool's territory.

---

## Reference Card

| Tool | File | Input | Output |
|------|------|-------|--------|
| Structure | `structure.md` | Messy notes, documents, multi-source input | Idea tree + dependencies + gaps |
| Assumptions | `assumptions.md` | Structured plan or argument | Assumption register + drivers + logic chain + clusters |
| Stress Test | `stress-test.md` | Idea/plan to attack | Attacks with verdicts + cascade + steelman |
| Synthesize | `synthesize.md` | 2+ sources on same topic | Unified view + adjudication + emergent findings |
| Evolve | `evolve.md` | Idea + weaknesses | 4-6 alternatives + comparison + recommendation |
| Distill | `distill.md` | Any analysis | 4 compression levels (1 sentence → 1,200 words) |
| Business Model | `business-model.md` | Business model/pitch | 6-bone analysis + stress test + distillation |
| Peer Review | `peer-review.md` | Multi-model research question | Ranked synthesis with peer validation |
| Full Analysis | `full-analysis.md` | Any idea/plan/strategy | 5-stage pipeline in one pass |
