# Price Elasticity of Demand Analysis

A linear regression study of price elasticity of demand (PED) and price optimization, applied to a 1,000-observation price/quantity dataset (`price_data.csv`). The full walkthrough lives in `final.ipynb`, built with `pandas` and `statsmodels`.

## Method

1. EDA: descriptive statistics, price and quantity histograms, scatter plot, correlation (Pearson r = -0.22).
2. Log transform of strictly positive prices and quantities.
3. Linear demand model: OLS regression of `Quantity ~ Price` with full diagnostics.
4. Point elasticity at the sample means: `PED = b * (P_mean / Q_mean)`.
5. Price optimization: revenue and profit curves over a price grid (unit cost = 40).

## Results

- Estimated demand curve: `Q = 2889.25 - 6.64 P` (slope t = -7.15, p < 0.001, 95% CI [-8.46, -4.82]; R-squared = 0.049).
- PED at the means: -0.79, so demand is inelastic across the observed range.
- Revenue-maximizing price: about 216.59 (revenue about 314,344).
- Profit-maximizing price: about 236.50 at a unit cost of 40 (profit about 259,213).

## Contents

- `final.ipynb` - analysis notebook
- `price_data.csv` - 1,000 price/quantity observations

## Running it

Requires `pandas`, `numpy`, `matplotlib`, and `statsmodels`. Open `final.ipynb` and run all cells; the unit cost used for profit optimization can be changed in the optimization cell.
