---

### 🧠 **context.md**
```markdown
You are assisting in building a quantitative finance research pipeline aligned with **Marcos López de Prado’s AFML/MLAM**.

Project: **SRSI-MLP-Pipeline**

Goal:
Find optimal parameters (K, D, RSI Length, Stoch Length, Source) for the Stochastic RSI indicator that best detects overbought/oversold zones across multiple assets.

Data:
- Source: Databento API
- Datasets: `GLBX.MDP3` (CBOT futures), `BINANCE.SPOT` (crypto)
- Schema: `ohlcv-1m`

Modules:
1. Data acquisition + cleaning  
2. Feature engineering (SRSI, volatility, trend, momentum, volume, structure, regime, cross-asset)  
3. Labeling (Triple-Barrier + Meta-Labeling)  
4. Modeling (LightGBM / Bayesian Opt / GA)  
5. Validation (Walk-Forward + Purged K-Fold + Embargo)  
6. Visualization (Lightweight Charts / DXCharts)

Rules:
- No look-ahead or leakage  
- Purge overlaps and embargo horizons  
- Use AUC-PR, MCC, Sharpe for evaluation  
- Log experiments and ensure reproducibility  
- Read API key from `.env` via `dotenv`  
- Code must be modular, robust, and production-ready

Environment:
Python 3.11 | VS Code / Cursor | GitHub repo `srsi-mlp-pipeline`
