# Day Trader Skill

Day trading analysis and trade-planning skill for Claude Code and Cowork.

## Overview

Helps plan and review day trades: setups, risk sizing, and trade journaling.

- **Pre-trade Setup**: Computes risk per share, position size (`account × risk % ÷ risk per share`), and risk/reward (R:R) ratio.
- **Risk Management**: Flags setups with R:R below 2:1, stops without clear invalidation levels, or risk exceeding 1–2% of the account.
- **Post-trade Review**: Compares execution against plan and summarizes lessons in a trade journal entry.

## Installation in Claude Code

Run the following commands:

```bash
/plugin marketplace add mishrasatvik94/day-trader-skill
/plugin install day-trader-skill@day-trader-skill
```

## Quick Test

Try a prompt in Claude:
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
└── README.md
```

## Notes
- To access the original 11 day-trading tools (chart scanner, news monitor, timemachine, broker, etc.), switch to the `11-trader-tools` branch.
