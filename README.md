# Derivatives-Pricing-engine
## Black-Scholes, Monte Carlo & Heston Models
### Overview

This project develops a Python-based quantitative framework for pricing European call and put options using three approaches: the Black-Scholes analytical model, Monte Carlo simulation, and the Heston stochastic volatility model.

The framework uses historical SPY market data and U.S. Treasury yields to estimate model inputs, calculate option Greeks, and evaluate pricing results through numerical validation, put-call parity, and Monte Carlo convergence analysis.

Project Objectives

-Price European call and put options using Black-Scholes.

-Estimate option prices using Monte Carlo simulation.

-Explore stochastic volatility using the Heston model.

-Calculate option Greeks to measure price sensitivity.

-Validate pricing results using put–call parity and numerical checks.

-Analyze Monte Carlo estimation error and convergence.

-Compare pricing results under different volatility assumptions.


## Models and Methods

### Black–Scholes Model

Calculates theoretical European call and put prices using the underlying asset price, strike price, time to maturity, risk-free interest rate, volatility, and continuous dividend yield.

### Monte Carlo Simulation

Simulates future stock prices under risk-neutral geometric Brownian motion. Option payoffs are calculated at maturity and discounted to the present.

The analysis includes estimated option prices, standard errors, confidence intervals, and convergence comparisons across different simulation sizes.

### Heston Stochastic Volatility Model

Models volatility as a random process rather than assuming it remains constant. Monte Carlo simulation estimates European option prices using correlated stock-price and variance processes.

The Heston parameters are illustrative and are not calibrated to live options market data.

### Option Greeks

Calculates the main Black-Scholes sensitivities:

Delta: Sensitivity to changes in the underlying asset price.

Gamma: Sensitivity of Delta to changes in the underlying asset price.

Vega: Sensitivity to changes in volatility.

Theta: Sensitivity to the passage of time.

Rho: Sensitivity to changes in the risk-free interest rate.

Finite-difference checks are used to assess selected analytical Greek calculations.

## Market Data

The project uses the following data sources and methods:

SPY historical prices: Retrieved from Yahoo Finance using yfinance.

Risk-free interest rate: The U.S. 3-month Treasury constant-maturity rate from FRED, series DGS3MO.

Historical volatility: Estimated from rolling daily log returns and annualized using the square root of 252 trading days.

Historical volatility is used as a modeling input. It differs from implied volatility, which is derived from market option prices.


## Validation and Analysis

The pricing framework is evaluated through:

Put-call parity checks.

Comparisons between Monte Carlo estimates and Black–Scholes prices.

Monte Carlo standard errors and confidence intervals.

Convergence analysis across increasing simulation sizes.

Numerical checks of option Greeks.

A Heston special-case comparison with Black–Scholes under constant-volatility conditions.

Comparisons of model prices and sensitivities.


### Technologies

Python

NumPy

pandas

Matplotlib

SciPy

yfinance



## Limitations

Strike prices and maturities are modeling assumptions rather than inputs from a complete live options chain.

Historical volatility may differ from market-implied volatility.

The 3-month Treasury yield may not match the maturity of the option being priced.

Heston parameters are not calibrated to observed market option prices.

Monte Carlo estimates are subject to sampling error.

Results may vary with simulation settings and the date on which market data are retrieved.

## Future Improvements

Calibrate the Heston model using observed market option prices.


## Disclaimer

This project is intended for educational and research purposes only. The model outputs are theoretical estimates and should not be considered financial advice or trading recommendations.
