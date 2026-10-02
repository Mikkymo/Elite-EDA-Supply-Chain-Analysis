# Analytical Notes

[Back to project overview](../README.md)

## Objective

Which procurement questions can be answered reliably when an order export has incomplete dates and inconsistent values?

## Data and method

Audit missing dates and recorded-cost consistency, standardise supplier spellings in a working column, and summarise recorded cost by category. Limit reported conclusions to fields supported by the supplied export.

## Reported results and definitions

| Finding | Result | Interpretation |
| --- | ---: | --- |
| Missing order dates | 2,683 (89.4%) | Monthly trends cannot be reliably reproduced |
| Missing delivery dates | 296 (9.9%) | Timing analysis needs an explicit missing-data approach |
| Cost differs from quantity × unit price by more than 0.02 | 154 (5.1%) | Investigate adjustments or input errors |
| Recorded cost attributed to Motors | 39.2% | Review category concentration |

Motors accounts for 66,671,196 dataset units. The currency is unspecified.

## Review the analysis

Open `supply-chain-eda.ipynb` from the repository root in Jupyter or VS Code. Use a Python environment with pandas and the packages imported by the notebook. Keep the CSV alongside the notebook.

## Interpretation

- Recover missing dates from the source before reporting monthly or delivery-speed trends.
- Investigate recorded-cost differences before assuming they are errors.
- Use supported category-cost comparisons to guide further review.

## Limitations

The orders are simulated. Cost mismatches are flags for investigation, not proof of incorrect values. Incomplete dates restrict time-based conclusions, and no procurement savings are demonstrated.

## Historical material

The archive retains an earlier notebook and visual exports, including time-based analysis that referenced a raw CSV not supplied here. Use the current notebook and supported findings for portfolio discussion.
