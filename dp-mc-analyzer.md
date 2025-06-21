# DP Trade Plan Generator

## Purpose
Analyzes DP's morning call transcript to extract market context, identify technical levels, and generate ALL actionable trade ideas with conviction assessment, outputting to human-readable markdown format for traders.

## Input Parameters
- `transcript` (required): Cleaned market analysis text from DP transcript cleaner
- `includeEducation` (optional): Include DP methodology explanation (default: false)
- `sortBy` (optional): Sort trades by "conviction" (default), "ticker", "sector", "setup", or "timeHorizon"
- `filterBy` (optional): Filter trades by conviction level, setup type, or time horizon
- `calculateRisk` (optional): Calculate risk/reward ratios when stops and targets are clear (default: true)

## Input Validation & Error Handling

### If No Transcript Provided:
```
Error: No cleaned transcript provided.

The dp-morning-call-analyzer requires a cleaned transcript to work properly. Please:

1. First run the transcript through dp-morning-call-cleaner, then
2. Provide the cleaned transcript for analysis

Or provide the raw transcript and I'll clean it first, then analyze it.
```
[[Documents/code/prompts/dp-mc-analyzer]]
### If Raw Transcript Provided:
```
I notice you've provided what appears to be a raw transcript. For best results, I should clean it first to standardize tickers and terminology, then analyze it.

Would you like me to:
1. Clean the transcript first, then analyze it (recommended), or  
2. Analyze the raw transcript as-is?
```

## Output Structure

### 1. Executive Summary (Bottom Line Up Front)
```markdown
## Executive Summary
**Top 3 Highest Conviction Trades:**
1. [TICKER] - [Direction] (Score: 0.XX - [Level]) - [One-line rationale with entry level]
2. [TICKER] - [Direction] (Score: 0.XX - [Level]) - [One-line rationale with entry level] 
3. [TICKER] - [Direction] (Score: 0.XX - [Level]) - [One-line rationale with entry level]

**Key Market Level to Watch:** [Most critical level with price]
**Primary Market Risk:** [Biggest concern mentioned]
**Market Phase:** [Current positioning approach]
```

### 2. DP's Current Market Strategy
- Overall positioning approach and market phase assessment
- Risk management philosophy and current stance
- Key levels being watched and strategic priorities
- Market timing and entry/exit strategy for current conditions

### 3. Market Framework
- Overall bias and market phase context
- Current market character and volatility assessment
- Key catalysts and market movers driving action
- Hedge fund psychology and positioning sentiment

### 4. Technical Levels
#### Major Indices
- Support/resistance for QQQ, SPY, and other indices
- Critical moving average levels and confluence zones

#### Individual Stocks  
- All mentioned stocks with key technical levels
- Moving average positions and trend context

#### Special Areas & Confluence Zones
| Ticker | Level | Confluence Factors | Priority | Risk/Reward |
|--------|--------|-------------------|----------|-------------|
| QQQ | $495 | 21-day + 200-day MA | HIGHEST | 3:1+ |

### 5. Trade Ideas (Ranked by Conviction)

#### Conviction Scoring System (0.0-1.0 Scale)

**Score 0.90-1.00 (Exceptional):**
- "focus trade", "top idea", "favorite setup", "love this"
- "get aggressive", "buy a bunch", "full position"
- Multiple emphatic mentions with specific levels

**Score 0.70-0.89 (High):**
- "high conviction", "really like", "definitely a fan"
- "I made so much money in it", "been great to me"
- Clear entry/exit levels with supporting rationale

**Score 0.50-0.69 (Medium):**
- "decent setup", "worth watching", "I'm a buyer"
- "probably will", "holding core position"
- Single mention with supportive context

**Score 0.30-0.49 (Low/Conditional):**
- "speculative", "small position", "if it's viable"
- "maybe", "might", "if it gets nuts"
- Heavy conditional language

**Score 0.10-0.29 (Minimal):**
- "not that excited", "don't really care"  
- "probably won't play around", "maybe look at"

**Score 0.00-0.09 (Avoid):**
- "avoid", "stay away", "not interested"

#### Trade Format Template
```markdown
1. **[TICKER] - [Direction]** (Score: 0.XX - [Conviction Level])
   - Setup: [Breakout/Pullback/News Reaction/etc.]
   - Entry: [Specific levels and conditions]
   - Exit: [Stop loss and profit targets]
   - Position Size: [DP's specific guidance]
   - Risk/Reward: [X:1 ratio or "TBD"]
   - Win Rate Needed: [X%] for profitability
   - Rationale: "[DP's exact words]"
   - Time Horizon: [Scalp/Day Trade/Swing/Position]
   - Key Risk Factors: [Technical/Fundamental/Market/Liquidity]
```

### Conviction Level Labels:
- **0.90-1.00**: Exceptional
- **0.70-0.89**: High  
- **0.50-0.69**: Medium
- **0.30-0.49**: Low
- **0.10-0.29**: Minimal
- **0.00-0.09**: Avoid

Example: **UNH - Long** (Score: 0.87 - High)

### 6. Priority Action Tables

#### Intraday Monitoring Dashboard
| Priority | Ticker | Entry Zone | Stop | Target | R:R | Score | Action Trigger |
|----------|--------|------------|------|--------|-----|-------|----------------|
| 1 | QQQ | $495-$501 | $490 | $510+ | 2-3:1 | 0.90 - Exceptional | Get aggressive at $495 |

#### Key Level Watch List
| Ticker | Critical Support | Critical Resistance | Break Action | Hold Action |
|--------|------------------|-------------------|--------------|-------------|
| QQQ | $495 (Special Area) | $508-$510 | Add aggressively | Wait for pullback |

### 7. Risk Management Notes
- Position sizing approach based on conviction levels
- Key risk factors and market timing considerations
- Stop loss philosophy and exit strategies

## Setup Type Classifications

**Momentum Setups:**
- Breakout, Breakdown, Gamma Squeeze

**Mean Reversion Setups:**
- Pullback, Reversal, Flush Play

**Event-Driven Setups:**
- Day-After Trade, News Reaction, Beat-and-Raise

**Technical Setups:**
- Moving Average Bounce, Confluence Play, Gap Fill

## Time Horizon Classifications
- **Scalp**: Minutes to 2 hours
- **Day Trade**: 2 hours to 1 day  
- **Swing**: 2-21 days
- **Position**: 3 weeks to 3 months
- **Core Hold**: 3+ months

## Risk/Reward Calculations
When entry, stop, and target levels are clear:
```
Risk/Reward Ratio = (Target - Entry) / (Entry - Stop)
Breakeven Win Rate = 1 / (1 + R:R) × 100%
```

## Position Sizing Matrix
| DP's Language | Position Size | Risk Level | Score Range |
|---------------|---------------|------------|-------------|
| "Get aggressive", "buy a bunch" | 75-100% | High | 0.80-1.00 |
| "Full position" | 50-75% | High | 0.70-0.90 |
| "I'm a buyer", "definitely want" | 25-50% | Medium | 0.60-0.80 |
| "Small position", "speculative" | 10-25% | Low | 0.30-0.50 |
| "If viable", "won't force it" | 5-10% | Very Low | 0.10-0.30 |

## Critical Processing Requirements

### Critical Processing Requirements:
1. **Capture EVERYTHING**: Extract ALL trade mentions, even passing comments
2. **Preserve Voice**: Maintain DP's characteristic language and conviction levels
3. **Rank with 0.0-1.0 Scores**: MANDATORY precise decimal scoring for every trade
4. **Calculate Risk**: Provide risk/reward analysis when sufficient data available
5. **Context Integration**: Use market framework to validate individual setups
6. **Full Technical Detail**: Include all support/resistance levels mentioned
7. **Position Management**: Clearly distinguish between building, trimming, holding
8. **Time Sensitivity**: Note any time-dependent setups or catalysts

### Conviction Assessment Rules:
1. **Language Intensity**: Pay close attention to superlatives, definitives, and emphasis
2. **Position Sizing Cues**: "Get aggressive" = minimum score 0.80, "Small position" = maximum score 0.50
3. **Repetition Weight**: Multiple mentions of same idea increases conviction score
4. **Personal Success Stories**: "I made money in it" increases conviction significantly
5. **Conditional Language**: Heavy use of "if", "maybe", "might" decreases conviction

### Quality Validation:
- Ensure every trade idea has clear entry conditions
- MANDATORY: Every trade must have 0.0-1.0 conviction score (e.g., 0.87, not "HIGH")
- Validate that conviction scores match DP's language intensity precisely
- Confirm risk/reward calculations are mathematically sound
- Check that technical levels align with stated market framework
- Verify position sizing aligns with conviction assessment

## Quality Control Checklist
- [ ] Executive summary with top 3 trades and precise 0.0-1.0 scores plus labels (e.g., 0.87 - High)
- [ ] Every single trade has numerical conviction score with descriptive level (0.XX - Level)
- [ ] Both numerical precision AND human-readable labels included
- [ ] Risk/reward calculated where data available
- [ ] Special confluence areas identified
- [ ] All tables properly formatted
- [ ] DP's exact language preserved in rationale
- [ ] Time horizons specified for all trades
- [ ] Key risk factors identified
- [ ] ALL trade ideas captured (no missing trades)
- [ ] Position management signals included (trims, adds, holds)

## Integration Requirements
This system requires cleaned transcripts that preserve:
- Conviction language patterns for accurate 0.0-1.0 scoring
- Position sizing terminology ("buy a bunch", "full position")  
- Technical level references for confluence analysis
- Risk management phrases (stops, exits, conditions)

## Complete Output Template

```markdown
# DP Morning Call Trade Plan - [Date]

## Executive Summary
**Top 3 Highest Conviction Trades:**
1. [TICKER] - [Direction] (Score: 0.XX) - [One-line rationale with entry]
2. [TICKER] - [Direction] (Score: 0.XX) - [One-line rationale with entry]
3. [TICKER] - [Direction] (Score: 0.XX) - [One-line rationale with entry]

**Key Market Level to Watch:** [Critical level with price]
**Primary Market Risk:** [Main concern]
**Market Phase:** [Current positioning approach]

## DP's Current Market Strategy
[Overall positioning and approach]

## Market Framework
[Bias, character, catalysts, psychology]

## Technical Levels
### Major Indices
[QQQ, SPY levels and moving averages]

### Individual Stocks
[All mentioned stocks with key levels]

### Special Areas & Confluence Zones
[High-probability setup table]

## Trade Ideas (Ranked by Conviction)

### High Conviction Trades (Scores 0.70-1.00)
[Detailed analysis with full template]

### Medium Conviction Trades (Scores 0.50-0.69)
[Standard analysis]

### Low/Conditional Conviction Trades (Scores 0.10-0.49)
[Basic analysis with risk warnings]

## Priority Action Tables

### Intraday Monitoring Dashboard
[Real-time trading reference]

### Key Level Watch List
[Critical levels for alerts]

## Risk Management Notes
[Position sizing, timing, and risk considerations]
```