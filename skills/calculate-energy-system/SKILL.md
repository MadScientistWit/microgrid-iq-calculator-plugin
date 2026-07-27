---
name: calculate-energy-system
description: Use the MicroGrid-IQ read-only calculators for energy, AC power, voltage drop, dwelling load, utility bill, battery backup, or explicit cash-flow calculations.
---

# Calculate an energy system

Use this skill when a user asks for a numeric energy or electrical calculation that matches one of the MicroGrid-IQ tools.

## Workflow

1. Select the narrowest matching calculator.
2. Confirm that every required numeric value and unit is present. Ask for a missing value instead of inventing it.
3. Call exactly one calculator first. Call another only when the user's question genuinely requires a second calculation.
4. Report the result with its units, assumptions, method version, and warnings.
5. Explain which input would change the result most when that is useful.

## Tool selection

- `microgrid_iq_energy_use`: constant power and duration.
- `microgrid_iq_ac_power`: single-phase or balanced three-phase AC power.
- `microgrid_iq_voltage_drop`: copper-conductor voltage-drop planning estimate.
- `microgrid_iq_dwelling_load`: traditional dwelling service-load planning estimate.
- `microgrid_iq_utility_bill`: caller-supplied flat rate and optional demand charge.
- `microgrid_iq_battery_size`: constant critical load and target backup duration.
- `microgrid_iq_cash_flow`: explicit investment, annual cash flows, and discount rate.

## Boundaries

- Do not infer a tariff, incentive, tax treatment, code edition, jurisdiction, conductor ampacity, or equipment specification.
- Do not claim that a result is a stamped design, permit determination, utility approval, code-compliance decision, tariff quote, or procurement recommendation.
- Keep electrical and dwelling results labeled as planning estimates pending adopted-code, authority, and qualified-professional review.
- Keep cash-flow results labeled as arithmetic analysis, not tax, legal, accounting, or investment advice.
- Never send customer accounts, private projects, billing records, credentials, or personal data to these public stateless tools.
