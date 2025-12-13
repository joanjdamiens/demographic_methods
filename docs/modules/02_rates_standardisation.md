# Rates and direct standardization

## What question does this answer?
How do I compare mortality between two groups (or over time) **without being fooled by different age structures**?

## What data do I need?
- Deaths by age group
- Exposure (population or person-years) by age group
- A standard population age distribution

## Core idea (plain language)
If one group is older, it will have more deaths even if “true” age-specific risks are identical.
Standardization answers: *“What would the rate be if both groups had the same age structure?”*

## Assumptions
- Age-specific death rates are reasonably measured
- The chosen standard population is appropriate for comparison

## Diagnostics
- Plot age-specific rates `mx` by age group
- Check for impossible values (negative, huge spikes from tiny denominators)

## Practical
- Data: `../data/mortality_standardization.csv`
- Code:
  - R: `../code/02_rates_standardization.R`
  - Stata: `../code/02_rates_standardisation.do`

## Self-check
When you run the script, the standardized rate should be around **0.007–0.008**.

## Interpretation
“This standardized rate is the death rate we would observe if the population had the age distribution of the standard population.”

## Common failure modes
- Very small exposures in an age group → unstable rates
- Comparing standardized rates computed with **different standards** (don’t do that)
