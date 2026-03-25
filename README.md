# Replication Study: Card & Krueger (1994)
## Minimum Wages and Employment: A Case Study of the Fast-Food Industry in New Jersey and Pennsylvania

---

## Executive Memo

### The Bottom Line
Raising New Jersey's minimum wage from $4.25 to $5.05 in 1992 **did not reduce fast-food employment**. Our replication confirms Card and Krueger's original finding: NJ restaurants gained approximately 2.75 more full-time equivalent (FTE) workers than Pennsylvania restaurants. Our extension reveals that this average effect is not uniform — restaurants forced to raise wages the most actually saw the **largest employment gains**, and different fast-food chains responded in notably different ways.

### How We Identified the Causal Effect
Imagine two identical neighborhoods separated by a state border. On April 1, 1992, one side (New Jersey) raised its minimum wage while the other (Pennsylvania) kept it the same. Everything else — the local economy, consumer demand, weather — affected both sides equally. By comparing how employment changed on each side of the border, we can isolate the effect of the wage increase alone. This is the Difference-in-Differences (DID) method: we take the change in NJ employment, subtract the change in PA employment, and what remains is the causal impact of the minimum wage policy. We surveyed 331 NJ and 79 PA fast-food restaurants before and after the policy change.

### The Visual Evidence

![Forest Plot: Heterogeneous Treatment Effects](forest_plot_hte.png)

**Figure 1: Subgroup DID estimates of the NJ minimum wage effect on FTE employment.** Each dot represents the estimated employment effect for a subgroup, with horizontal lines showing 95% confidence intervals. The red dashed line marks zero effect; the green dashed line marks the full-sample average (+2.75). Blue rows compare individual chains, green rows compare large vs small firms, and orange rows compare restaurants by treatment intensity (GAP). KFC is the only subgroup with a negative point estimate, while Burger King and high-GAP restaurants show the strongest positive effects.

### Business and Policy Implications

**1. Moderate minimum wage increases are unlikely to cause aggregate job losses in the fast-food sector.** The positive employment effect held across most subgroups, supporting the view that fast-food employers had room to absorb higher wages — consistent with monopsony power in low-wage labor markets.

**2. The impact is not one-size-fits-all.** KFC's negative (though not statistically significant) estimate suggests that some firms may face tighter margins. Policymakers should monitor industry-specific responses rather than relying solely on aggregate statistics.

**3. Firms paying the lowest wages are not the most vulnerable — they may benefit the most.** The dose-response pattern (high-GAP restaurants gaining more jobs) suggests that the minimum wage corrects an existing market distortion where employers suppress wages below competitive levels.

---

## Paper
"Minimum Wages and Employment: A Case Study of the Fast-Food Industry in New Jersey and Pennsylvania"
Card, D., & Krueger, A. B. (1994). American Economic Review, 84(4), 772-793.

## Track
Track A: The Causal Policy Track (Difference-in-Differences)

## Research Question
Does raising the minimum wage reduce employment in the fast-food industry? Card and Krueger exploit the 1992 New Jersey minimum wage increase (from $4.25 to $5.05/hour) as a natural experiment, using Pennsylvania restaurants as a control group in a difference-in-differences framework.

## Extension: Heterogeneous Treatment Effects (HTE)
This extension examines whether the average DID effect (+2.75 FTE) masks heterogeneity across restaurants:
- **GAP variable**: measures treatment intensity (how much each restaurant had to raise wages)
- **Chain-level subgroups**: separate DID for Burger King, KFC, Roy Rogers, Wendy's
- **Firm size**: large chains (BK, KFC, Wendy's) vs small chain (Roy Rogers)
- **Visualization**: forest plot comparing all subgroup effects

Key finding: restaurants facing larger mandated wage increases experienced greater employment gains, consistent with a monopsony labor market interpretation.

## Data Source
Original dataset (public.dat) downloaded from David Card's Berkeley data archive:
https://davidcard.berkeley.edu/data_sets.html

## Repository Structure
```
├── README.md
├── data/
│   ├── raw/ (Original paper data)
│   └── codebook
├── notebooks/
│   ├── 01_Data_Cleaning.ipynb
│   ├── 02_Replication_Analysis.ipynb
│   └── 03_Extension_and_Results.ipynb
└── .gitignore
```

## GenAI Disclosure
This project used Claude (Anthropic) to assist with extension design, Python code for subgroup DID regressions, and forest plot visualization. All AI-generated code was reviewed, tested, and validated by the author. Full prompt details are documented in the Phase 3 notebook.
