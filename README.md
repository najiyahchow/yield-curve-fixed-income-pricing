# Yield Curve Construction and Fixed-Income Pricing

This project investigates how the representation and interpolation of the
yield curve affect the valuation and interest-rate risk of fixed-income
instruments.

Two simple curve-construction approaches are implemented and compared:
linear interpolation of continuously compounded zero rates and linear
interpolation of discount factors. The resulting curves are used to price
bonds and a plain-vanilla interest-rate swap and to calculate key risk
measures.

## Research question

How materially does the choice of yield-curve interpolation method affect
instrument valuation and measured interest-rate sensitivity?

## Project scope

The project covers:

- construction of discount, zero-rate and forward curves;
- comparison of two interpolation methods;
- pricing of a fixed-rate coupon bond;
- Macaulay duration, convexity and DV01;
- calculation of par swap rates;
- valuation of a plain-vanilla interest-rate swap;
- parallel yield-curve shocks and finite-difference risk measures.

The implementation deliberately uses simplified assumptions so that the
mathematics and numerical effects remain transparent. Production-level
market conventions, multi-curve frameworks and stochastic interest-rate
models are outside the scope.

## Project structure

- `01_curve_construction.ipynb` compares linear interpolation of zero rates
  with linear interpolation of discount factors and examines the resulting
  zero, discount and instantaneous forward curves.
- `02_bond_pricing_and_risk.ipynb` studies how the two term structures affect
  coupon-bond valuation, Macaulay duration, DV01 and convexity.
- `03_interest_rate_swap_valuation.ipynb` compares par swap rates, off-market
  swap values and DV01 under the two curve constructions.

## Key findings

Both interpolation methods reproduce the same quoted market inputs but generate
different term structures between quoted maturities. These differences are more
visible in implied forward rates than in zero rates.

For the instruments considered, interpolation choice produces measurable
differences in bond and swap valuation, while parallel-rate risk measures such
as DV01 remain very similar under the two curve constructions.
