# Day Trader Skill

Day trading analysis, setup evaluation, position sizing, and trade-planning skill for Claude Code and Cowork.

## Workflows Covered

- **Pre-Market Plan**: Key technical levels (PDC, PDH, PDL, PMH, PML), catalysts, and if/then scenarios.
- **Setup Evaluation**: Structural invalidation check and minimum 2:1 Risk:Reward (R:R) filtering.
- **Position Sizing**: Strict account % risk-based sizing calculation (`Shares = floor((Account * Risk %) / |Entry - Stop|)`).
- **End-of-Day Journal**: Logs plan vs. actual execution, metrics in R-multiples, errors, and lessons.

## Installation in Claude Code

Run the following commands:

```bash
/plugin marketplace add mishrasatvik94/day-trader-skill
/plugin install day-trader-skill@day-trader-skill
```

## Quick Test

Try asking Claude:
> *"Plan a long on NVDA, entry 120, stop 118.5, $25k account, 1% risk."*

## Repository Structure

```
day-trader-skill/
├── .claude-plugin/
│   ├── marketplace.json
│   └── plugin.json
├── skills/
│   └── day-trader/
│       └── SKILL.md
├── .gitignore
├── LICENSE
└── README.md
```

## Guardrails
- Educational and planning purposes only; not financial advice.
- No guaranteed profits or win rates.
- Numbers and prices come from the user or live search/data tools (never hallucinated).
