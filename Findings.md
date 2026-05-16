# Economic Interpretation & Key Findings
## Macroeconomic Regime Analysis of the 2008 Financial Crisis

---

## 1. Regime Classification & Structural Breaks

The three-regime decomposition — **Pre-Crisis (2005–2007)**, **Crisis (2008–2009)**, and **Post-Crisis (2010–2012)** — is not an arbitrary periodisation. Each boundary corresponds to an identifiable structural break in the data-generating process:

- **Q3 2007**: Bear Stearns liquidates two hedge funds heavily exposed to subprime mortgage-backed securities. The interbank lending market begins seizing — LIBOR-OIS spreads widen sharply, signalling stress in short-term funding markets before any major equity correction.
- **September 2008**: Lehman Brothers files for bankruptcy. This is the canonical break point — the moment counterparty risk became unquantifiable and the crisis transitioned from a sectoral (housing/credit) shock to a systemic one.
- **Q2 2009**: S&P 500 bottoms out (March 2009); GDP contraction slows. The Fed's emergency facilities (TALF, CPFF) and fiscal stimulus (ARRA, February 2009) begin stabilising the system.

**What the data shows:** Mean GDP growth across the three regimes shifts from positive in Pre-Crisis, to sharply negative in Crisis (annualised contraction of approximately 4% at the trough in Q4 2008), to a slow positive recovery. Variance in all indicators increases in the Crisis regime — consistent with the theoretical prediction that uncertainty rises during financial stress.

---

## 2. Cross-Asset Correlation & Contagion

**Finding:** Pairwise correlations between the S&P 500, Housing Price Index (HPI), and CPI increase substantially in the Crisis regime relative to the Pre-Crisis baseline.

**Economic interpretation:**

In normal times, equity markets and housing markets are driven by partially independent factors — corporate earnings and risk appetite on one side, mortgage credit conditions and local supply/demand on the other. The Pre-Crisis correlation between S&P 500 and HPI is moderate, reflecting the fact that both are exposed to the common factor of broad economic expansion, but not tightly coupled.

During the crisis, this decoupling collapses. The mechanism is balance sheet contagion: financial institutions held both mortgage-backed securities (housing exposure) and equity positions. As MBS values declined, institutions faced margin calls and were forced to liquidate equity holdings, mechanically transmitting the housing shock into equity markets. This is precisely the **portfolio contagion channel** described by Kyle & Xiong (2001).

Forbes & Rigobon (2002) warn that measured correlation increases during high-volatility periods partly reflect a statistical artefact — heteroskedasticity bias — rather than a true change in transmission. Even accounting for this, the magnitude of co-movement during 2008 is too large to be explained by bias alone, suggesting genuine contagion rather than mere interdependence.

**Implication for risk management:** Pre-crisis portfolio models (including Value-at-Risk models used by major banks) assumed stable correlation matrices. The crisis demonstrated that correlations are regime-dependent, and that diversification benefits evaporate precisely when they are most needed — a fundamental failure of models calibrated on tranquil-period data.

---

## 3. Housing Price Index as a Leading Indicator

**Finding:** HPI begins declining in **mid-2006**, approximately 18–24 months before the GDP contraction that defines the Crisis regime onset.

**Economic interpretation:**

This leading relationship is consistent with the **wealth effect channel** of monetary transmission: household net worth is heavily concentrated in residential real estate (for median US households, home equity constitutes the majority of wealth). A sustained decline in HPI reduces household net worth, triggering a contraction in consumption via the wealth effect — which feeds through to GDP with a lag.

The HPI decline also preceded the equity market peak (October 2007) by roughly 12 months, suggesting that the subprime stress was visible in housing data well before it was priced into equity markets — a significant failure of market efficiency in the semi-strong sense.

This sequencing — HPI → equity markets → GDP — is consistent with Reinhart & Rogoff's (2009) empirical finding across 800 years of financial crises that real estate price declines are among the most reliable leading indicators of banking crises.

---

## 4. Federal Funds Rate & Monetary Transmission

**Finding:** The Federal Funds Rate peaks at 5.25% in June 2006, remains elevated through mid-2007, then is cut aggressively from September 2007 onward — reaching the effective zero lower bound (0–0.25%) by December 2008, where it remained until 2015.

**Economic interpretation:**

Evaluated against a simple **Taylor Rule** benchmark:

```
r = 2% + π + 0.5(π − 2%) + 0.5 × output_gap
```

The Fed's rate in 2006–2007 appears roughly consistent with a Taylor prescription given the prevailing inflation and output gap estimates. The critique — made prominently by Taylor (2009) himself — is that rates were held too low for too long in 2003–2005 (the post-dot-com-bust period), providing the cheap credit that fuelled the housing boom. This is visible in the data: the Fed Funds Rate was below 2% for nearly three years (2003–2005) while HPI was accelerating.

The **transmission lag** from rate cuts to real economic impact is visible in the data: the most aggressive cuts (September 2007 – December 2008) did not arrest GDP contraction until mid-2009, consistent with the standard monetary economics finding that policy operates with a lag of 6–18 months. At the zero lower bound, conventional monetary policy was exhausted — the Fed shifted to unconventional tools (quantitative easing, forward guidance), which operate through different transmission channels (long-term rate compression, portfolio rebalancing).

---

## 5. CPI Dynamics & the Debt-Deflation Mechanism

**Finding:** CPI inflation, which was running at approximately 4–5% in mid-2008 (partly driven by oil price spikes), collapsed sharply in the second half of 2008 and briefly turned negative in 2009.

**Economic interpretation:**

The deflationary pressure of 2008–09 is particularly significant because deflation in the presence of high nominal debt loads activates the **Fisher debt-deflation mechanism** (Fisher, 1933): falling prices increase the real value of outstanding debt, which worsens borrower balance sheets, leading to further deleveraging, further demand contraction, and further price declines — a self-reinforcing spiral.

This dynamic was the Fed's central concern in late 2008 and drove the urgency of unconventional monetary interventions. The parallels to Japan's "lost decade" (1990s) — where mild deflation combined with debt overhang produced a prolonged demand deficiency — shaped Fed Chairman Bernanke's (a scholar of the Great Depression) policy calculus.

**The oil price spike and reversal** visible in mid-2008 CPI data is a separate supply-side shock: Brent crude peaked at approximately $147/barrel in July 2008 before collapsing to under $40 by December 2008. This commodity price cycle, interacting with the financial crisis, produced the sharp CPI spike-then-collapse pattern observed in the data.

---

## 6. Summary of Regime-Wise Statistics

| Indicator | Pre-Crisis (2005–07) | Crisis (2008–09) | Post-Crisis (2010–12) |
|-----------|---------------------|-----------------|----------------------|
| GDP Growth (approx.) | +2.5% to +3.5% | −4% (trough) | +2% to +2.5% |
| S&P 500 Trend | Rising | −57% peak to trough | Recovering |
| HPI Trend | Peak → Declining | Sharply declining | Stabilising |
| CPI | Moderate / rising | Spike then deflationary | Moderate |
| Fed Funds Rate | 5.25% → cutting | Cutting → 0% | 0–0.25% |
| Cross-asset Correlation | Moderate | Elevated (contagion) | Normalising |

---

## 7. Limitations & Extensions

- **Causality vs. correlation:** The analysis establishes co-movement and temporal sequencing but does not formally identify causal relationships. A rigorous treatment would employ Granger causality tests or a structural VAR (SVAR) model to identify the direction and magnitude of transmission between series.
- **Unit root testing:** The series are likely non-stationary in levels. A full econometric treatment would begin with ADF (Augmented Dickey-Fuller) or KPSS tests and work with first differences or cointegrated specifications where appropriate.
- **International spillovers:** The analysis is confined to US data. The 2008 crisis had substantial international transmission (European banking crisis, global trade collapse) which is not captured here.
- **High-frequency data:** Monthly/quarterly data smooth over intra-period dynamics. Key contagion events (Lehman weekend, money market fund breaks) played out over days, which is not visible in the frequency used.

---

## References

- Bernanke, B. S. (2015). *The Courage to Act*. W. W. Norton.
- Fisher, I. (1933). The debt-deflation theory of great depressions. *Econometrica*, 1(4), 337–357.
- Forbes, K. J., & Rigobon, R. (2002). No contagion, only interdependence. *Journal of Finance*, 57(5), 2223–2261.
- Hamilton, J. D. (1989). A new approach to the economic analysis of nonstationary time series. *Econometrica*, 57(2), 357–384.
- Kyle, A. S., & Xiong, W. (2001). Contagion as a wealth effect. *Journal of Finance*, 56(4), 1401–1440.
- Reinhart, C. M., & Rogoff, K. S. (2009). *This Time is Different: Eight Centuries of Financial Folly*. Princeton University Press.
- Taylor, J. B. (1993). Discretion versus policy rules in practice. *Carnegie-Rochester Conference Series on Public Policy*, 39, 195–214.
- Taylor, J. B. (2009). *Getting Off Track: How Government Actions and Interventions Caused, Prolonged, and Worsened the Financial Crisis*. Hoover Institution Press.
