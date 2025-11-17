# Example Submod: Balance Tweak

This is a **complete example submod** that demonstrates how to make simple balance adjustments to the Dynamic Research Slots system.

## What This Example Does

This submod makes the following changes:
- **Increases civilian factory RP** by +1 (from 3 to 4 base RP per civ factory)
- **Increases nuclear facility RP** by +10 (from 50 to 60 RP per facility)
- **Adds a small RP bonus** for countries with high stability (>80%)

## How It Works

This example uses the `dr_apply_research_config_submods` hook for config tweaks and the `dr_total_rp_modifier_submods` hook for conditional bonuses.

## Installation

**This is an example only** - it's not meant to be used as an actual submod. To use it:

1. Copy the `common/` folder to your own submod
2. Create a `descriptor.mod` file
3. Load it after "Dynamic Research Slots Reborn" in the launcher

## Files

- `common/scripted_effects/ZZ_example_balance_tweak.txt` - The actual submod code

## Learning Points

- How to use `dr_apply_research_config_submods` for small config tweaks
- How to use `dr_total_rp_modifier_submods` for conditional bonuses
- Simple variable operations and conditional logic

