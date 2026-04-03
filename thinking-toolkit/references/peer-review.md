# Peer Review Workflow
*Multi-model research collection with anonymous ranking for high-stakes synthesis.*

## When To Use

**Always** for: irreversible decisions, high-stakes strategy, significant model disagreement, safety-critical technical decisions.

**Consider** for: medium-stakes decisions, complex analytical questions, client deliverables.

**Skip** for: routine research, time-sensitive answers, obvious consensus, low-stakes exploration.

## The Protocol

### Round 1: Collect research

Submit your question to 3-4 AI models (e.g., Claude, GPT-4, Gemini, Grok). Save each response with a clear label.

### Round 2: Anonymous peer review

Submit this prompt to each of the same models:

```
Below are [N] anonymized responses to the question: "[YOUR QUESTION]"

Response A:
[Content — DO NOT identify which AI]

Response B:
[Content]

Response C:
[Content]

Response D:
[Content]

Rank these responses from best (1) to worst ([N]) based on:
1. Evidence quality and factual accuracy
2. Logical coherence and reasoning quality
3. Practical insight and usefulness
4. Completeness of coverage

Provide your ranking in this EXACT format:
RANKING: A=X, B=Y, C=Z, D=W

Then explain:
- Why you ranked the top choice #1 (be specific)
- What made the bottom choice weakest
- Any notable strengths or weaknesses in middle choices
- Any evidence concerns or logical flaws you noticed
```

**Critical**: Randomize the A/B/C/D assignments so each model doesn't know which response is its own. Keep a separate mapping:
```
Mapping (your reference only):
A = Gemini, B = Claude, C = GPT-4, D = Grok
```

Rotate assignments across queries so models don't always review themselves as "Response A."

### Round 3: Extract rankings

Build the ranking table:

```
           Response A  Response B  Response C  Response D
Claude         2          1          3          4
GPT-4          1          2          4          3
Gemini         1          3          2          4
Grok           2          1          3          4
------------------------------------------------------
Average:      1.5        1.75       3.0        3.75
Rank:         1st        2nd        3rd        4th
```

Identify:
- **Consensus picks**: Ranked #1 or #2 by ≥75% of reviewers (high confidence)
- **Controversial positions**: Ranked #1 by some, #3-4 by others (needs scrutiny)
- **Rejected positions**: Consistently bottom-ranked (likely weak)

### Round 4: Synthesize with peer data

Feed everything to the Synthesize tool with this addition:

```
PEER REVIEW RANKINGS:
[Table from Round 3]

PEER REVIEW RATIONALES:
[Each model's explanation of their rankings]
```

When synthesizing, use peer data as an additional signal:
- **Consensus pick + strong evidence** → High confidence finding
- **Rejected position + weak evidence** → Likely omit or heavily caveat
- **Controversial position** → Present both sides, note the peer split
- **Peer consensus contradicts evidence quality** → Flag and investigate ("strong evidence but peer rejection suggests oversight")

### Mining rationales

Extract from peer review explanations:
- Specific evidence challenges ("Response C cited outdated data from 2019...")
- Reasoning flaws ("Response B's logic is circular because...")
- Unique insights praised ("Only Response A mentioned the regulatory angle...")
- Practical concerns ("Response D is theoretically sound but ignores implementation costs...")

These inform adjudication in the synthesis.

## Output

Follow the Synthesize tool's output format, adding:

```
### Peer Review Summary
- Models reviewed: [N]
- Consensus pick: Response [X] (avg rank [N])
- Controversial: Response [Y] (ranked #1 by [model], #4 by [model])
- Rejected: Response [Z] (avg rank [N])
- Key insight from rationales: [most useful observation from peer reviews]
```

## Self-Check

- [ ] ≥ 3 models used for both research and peer review
- [ ] Anonymization was randomized (not A=Claude every time)
- [ ] Rankings extracted into a table with averages
- [ ] Consensus picks and controversial positions identified
- [ ] Peer rationales mined for specific evidence challenges and unique insights
