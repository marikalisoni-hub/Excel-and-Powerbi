# Store Network Investment Analysis

Self-directed analytics project that appraises a portfolio of 20 retail stores, modelling each store's economics from sales through to a full investment verdict and visualising the estate in a Power BI dashboard that recommends a lifecycle action for every store.

> **Note on the data.** The dataset is **synthetic and illustrative** — it is not drawn from any real company. Every figure is constructed, but each variable is made to sit within reasonable industry benchmark ranges (sales density, fit-out cost, store payback, conversion rates). The project tries to demonstrates an analytical approach and financial reasoning, not a specific company's results.

---

## Contents

| File | What it is |
|------|------------|
| `store_network_model.xlsx` | The dataset and financial model: data table, editable assumptions, and a documentation & sources tab. |
| `Store_network_power_bi.pbix` | The Power BI dashboard built on the dataset. |
| `dashboard.png` | A static image of the dashboard, so it can be viewed without Power BI Desktop. |

---

## What it does

### The Excel model
Builds a per-store economic picture and turns it into an investment decision:

- **Store P&L logic:** Annual sales → four-wall contribution  → less an allocation of central overhead → store net contribution → less tax and maintenance capex → after-tax cash flow.
- **Investment appraisal:** Total CAPEX + working capital = investment base; **NPV** via a finite growing-annuity over an **editable lease horizon** (for the dashboard set at 15 years), plus **ROIC** and an **investment verdict** (value-creating / marginal / value-destroying).
- **Rule-based recommendation engine:** each store is tagged Keep / Keep (maturing) / Refurbish / Turnaround / Expand format / Close–Relocate, driven by the value verdict and the store's trajectory, with every threshold held in an editable cell.
- **Benchmarked, sourced inputs:** input ranges are calibrated to published figures and documented with sources on a dedicated tab.

### The Power BI dashboard
A single-screen executive view:

- **KPI strip:** total CAPEX deployed, portfolio sales per m², like-for-like growth, weighted ROIC, and % of the estate destroying value.
- **Signature scatter:** CAPEX per m² vs sales per m², bubble-sized by annual sales, coloured by recommendation, with median quadrant lines separating stars from problem stores.
- **NPV ranked bar** coloured by verdict, and a **recommendation matrix** summarising the number of stores, CAPEX and NPV in each action bucket.

---

## Key assumptions (illustrative and editable)

Discount rate 8% · long-run growth 1.5% · corporation tax 25% · central overhead 5% of sales · working capital 8% of sales · maintenance capex ~2% of sales · appraisal horizon 15 years (≈ a typical retail lease term).
---


- **Four-wall margin is a modelling assumption.** Retailers do not disclose it publicly, so it is set by format and maturity and kept deliberately conservative here.
- **The estate reads as a mixed portfolio** — some stores create value, several destroy it. 

---

## How to use

- **Excel:** open the file and edit the blue assumption cells to re-appraise the whole estate; see the *Documentation & Sources* tab for definitions and benchmark references.
- **Power BI:** open the `.pbix` in Power BI Desktop (free), or simply view `dashboard.png`.
