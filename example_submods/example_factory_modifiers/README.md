# Example Submod: Factory Modifiers

This is a **complete example submod** that demonstrates how to add factory RP modifiers based on ideas, national spirits, or focuses.

## What This Example Does

This submod adds factory RP bonuses based on ideas:
- **Free Trade idea**: +10% civilian factory RP
- **War Economy idea**: +15% military factory RP
- **Naval Focus idea** (fictional): +20% naval factory RP

## How It Works

This example uses the `dr_apply_factory_modifiers_submods` hook to set multiplicative modifiers that are applied before factory RP calculation.

## Installation

**This is an example only** - it's not meant to be used as an actual submod. To use it:

1. Copy the `common/` folder to your own submod
2. Create a `descriptor.mod` file
3. Load it after "Dynamic Research Slots Reborn" in the launcher

**Note**: This example uses vanilla idea IDs (`free_trade`, `war_economy`). If you're using an overhaul mod that changes these, adjust the idea IDs accordingly.

## Files

- `common/scripted_effects/ZZ_example_factory_modifiers.txt` - The actual submod code

## Learning Points

- How to use `dr_apply_factory_modifiers_submods` hook
- How to set multiplicative factory modifiers
- How to check for ideas/national spirits
- Understanding that modifiers are multiplicative (0.10 = +10%)

## Extending This Example

You could extend this to:
- Check for national spirits instead of ideas
- Check for completed focuses
- Add country-specific modifiers
- Add conditional modifiers (e.g., only during war)
- Stack multiple modifiers

