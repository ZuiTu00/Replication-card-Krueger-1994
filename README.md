# Replication & Extension: Card & Krueger (1994) — The Effect of Minimum Wage on Employment

## Executive Memo

### The Bottom Line Up Front (BLUF)

New Jersey's 1992 minimum wage increase from $4.25 to $5.05 did not reduce fast-food employment — in fact, restaurants forced to raise wages the most experienced the largest employment gains (+3.29 FTE, p < 0.05). This dose-response pattern is inconsistent with the standard competitive labor market model and instead supports a **monopsony** interpretation, where employers had been paying workers below the market-clearing wage.

### The Mechanism: How We Isolated the Causal Effect

To estimate the causal effect of minimum wage on employment, we used a **Difference-in-Differences (DID)** design — a method that mimics a randomized experiment using naturally occurring policy variation.

Think of it this way: imagine you want to know whether a new fertilizer helps plants grow. You can't just compare fertilized plants to unfertilized ones, because the fertilized group might have had better soil to begin with. Instead, you measure how much *both* groups grow over time, and then compare the *change* in growth. If the fertilized plants grew faster than the unfertilized ones — relative to where they started — you can attribute that extra growth to the fertilizer.

Here, New Jersey (which raised its minimum wage) is the "fertilized" group, and neighboring Pennsylvania (which did not) is the control. By comparing the *change* in employment in NJ restaurants to the *change* in PA restaurants, we difference out any common economic trends that would have affected both states equally — isolating the causal effect of the wage policy.

**The critical identifying assumption** is the *parallel trends* assumption: absent the policy, NJ and PA fast-food employment would have followed the same trajectory. Given the geographic proximity and shared labor markets along the NJ–PA border, this assumption is plausible.

### The Visual Evidence

![Forest Plot: Heterogeneous Treatment Effects](Forest%20plot.png)

**Figure 1. Heterogeneous Treatment Effects of NJ Minimum Wage Increase on FTE Employment.**
This forest plot displays DID estimates across restaurant subgroups. Blue points represent chain-level effects (Burger King, KFC, Roy Rogers, Wendy's); orange points represent effects by treatment intensity (High-GAP vs. Low-GAP, where GAP measures the percentage wage increase mandated by the policy). The red dashed line marks zero effect; the green dotted line marks the full-sample average (+2.75 FTE). Restaurants facing larger mandated wage increases (High-GAP) show a stronger positive employment response, consistent with monopsony dynamics. Confidence intervals are based on heteroskedasticity-robust standard errors.

### Business/Policy Implications

These findings carry three actionable implications for policymakers considering minimum wage legislation:

1. **Moderate minimum wage increases are unlikely to cause the job losses predicted by textbook competitive models.** The evidence from this natural experiment shows that employment can remain stable or even increase following a wage floor adjustment — provided the increase is within a range where monopsony power exists.

2. **The effects are not uniform — policy design should account for heterogeneity.** High-treatment-intensity restaurants (those paying the lowest wages pre-policy) responded most strongly. This suggests that minimum wage policy disproportionately benefits workers at the very bottom of the wage distribution, and that blanket predictions of uniform job loss are overly simplistic.

3. **Chain-level variation matters for enforcement and impact assessment.** The finding that Burger King restaurants showed the largest positive effect while KFC showed a small (insignificant) negative effect suggests that firm-level characteristics — such as pricing power, franchise structure, and labor substitution strategies — mediate the employment response. Regulators should monitor compliance and labor outcomes at the firm level, not just in aggregate.

---

## Repository Structure

```
├── README.md                  ← You are here (Executive Memo)
├── data/
│   ├── raw/                   ← Original Card & Krueger data (public.dat)
│   └── processed/             ← Cleaned data ready for modeling
├── notebooks/
│   ├── 01_Data_Cleaning.ipynb
│   ├── 02_Replication_Analysis.ipynb
│   └── 03_Extension_and_Results.ipynb
├── forest_plot_hte.png        ← Production-grade visualization
└── requirements.txt           ← Python dependencies
```

## Phase 3: Extension — Heterogeneous Treatment Effects

This extension examines whether the average DID effect (+2.75 FTE) masks heterogeneity across restaurants. Analysis includes:

- **GAP variable**: measures treatment intensity — the percentage by which each NJ restaurant's pre-policy wage must rise to meet the new $5.05 minimum
- **Chain-level subgroups**: separate DID regressions for Burger King, KFC, Roy Rogers, Wendy's
- **Treatment intensity subgroups**: High-GAP vs. Low-GAP restaurants
- **Visualization**: forest plot comparing all subgroup effects

**Key finding**: restaurants facing larger mandated wage increases experienced greater employment gains (GAP coefficient = 12.49, p = 0.038), consistent with a monopsony labor market interpretation.

## Replication Results (Phase 2)

The baseline DID estimate replicates Card & Krueger's core finding: NJ fast-food restaurants experienced an average increase of approximately **+2.75 FTE** relative to PA controls following the minimum wage increase, contradicting the competitive model prediction of employment decline.

## Data Source

Card, D. & Krueger, A.B. (1994). "Minimum Wages and Employment: A Case Study of the Fast-Food Industry in New Jersey and Pennsylvania." *American Economic Review*, 84(4), 772–793.

## Requirements

```
pandas
numpy
statsmodels
matplotlib
seaborn
```
