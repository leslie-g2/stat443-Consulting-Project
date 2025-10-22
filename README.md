````markdown
# Gas Turbine NOx Reduction – STAT 443 Consulting Project

## Project Goal
Consulting project for STAT-443 Professional Statistics.
We work with turbine sensor data from an energy provider in Turkey to:
- Analyze NOx (nitrogen oxides) and CO (carbon monoxide).
- Identify operational variables that drive NOx.
- Recommend actions to reduce NOx while keeping CO acceptable.
- Deliver a final report + documented code (R/Python) by December.

---

## Requirements / Objectives
1) Data Exploration (EDA)
- Check distributions, trends, outliers for all variables.
- Plot NOx and CO against turbine variables (TIT, CDP, TEY, etc.).

2) Data Cleaning
- Handle missing values or sensor errors.
- Remove outliers (spikes beyond physical turbine ranges).

3) Feature Engineering
- Create load bands from TEY.
- Derive temperature deltas (e.g., TIT–TAT).
- Add interaction terms (e.g., CDP × TIT, AT × AH).

4) Modeling
- Build predictive models for NOx (Linear Regression, Random Forest, etc.).
- Compare performance and feature importance.
- Run “what-if” scenarios (lower TIT, shift load band).

5) Recommendations
- Operational changes to lower NOx.
- NOx–CO trade-off analysis.
- Sensitivity to ambient conditions (temperature, humidity).

---

## Client + Context (from first meeting)
- Client: Energy provider in Turkey.
- Equipment: Gas turbines with emissions and operational sensors.
- Contact: Engineering Manager. Preferred communication: email.
- Data: Hourly averages for ~2 years (~14k rows).
- Normal power range ~130–136 MWh; higher loads up to ~160 MWh.
- Variables include:
  - Ambient: AT (temp), AP (pressure), AH (humidity)
  - Process: AFDP (air filter ΔP), CDP (compressor discharge pressure), GTEP (exhaust pressure)
  - Temps: TIT (turbine inlet), TAT (turbine exhaust)
  - Output: TEY (power/energy)
  - Emissions: CO, NOX (target)
- Deliverables: Report + documented code (R/Python), guidance for different weather conditions.
- Deadline: December.

---

## EDA Findings (summary)
- TIT often near upper limit → strong driver of NOx.
- TAT tightly controlled ~550°C → less variance.
- TEY shows discrete load bands → segment analysis by load.
- CDP, GTEP, AFDP show multi-modal behavior → indicates modes/regimes.
- CO mostly near zero with occasional spikes → typical NOx–CO trade-off.
- Ambient humidity tends to suppress NOx slightly; temperature shifts baseline.

---

## Methods Used So Far
- Histograms, correlation matrix (Pearson), scatter plots (NOX vs TIT, CDP, TEY, CO).
- Load band segmentation by TEY (e.g., ≤136, 136–160, >160).
- Baseline models: Linear Regression (scaled), Random Forest for nonlinearity.
- Early importance: TIT, CDP, TEY rank high for NOx.

---

## Next Steps
- Feature engineering: ΔT (TIT–TAT), interactions (CDP×TIT), ambient bins.
- Scenario testing: effect of decreasing TIT by set increments, high-humidity vs low-humidity cases.
- Multi-metric view: ensure CO stays within limits while reducing NOx.
- Finalize recommendations and KPI targets (compliance margin, $/ton abated, uptime).

---

## Setup
- Python 3.x
- Packages: pandas, numpy, matplotlib, scikit-learn
- Optional: R environment if required for deliverable parity.
- Run notebooks in order; keep individual work inside each person’s folder.

---

## Git Workflow (Direct to main)
Since each member works only inside their own folder, push directly to `main`.

1. Check status
```bash
git status
````

2. Stage changes

```bash
git add .
git status
```

3. Commit (short message, straight)

```bash
git commit -m "feat(<name>): add/update analysis"
# examples:
# feat(hee-jae): add NOx vs TEY plots
# feat(sean): update regression model
# chore(viraj): clean CO outliers
```

4. Push to main

```bash
git push origin main
```

---

## Notes

* Keep work inside your folder. Do not edit others’ folders.
* Use short commit messages: feat, fix, chore + your name + action.
* If stuck, check README or ask teammates; ChatGPT can assist.

```
::contentReference[oaicite:0]{index=0}
```