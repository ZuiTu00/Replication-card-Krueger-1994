# Replication Study: Card & Krueger (1994)

## Paper
"Minimum Wages and Employment: A Case Study of the Fast-Food Industry in New Jersey and Pennsylvania"
Card, D., & Krueger, A. B. (1994). American Economic Review, 84(4), 772-793.

## Track
Track A: The Causal Policy Track (Difference-in-Differences)

## Research Question
Does raising the minimum wage reduce employment in the fast-food industry? Card and Krueger exploit the 1992 New Jersey minimum wage increase (from $4.25 to $5.05/hour) as a natural experiment, using Pennsylvania restaurants as a control group in a difference-in-differences framework.

## Data Source
Original dataset (public.dat) downloaded from David Card's Berkeley data archive:
https://davidcard.berkeley.edu/data_sets.html

## Repository Structure
- data/raw/ — Original data files (public.dat, codebook)
- data/processed/ — Cleaned output files
- notebooks/ — Analysis notebooks
## Phase 3: Extension — Heterogeneous Treatment Effects
This extension examines whether the average DID effect (+2.75 FTE) masks heterogeneity across restaurants. Analysis includes:
- **GAP variable**: measures treatment intensity (how much each restaurant had to raise wages)
- **Chain-level subgroups**: separate DID for Burger King, KFC, Roy Rogers, Wendy's
- **Firm size**: large chains vs small chain
- **Visualization**: forest plot comparing all subgroup effects

Key finding: restaurants facing larger mandated wage increases experienced greater employment gains, consistent with a monopsony labor market interpretation.
