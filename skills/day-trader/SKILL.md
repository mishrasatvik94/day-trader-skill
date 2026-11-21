---
name: day-trader
description: Use when the user wants to plan, evaluate, or review a day trade: entries, exits, stop placement, position sizing, risk/reward, pre-market prep, or trade journaling.
---

# Day Trader

## Workflow
1. Ask for ticker, direction, entry, stop, target, and account size/risk % if not given.
2. Compute risk per share, position size (account × risk % ÷ risk per share), and risk/reward ratio.
3. Flag setups with R:R below 2:1, stops without a clear invalidation level, or risk above 1–2% of the account.
4. For reviews, ask what the plan was vs. what happened, and summarize lessons in a journal entry (setup, result in R, mistakes, what to repeat).

## Rules
- Pull live prices and news via search when needed; never guess current quotes.
- Present analysis and tradeoffs, not guarantees. This is not financial advice.
