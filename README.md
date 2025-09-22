# Stock Portfolio Analysis (Python)

A hands-on project that analyzes stock portfolios using **pandas**, **yfinance**, and **matplotlib**.  
The script downloads historical price data, builds a weighted portfolio, benchmarks performance against the **S&P 500**, and produces both **visualizations** and a **metrics summary (CSV + Markdown table)**.

### Why this matters
This project demonstrates practical skills in:
- Financial data extraction and cleaning (via yfinance & pandas)  
- Portfolio return/volatility analysis and benchmarking  
- Risk-adjusted performance measurement (Sharpe ratio, CAGR)  
- Data visualization with matplotlib  
- Reproducible workflows (config-driven + version-controlled outputs)  

---

## Metrics (from `summary/metrics.csv`)

|           | Total Return | CAGR   | Ann. Volatility | Sharpe (rf=0) |
|-----------|--------------|--------|-----------------|---------------|
| Portfolio | 273.2%       | 62.9%  | 26.5%           | 1.98          |
| S&P 500   | 74.3%        | 22.9%  | 15.3%           | 1.42          |

**Metric Definitions**
- **Total Return**: Overall growth of the portfolio for the selected period.  
- **CAGR (Compound Annual Growth Rate)**: Average yearly growth rate, smoothing out volatility.  
- **Ann. Volatility**: How much the portfolio fluctuates day-to-day, annualized. Lower = more stable.  
- **Sharpe (rf=0)**: Risk-adjusted return. A higher Sharpe ratio means better returns per unit of risk.  

---

## Quick Start
```bash
python -m venv .venv
# macOS/Linux
source .venv/bin/activate
# Windows (PowerShell)
# .venv\Scripts\Activate.ps1

pip install -r requirements.txt
python portfolio_analysis.py
