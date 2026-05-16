# Macroeconomic Regime Analysis of the 2008 Financial Crisis
### Structural Breaks, Cross-Asset Correlation & Monetary Transmission

---

## Overview

This project analyses the 2008 Global Financial Crisis through the lens of macroeconomic regime decomposition and financial contagion theory. Using a dataset of key US macroeconomic indicators, the analysis examines how GDP, equity markets, inflation, housing prices, and monetary policy co-evolved across three distinct regimes — Pre-Crisis (2005–2007), Crisis (2008–2009), and Post-Crisis (2010–2012) — and quantifies the breakdown in cross-asset correlation structure that is characteristic of systemic financial stress.

The goal is not merely descriptive visualisation, but an empirically grounded examination of how monetary transmission mechanisms, asset price dynamics, and macroeconomic fundamentals interact during periods of financial instability.

---

## Theoretical Framework

### 1. Regime Decomposition & Structural Breaks

The three-phase decomposition used in this analysis is motivated by the Markov regime-switching framework introduced by Hamilton (1989), in which an economy is modelled as transitioning between latent states — expansion and contraction — governed by a transition probability matrix. While this project applies a deterministic phase classification rather than a full Markov chain estimation, the underlying intuition is identical: macroeconomic relationships are non-stationary across regimes, and pooling observations across phases obscures the structural shifts of interest.

The identification of the crisis regime onset (Q3 2007 – Bear Stearns hedge fund collapse; September 2008 – Lehman Brothers) follows the structural break literature, where a break point marks a change in the data-generating process rather than a mere outlier.

### 2. Cross-Asset Correlation & Contagion

A central observation in the crisis literature is that asset correlations — typically assumed stable in portfolio construction — increase dramatically during stress periods. Forbes & Rigobon (2002) attribute this in part to heteroskedasticity bias: when volatility rises, measured correlations rise mechanically even without a change in the true transmission channel. This project examines pairwise correlations between equity (S&P 500), housing (HPI), and inflation (CPI) across regimes as a proxy for contagion dynamics.

From a portfolio theory perspective (Markowitz, 1952), the convergence of correlations toward 1 during the crisis implies a collapse in diversification benefits — a key failure mode of pre-crisis risk models.

### 3. Monetary Transmission & the Taylor Rule

The Federal Funds Rate series is analysed as the primary instrument of monetary policy. The Taylor Rule (Taylor, 1993) prescribes:

```
r = r* + π + 0.5(π − π*) + 0.5(y − y*)
```

where `r` is the nominal rate, `π` is inflation, `π*` is the inflation target, and `(y − y*)` is the output gap. The project examines whether the Fed's rate trajectory across the crisis period was consistent with a Taylor-type rule, and analyses the lagged transmission of rate changes to CPI and GDP — the classic monetary transmission mechanism.

### 4. Non-Stationarity & Time-Series Properties

Macroeconomic time series such as GDP and CPI are typically non-stationary — they contain unit roots, meaning shocks have permanent rather than transitory effects. The analysis accounts for this by examining first differences and identifying periods of mean reversion, consistent with standard practice in applied econometrics (Engle & Granger, 1987).

---

## Data

- **Source:** US Recession Dataset (Kaggle), derived from FRED (Federal Reserve Economic Data)
- **Indicators:** GDP, S&P 500 Index, Consumer Price Index (CPI), Housing Price Index (HPI), Federal Funds Rate
- **Frequency:** Monthly / Quarterly
- **Period:** Approximately 2000–2012

---

## Methodology

| Step | Description |
|------|-------------|
| Data Cleaning | Handled missing values, aligned time indices across series |
| Regime Classification | Manual structural break identification at Q3 2007 and Q3 2009 |
| Time-Series Analysis | Trend decomposition, phase-wise mean and variance comparison |
| Correlation Analysis | Pairwise correlation heatmaps across full sample and by regime |
| Monetary Transmission | Rate change event study around FOMC decisions; lagged effects on CPI and GDP |
| Visualisation | Annotated time-series plots marking key crisis events (Bear Stearns, Lehman, TARP) |

---

## Key Findings

- **Correlation structure is regime-dependent.** Cross-asset correlations between equity and housing markets rise substantially during the crisis regime, consistent with contagion dynamics described by Forbes & Rigobon (2002). Pre-crisis correlations understate systemic co-movement.

- **GDP contraction is preceded by HPI deterioration.** The Housing Price Index begins declining in 2006, approximately 18 months before the GDP contraction registers — consistent with the narrative of a housing-led transmission into the real economy.

- **Federal Funds Rate reduction lags the equity market shock.** The S&P 500 peak (October 2007) precedes the most aggressive Fed rate cuts by several months, raising questions about the timeliness of monetary transmission under the prevailing policy framework.

- **CPI dynamics diverge sharply across regimes.** Pre-crisis inflation is moderate and trending; crisis-period CPI exhibits deflationary pressure (2008–09) before recovering — a pattern consistent with Fisher's debt-deflation theory.

---

## Repository Structure

```
├── data/
│   └── us_recession_data.csv
├── notebooks/
│   └── financial_crisis_analysis.ipynb
├── figures/
│   └── (all output plots)
└── README.md
```

---

## References

- Forbes, K. J., & Rigobon, R. (2002). No contagion, only interdependence: measuring stock market comovements. *Journal of Finance*, 57(5), 2223–2261.
- Hamilton, J. D. (1989). A new approach to the economic analysis of nonstationary time series and the business cycle. *Econometrica*, 57(2), 357–384.
- Markowitz, H. (1952). Portfolio selection. *Journal of Finance*, 7(1), 77–91.
- Taylor, J. B. (1993). Discretion versus policy rules in practice. *Carnegie-Rochester Conference Series on Public Policy*, 39, 195–214.
- Engle, R. F., & Granger, C. W. J. (1987). Co-integration and error correction: representation, estimation, and testing. *Econometrica*, 55(2), 251–276.
- Bernanke, B. S. (2015). *The Courage to Act: A Memoir of a Crisis and Its Aftermath*. W. W. Norton.
- Fisher, I. (1933). The debt-deflation theory of great depressions. *Econometrica*, 1(4), 337–357.
