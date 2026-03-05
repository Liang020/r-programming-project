# COVID-19 Peak Synchrony Across U.S. States (County-Level)

## What this project does
Quantifies how synchronized county-level COVID-19 case peaks were *within each U.S. state* during a national-wave window.  
I compute a state-level **dispersion metric** (IQR of county peak dates, in days): **larger IQR = less within-state synchrony**.

## Data
This project uses county-level COVID-19 time series data provided as part of a course dataset (not redistributed in this repo).  
See `data/README.md` for instructions.

## Methods (high-level)
- Construct 7-day rolling average case series
- Define each county’s peak date within a fixed national-wave window (±90 days)
- Aggregate county peak dates to state-level dispersion using **IQR (days)**
- Visualize results via map, ranking, and case studies

## Key results (2–3 takeaways)
- States vary substantially in within-state peak synchrony (IQR ranges widely across states).
- A clear top/bottom ranking emerges, highlighting states with the most vs. least synchronized county peaks.
- Case-study states illustrate how tighter clustering of county peak dates corresponds to stronger synchrony.

---

## Figure 2 — State-level peak-date dispersion (IQR days)
![State-level IQR map](figures/fig2_state_iqr_map.png)

## Figure 3 — Ranking (Top 10 vs Bottom 10)
![Top vs Bottom states](figures/fig3_top_bottom10.png)

## Figure 4 — Case study (county peak dates within selected states)
![Case study states](figures/fig4_case_study_states.png)

---

## Report
- HTML report: see instructions below to view via GitHub Pages (recommended), or download from the repo after enabling Pages.

## Reproducibility (summary)
Open `Final_Project.rmd` and run the analysis end-to-end.  
Figures are exported to `figures/` via `ggsave()` calls in the Rmd.