# Betting-Against-Beta


## Methodology
1. **Data Preparation**  
   - Collected U.S. equity data from CRSP (monthly returns) and Fama-French factors.  
   - Constructed decile portfolios sorted on beta, Operating Profit (OP), Earnings/Price (E/P), and Dividend Yield (D/P).  

2. **Portfolio Construction**  
   - Long/short strategies:  
     - BAB → Long low-beta, short high-beta.  
     - Factor sorts → Long high decile, short low decile for OP, E/P, and D/P.  

3. **Performance Analysis**  
   - Summary statistics: mean, standard deviation, skewness, kurtosis.  
   - **CAPM regressions** → to estimate alpha, beta, and market exposure.  
   - **Fama-French 3-factor regressions** → to evaluate size/value influences.  

---

## Findings

### Betting Against Beta (BAB)
- **Value-weighted portfolios**:  
  - Low-beta (Lo 10) portfolios outperformed high-beta (Hi 10) on a risk-adjusted basis.  
  - Long-short BAB portfolio delivered positive mean return (0.441) with negative market beta (−0.400), suggesting hedging properties.
  - CAPM regressions showed strong positive alphas for low-beta and BAB portfolios.  

- **Equal-weighted portfolios**:  
  - Higher beta portfolios yielded higher raw returns, but the BAB long-short still produced significant alpha (0.509) in Fama-French regressions.
  - BAB strategy remained robust even after adjusting for SMB and HML factors.  

**Conclusion**: BAB portfolios generate **positive abnormal returns**, confirming the leverage constraint hypothesis from Frazzini & Pedersen (2014).

---

### Extended Factor Sorts
- **Operating Profit (OP)**:  
  - Higher profitability associated with stronger returns, consistent with Fama & French (2015) and Novy-Marx (2013).  
  - Long-short OP portfolios showed positive alphas, though statistical significance varied.  

- **Earnings/Price (E/P)**:  
  - High E/P decile (Hi 10) achieved the strongest mean return (1.048), highly significant (p < 0.001).  
  - Long-short E/P portfolios produced large positive alphas, supporting classic evidence from Basu (1983).  

- **Dividend Yield (D/P)**:  
  - High-dividend portfolios generated superior returns with statistically significant excess performance.  
  - D/P long-short portfolio also exhibited high skewness and kurtosis, suggesting fatter tails and potential risk of extremes.  

**Conclusion**: Profitability, valuation, and income-based sorts all yield **statistically significant abnormal returns**, reinforcing their role as explanatory factors in the cross-section of stock returns.

---

## Requirements
Install required packages before running:
```bash
pip install pandas numpy matplotlib seaborn statsmodels
