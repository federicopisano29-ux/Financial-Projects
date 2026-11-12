# Financial Projects Portfolio

This repository brings together a collection of projects developed in the field of finance, covering different areas of financial analysis, valuation, risk management and derivatives.
Currently, the repository includes projects focused on:
- Corporate Valuation: Company valuation methodologies, including the analysis of RETI S.p.A. using DCF, Total Cash Flow, APV and Equity Approaches.
- Quantifying Extreme Risk in Commodity Prices: Analysis and measurement of extreme market risk in commodity markets.
- Derivatives: Exploration and practical application of derivative instruments, pricing methodologies and financial models.

These projects represent an ongoing effort to deepen, test and put into practice the knowledge and skills acquired through academic studies and independent learning.
They are not intended to be perfect or definitive solutions. Rather, they document a learning process: experimenting with methodologies, confronting practical challenges, making mistakes and improving along the way.
The repository will continue to evolve as new projects, ideas and areas of interest are explored.

*---------------------------------------------------------------------------------------*

# Quantifying-Extreme-Risk-in-Commodity-Prices
Quantifying Extreme Risk in Commodity Prices under Systemic Stress Evidence from Gold and Brent. Focused on the measurement and analysis of market and tail risk. The project combines traditional risk measures with statistical and simulation-based approaches to investigate the behavior of portfolio losses under normal and extreme market conditions.

The MATLAB code is provided in two formats, so it can be consulted, run, or reviewed depending on what the reader needs:
-	`Commodities_Analysis.mlx`	
- `Commodities_Analysis.pdf`	— for quick consultation without opening MATLAB.

**Overview**
Extreme movements in commodity prices are a first-order concern for investors, risk managers, and regulators: sharp shocks in energy and precious-metal markets can trigger inflationary pressure, destabilize budgets, and expose portfolios to losses that classical Gaussian risk models systematically underestimate.
This project builds and validates a quantitative framework, combining GARCH-based conditional volatility filtering with Extreme Value Theory
(EVT) — to estimate tail risk in two commodities with structurally different risk profiles: Gold (GC_F), traditionally viewed as a safe-haven asset, and Brent Crude Oil (CO_F), which is more exposed to geopolitical and supply-side shocks. The analysis uses daily data from 2000 to 2023, a window that includes the 2008 global financial crisis, the COVID-19 shock, and the onset of the
Russia-Ukraine war.

**Methodology pipeline**
1. Data preparation — log-returns, outlier handling, stationarity (ADF).
2. Diagnostics — ACF/PACF, Ljung-Box, ARCH-LM, Jarque-Bera, D'Agostino-Pearson, Turning Point test.
3. AR(1)-GARCH(1,1) with Student-t innovations — conditional volatility
4. filtering to obtain approximately i.i.d. standardized residuals.
5. EVT-POT — threshold selection (Mean Excess plot, parameter stability, Anderson-Darling / Cramér-von Mises goodness-of-fit), GPD parameter
estimation (MLE), VaR/CVaR at 95%, 97%, 99%.
6. Monte Carlo backtesting — 10,000 simulations per crisis window (2008, COVID-19, Ukraine war), Kupiec unconditional coverage,
Christoffersen conditional coverage, Clopper-Pearson confidence intervals.

**Results summary**
- EVT materially improves tail-risk estimation.
- Across confidence levels (95%, 97%, 99%), observed VaR exceedance rates deviate less than 5% from theoretical expectations, and both Kupiec and Christoffersen coverage tests fail to reject correct model specification in almost every scenario tested. 
- **Gold behaves as a partial safe haven**. Its estimated tail index (ξ ≈ 0.11–0.15) is lower than Brent's, VaR/CVaR violations are rarer than
theoretically expected, and the model shows a mildly conservative bias, consistent with lower, more stable extreme-loss exposure.
-** Brent shows heavier, less stable tails**. Higher estimated tail index (ξ ≈ 0.25–0.30, depending on the crisis window), larger VaR/CVaR magnitudes,
and a higher concentration of violations during acute shock episodes (e.g. the 2008 collapse, the March–April 2020 COVID-19 sell-off), reflecting its
greater sensitivity to supply and geopolitical shocks.
- **The framework is robust but not adaptive**. In all three crisis windows the model recalibrates quickly after an initial cluster of violations, and no statistically significant autocorrelation in exceedances is detected.
- However, the static threshold used in the POT step is a **known limitation**: results point to time-varying/rolling thresholds as a natural extension for faster adaptation to sudden regime changes (see thesis, §4.8 and §5). 
- **Practical implication**: a Gaussian VaR/CVaR approach would systematically understate tail risk for both assets, and especially for Brent during acute stress — supporting the case for GARCH-EVT-based frameworks in stress-testing and capital-adequacy contexts for commodity exposures.

*---------------------------------------------------------------------------------------*

# COMPANY VALUATION

**Example of RETI S.p.A.** 

**Project Overview**
This project focuses on the valuation of RETI S.p.A., applying multiple financial valuation methodologies to estimate the company's intrinsic value and assess its financial and economic profile.
The analysis combines cash flow-based valuation approaches, capital structure considerations and equity valuation techniques, with the objective of comparing different valuation perspectives and understanding how financing decisions influence enterprise and equity value.

**Valuation Methodologies**
The financial model incorporates the following approaches:
- Discounted Cash Flow (DCF): valuation based on projected Free Cash Flow to the Firm (FCFF), discounted using the Weighted Average Cost of Capital (WACC).
- Total Cash Flow (TCF): valuation through the analysis and discounting of total cash flows generated for debt and equity capital providers.
- Adjusted Present Value (APV): separation of the operating value of the business from the financial effects of leverage, including the value of interest tax shields.
- Equity Approach (FCFE): direct estimation of equity value by discounting Free Cash Flow to Equity at the Cost of Equity (Ke).

**Key Areas of Analysis**
The project includes:
- Historical financial statement analysis.
- Revenue, operating performance and profitability assessment.
- Forecasting of financial statements and operating cash flows.
- Estimation of WACC and Cost of Equity.
- Capital structure and financial leverage analysis.
- Terminal Value estimation.
- Net Debt and Enterprise Value reconciliation.
- Equity Value determination.
- Comparison of valuation results across different methodologies.

**Objective**
The primary objective is to develop an integrated valuation framework, comparing alternative methodologies and examining the impact of operating assumptions, financial leverage, discount rates and long-term growth expectations on the estimated company value.
The project also aims to demonstrate the practical application of corporate finance theory to a real-world listed company.

**Tools & Technologies**
- Microsoft Excel
- Financial Modelling
- Corporate Finance
- Business Valuation
- Discounted Cash Flow Analysis

**Disclaimer**
This project has been developed for educational and analytical purposes. The valuation estimates are based on financial information, assumptions and projections used in the model and should not be interpreted as investment recommendations.
