# Supply Chain Data Quality and Cost Analysis
### Reliable conclusions from incomplete order data

A reproducible analysis of 3,000 simulated orders, focused on data completeness, inconsistent recorded costs, and category-level cost concentration.

**Tools:** Python · pandas · Jupyter  
**Analyst:** Chukwuemeka Ogo

**[View dashboards](docs/dashboard-gallery.md)** · [Read analytical notes](docs/analytical-notes.md)

## Business question

Which procurement questions can be answered reliably when an order export has incomplete dates and inconsistent values?

## Dashboard preview

![Supply Chain Data Quality and Cost Analysis overview](images/data-quality-overview.png)

[Explore all dashboard views and version notes →](docs/dashboard-gallery.md)

## Key findings

| Finding | Result | Interpretation |
| --- | ---: | --- |
| Missing order dates | 2,683 (89.4%) | Monthly trends cannot be reliably reproduced |
| Missing delivery dates | 296 (9.9%) | Timing analysis needs an explicit missing-data approach |
| Cost differs from quantity × unit price by more than 0.02 | 154 (5.1%) | Investigate adjustments or input errors |
| Recorded cost attributed to Motors | 39.2% | Review category concentration |

Motors accounts for 66,671,196 dataset units. The currency is unspecified.

## Decision use

1. Recover missing dates from the source before reporting monthly or delivery-speed trends.
2. Investigate recorded-cost differences before assuming they are errors.
3. Use supported category-cost comparisons to guide further review.

These recommendations identify next steps; they do not represent measured business impact.

## Approach

Audit missing dates and recorded-cost consistency, standardise supplier spellings in a working column, and summarise recorded cost by category. Limit reported conclusions to fields supported by the supplied export.

## Explore the project

| Resource | Purpose |
| --- | --- |
| [Analysis notebook](supply-chain-eda.ipynb) | Analysis notebook |
| [Supplied order data](cleaned_supply_chain_dataset.csv) | Supplied order data |
| [Dashboard gallery](docs/dashboard-gallery.md) | Full-size views and version context |
| [Analytical notes](docs/analytical-notes.md) | Methodology, metric definitions, and limitations |

## Scope and limitations

The orders are simulated. Cost mismatches are flags for investigation, not proof of incorrect values. Incomplete dates restrict time-based conclusions, and no procurement savings are demonstrated.

---

[Portfolio](https://mikkymo.github.io/portfolio/) · [LinkedIn](https://www.linkedin.com/in/ogochukwuemeka/)
