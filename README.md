# Fixed Income Portfolio Construction & Immunization

An academic liability-driven investing project examining how Treasury and Aaa/Baa credit allocations can support a **hypothetical $100 million future liability**. The analysis compares static holdings with semiannual rebalancing to explore duration alignment, portfolio funding, and interest-rate exposure.

**Bloomberg · Excel · Python · Fixed Income · Liability-Driven Investing**

[Read the report](reports/final-project-original.pdf) · [Download the Excel model](models/portfolio-model-original.xlsx) · [View the Python notebook](notebooks/bloomberg-data-retrieval-original.ipynb) · [Explore the Bloomberg data](data/bloomberg-index-data-2018-2025-original.xlsx)

---

## Project at a Glance

| Item | Scope |
|---|---|
| Objective | Examine fixed income portfolio strategies for a future payment obligation |
| Hypothetical liability | $100 million due December 31, 2025 |
| Study window | December 31, 2018–December 31, 2025 |
| Assets examined | Treasury indexes and Aaa/Baa long credit indexes |
| Strategies | Static holdings and semiannual rebalancing |
| Risk and funding measures | Portfolio duration, duration gap, surplus/shortfall, and funding ratio |
| Tools | Bloomberg, Excel, Python, pandas, xbbg, and Bloomberg API |
| Context | FRL 6460: Fixed Income Securities — academic team project |

## Investment Question

How can a fixed income portfolio be structured and managed to support a known future liability?

A future payment creates two related questions: how much capital is needed today, and how sensitive should the portfolio be to changes in interest rates? Duration-based immunization considers asset value, liability present value, and their respective interest-rate sensitivities.

As the payment date approaches, the liability's remaining horizon declines. This project explores how static holdings and periodic allocation adjustments address that changing horizon, using Treasury and Aaa/Baa credit indexes as the investment inputs.

## Analytical Approach

1. **Prepare market data.** Retrieve Bloomberg index observations with Python and organize the data for spreadsheet analysis.
2. **Model portfolio allocations.** Examine Treasury and credit allocations in relation to a seven-year liability horizon.
3. **Compare management strategies.** Evaluate static holdings alongside semiannual rebalancing.
4. **Analyze risk and funding.** Examine duration gaps, portfolio values, liability present values, surplus or shortfall, and funding ratios.
5. **Communicate the analysis.** Present the strategy framework and portfolio comparisons in a written report supported by an Excel model and market data.

## Portfolio Analysis

### Static Holdings

The static approach provides a reference for examining how a portfolio's interest-rate exposure evolves when initial holdings are maintained. The analysis considers duration drift and the relationship between portfolio value and the liability's present value over time.

### Semiannual Rebalancing

The rebalancing approach explores periodic allocation adjustments as the liability horizon shortens. It provides a framework for assessing how ongoing portfolio management can address changes in duration exposure and funding needs.

### Aaa and Baa Credit Allocations

The project examines two credit-index allocations alongside Treasury exposure. This comparison adds a credit-quality dimension to the portfolio construction exercise and supports discussion of how asset selection interacts with liability-management objectives.

### Measures Used

| Measure | Analytical purpose |
|---|---|
| Portfolio duration | Assess sensitivity to changes in interest rates |
| Duration gap | Compare portfolio duration with liability duration |
| Portfolio value and liability present value | Track assets relative to the discounted payment obligation |
| Surplus or shortfall | Examine the difference between portfolio value and liability present value |
| Funding ratio | Express portfolio value relative to liability present value |

## Technical Implementation

### Python and Bloomberg Data Workflow

The notebook uses `xbbg` and `blpapi` to retrieve Bloomberg index levels, organizes the responses into pandas tables, calculates index-level percentage changes, and exports the data to Excel.

The workflow covers **five fixed income indexes**, providing a structured data foundation for the portfolio analysis.

| Series | Bloomberg identifier |
|---|---|
| Treasury 1–4 year | `I03840US Index` |
| Treasury 3–7 year | `LT13TRUU Index` |
| Treasury 3–10 year | `LT31TRUU Index` |
| Long credit Aaa | `I02787US Index` |
| Long credit Baa | `I02788US Index` |

The notebook focuses on market-data retrieval and preparation. The accompanying data workbook contains index observations, durations, and coupon inputs used in the spreadsheet work.

### Excel Portfolio Analysis

The Excel workbook contains initial allocation exercises, cash-flow calculations, and rebalancing schedules. These components support the comparison of portfolio strategies and the examination of duration and funding measures.

### Written Report

The report brings together the investment objective, analytical framework, and portfolio comparisons. It connects the technical work to the practical question of managing assets against a future payment obligation.

## Skills Demonstrated

- **Portfolio construction:** Framing Treasury and credit allocations around a defined liability and investment horizon.
- **Fixed income risk analysis:** Examining duration exposure, funding ratios, and surplus or shortfall.
- **Programming and data preparation:** Retrieving Bloomberg observations with Python and organizing them for Excel analysis.
- **Investment communication:** Synthesizing portfolio methods and comparisons in a team research report.

## Project Materials

| Material | Contents |
|---|---|
| [PDF report](reports/final-project-original.pdf) | Team research narrative, portfolio comparisons, and supporting figures |
| [Excel model](models/portfolio-model-original.xlsx) | Allocation exercises, cash-flow calculations, and rebalancing schedules |
| [Python notebook](notebooks/bloomberg-data-retrieval-original.ipynb) | Bloomberg data retrieval, preparation, and export |
| [Bloomberg data workbook](data/bloomberg-index-data-2018-2025-original.xlsx) | Index observations and supporting market inputs |

The report can be read without running Python. Running the data-retrieval notebook requires a compatible Python environment and authorized Bloomberg Desktop API access.

## Team Credit

Prepared for FRL 6460 by **Noah Avina, Ana Lopez, Joshua Robles, and Andrew Pasten**. This repository presents the academic team project as part of Andrew Pasten's portfolio.

## Connect

[GitHub](https://github.com/Andrew-Pasten) · [LinkedIn](https://www.linkedin.com/in/andrewpastencpp/) · [Portfolio](https://andrew-pasten.github.io/Portfolio.io/index.html)
