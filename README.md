# SQL-NYSE-Market-Performance-Risk-Drivers
SQL-first equity analytics on NYSE-listed stocks using **daily split-adjusted prices** + **company fundamentals** (Kaggle “NYSE” dataset: `prices-split-adjusted.csv`, `securities.csv`, `fundamentals.csv`). The goal is simple: translate real investor questions into **clean, reproducible SQL outputs** (ranked tables + concise insights).

---

## What this demonstrates 
- **Market reasoning → metrics:** returns, sector leadership, liquidity, volatility/drawdowns, risk-adjusted performance, fundamental screens  
- **Strong SQL fundamentals:** CTEs, joins, window functions (`LAG`), ranking, bucketing (`CASE`), aggregation sanity checks  
- **Reproducibility:** one query suite that regenerates the same tables end-to-end

---

## Analyses included (2016 unless stated)
1. **Liquidity:** top stocks by average daily **$ volume**  
2. **Sector performance:** sector-level average returns + dispersion  
3. **Outliers:** biggest winners/losers (tail behavior)  
4. **Risk:** most volatile names  
5. **Risk-adjusted performance:** “Sharpe-like” (0% RF, annualized from daily)  
6. **Growth (2012→2015):** revenue CAGR leaders  
7. **Profitability (2015):** sector **weighted net margin**  
8. **Pattern test:** 2015 margin buckets vs 2016 returns (rebound/mean reversion)  
9. **Balance-sheet risk:** sector leverage (2015) vs volatility (2016)

---

## Key insights (from the outputs)
- Liquidity concentrates in **mega-caps** and large banks; Tech + Financials dominate tradability.
- **Energy** leads raw 2016 returns (rebound), but also carries extreme volatility.
- **Financials / Industrials** look strongest on risk-adjusted terms vs high-vol sectors.
- Revenue growth leaders cluster in **Health Care / Real Estate** (growth ≠ profitability).
- Negative-margin firms show stronger next-year returns (rebound), while “quality” can be priced in.
- Volatility is not explained by leverage alone (Energy is the clearest counterexample).

---

## Repo layout

```text
SQL-NYSE-Market-Performance-Risk-Drivers/
├─ README.md
├─ NYSE_SQL-Analytics_Prices+Fundamentals.ipynb
└─ data /
   └─ data.7z /
      ├─ prices.csv
      ├─ securities.csv
      ├─ prices-split-adjusted.csv
      └─ fundamentals.csv
