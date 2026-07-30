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
- pricing of zero-coupon and fixed-coupon bonds;
- duration, convexity and DV01;
- calculation of par swap rates;
- valuation of a plain-vanilla interest-rate swap;
- parallel and non-parallel yield-curve shocks.

The implementation deliberately uses simplified assumptions so that the
mathematics and numerical effects remain transparent. Production-level
market conventions, multicurve frameworks and stochastic interest-rate
models are outside the scope.
