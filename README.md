# Time Series Analysis - ArcelorMittal & Eurostat

Academic project on financial and macroeconomic time series modeling.

## Context

**Université Paris-Dauphine - PSL**  
M2 ISF - Time Series and Actuarial Applications  
Academic Year 2025/2026

**Author:** Arthur Danjou  
**Supervisor:** Tachine El Alami (Cérémade)

## Objectives

This project applies time series methods to two domains:

1. **Financial Markets**: Analysis of ArcelorMittal returns (CAC40, 2000-2010)
   - Conditional heteroskedasticity modeling (GARCH)
   - Capture of *volatility clustering* phenomenon

2. **Macroeconomics**: Analysis of Eurostat series (GDP, industrial production)
   - Univariate modeling (SARIMA)
   - Multivariate modeling (VAR)
   - Evaluation against exogenous shocks (2020 break)

## Structure

```
├── data/
│   ├── DANJOU_CAC40_ARCELOR.MITTAL.csv    # Daily ArcelorMittal prices
│   └── DANJOU_EcoSeriePIB.csv              # Eurostat macroeconomic series
├── Projet_DANJOU_Arthur.qmd                # Main Quarto notebook
└── Projet_DANJOU_Arthur.pdf                # Generated report
```

## Data

### ArcelorMittal
- **Source**: CAC40
- **Period**: 2000-2010
- **Frequency**: Daily (monthly aggregation used)
- **Variables**: Closing prices

### Eurostat
- **Period**: 1990-2021
- **Frequency**: Quarterly
- **Variables**: GDP, EUR/USD exchange rate, debt, interest rates, industrial production, etc.

## Requirements

R (>= 4.0) with packages:

```r
install.packages(c(
  "dplyr", "ggplot2", "tseries", "patchwork",
  "forecast", "fGarch", "FinTS", "lmtest",
  "corrplot", "vars"
))
```

## Execution

```bash
quarto render Projet_DANJOU_Arthur.qmd --to typst
```

Or in RStudio: open `Projet_DANJOU_Arthur.qmd` and click *Render*.

## Methodology

1. Data import and visualization
2. Stationarity tests (ADF, PP, KPSS)
3. Model identification (ACF/PACF)
4. Estimation and diagnostics (residuals, white noise tests)
5. Validation and out-of-sample forecasting

## License

Academic project - Université Paris-Dauphine
