---
name: day-trader
description: Use when the user wants to plan, evaluate, or review a day trade: pre-market prep, setup evaluation, entry/stop/target planning, risk sizing, risk/reward calculations, or trade journaling.
---

# Day Trader Skill

A structured day-trading planning, evaluation, position sizing, and journaling assistant.

## Workflows

### 1. Pre-Market Plan
When the user wants to prepare for the trading session:
1. Identify watchlisted tickers, key technical levels (prior day high/low, pre-market high/low, major support/resistance), and catalysts (earnings, economic releases, news).
2. Define trigger conditions: break and retest, opening range breakout (ORB), or bounce from key level.
3. Formulate if/then scenarios before the open. Avoid chasing outside the predefined levels.

### 2. Setup Evaluation & Invalidation
When the user brings a trade setup:
1. Gather core parameters: ticker, direction (long/short), intended entry, planned stop-loss, and profit target(s).
2. Invalidation Level: Verify that the stop-loss is anchored to a concrete technical invalidation point (e.g., below swing low, under support level, breakdown of VWAP), not an arbitrary dollar amount.
3. Calculate Risk:Reward (R:R):
   - Risk per share = |Entry - Stop|
   - Reward per share = |Target - Entry|
   - R:R Ratio = (Reward per share) / (Risk per share)
4. Evaluation Guardrails:
   - Flag any setup where R:R is below 2:1.
   - Flag any setup lacking a clear structural invalidation level.

### 3. Position Sizing & Risk Management
When sizing an order:
1. Request account equity and risk tolerance percentage (recommend 1–2% max per trade).
2. Calculate dollar risk: Account Size * Risk %.
3. Calculate share size:
   - Shares = floor((Account Size * Risk %) / |Entry - Stop|)
4. Compute total position value (Shares * Entry) and verify it fits within purchasing power.
5. If dollar risk exceeds 2% of the account, actively warn the user to reduce size.

### 4. End-of-Day Journal & Review
When reviewing past trades or logging results:
1. Compare execution to the pre-trade plan:
   - What was the intended setup vs. actual execution?
   - Was the stop respected, moved, or removed?
   - Did the exit follow the target rules or was it an emotional exit?
2. Record metrics:
   - Outcome in R-multiples (e.g., +2.5R or -1R).
   - Net profit/loss and execution quality score.
3. Extract actionable takeaways:
   - Mistakes made (FOMO, oversized, chasing, hesitated).
   - Good behaviors to repeat.

---

## Guardrails & Rules

- **Educational & Planning Purpose Only**: This skill provides analysis, risk modeling, and structured workflows. It does not provide financial or investment advice.
- **No Guaranteed Profits**: Never promise profits, win rates, or certain outcomes. Day trading carries substantial risk of capital loss.
- **Data Integrity**: Numbers (prices, entries, account size, stops) must come directly from the user or from live data/search tools if available. Never guess or hallucinate quotes or historical levels.
- **Risk First**: Always prioritize capital preservation over return potential.
