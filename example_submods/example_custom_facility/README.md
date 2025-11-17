# Example Submod: Custom Facility

This is a **complete example submod** that demonstrates how to add a custom building type that generates Research Power.

## What This Example Does

This submod adds support for a fictional "Quantum Research Lab" building:
- Counts `quantum_lab` buildings across all owned states
- Each quantum lab provides +40 flat RP
- The RP is added to both `total_research_power` and `facility_research_power` (for display)

## How It Works

This example uses two hooks:
1. `dr_collect_facility_counts_submods` - Counts the custom buildings
2. `dr_apply_facility_rp_submods` - Converts the count into RP

## Installation

**This is an example only** - it's not meant to be used as an actual submod. To use it:

1. Copy the `common/` folder to your own submod
2. Create a `descriptor.mod` file
3. Load it after "Dynamic Research Slots Reborn" in the launcher

**Note**: This example assumes you have a `quantum_lab` building type defined elsewhere in your mod. If you don't have this building, the submod will simply do nothing (no errors).

## Files

- `common/scripted_effects/ZZ_example_custom_facility.txt` - The actual submod code

## Learning Points

- How to count custom buildings using `every_owned_state`
- How to convert building counts into RP
- How to add RP to both `total_research_power` and `facility_research_power`
- Working with state-scope building variables

## Extending This Example

You could extend this to:
- Count multiple building types
- Add different RP values for different building types
- Add conditional bonuses (e.g., +20% RP if you have 5+ labs)
- Make the RP value configurable via game rules

