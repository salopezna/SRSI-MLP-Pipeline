# SRSI-MLP-Pipeline
Find optimal parameters (K, D, RSI Length, Stoch Length, Source) for a Stochastic RSI indicator that best detects overbought/oversold zones across assets (futures + crypto).

# SRSI-MLP-Pipeline

Pipeline cuantitativo basado en Marcos López de Prado (AFML/MLAM) para optimizar los parámetros de **Stochastic RSI** y detectar zonas de sobrecompra/sobreventa con precisión adaptativa.

## Objetivo
Encontrar las combinaciones óptimas de K, D, RSI Length, Stoch Length y Source que maximicen aciertos de reversión en activos **futuros y cripto**.

## Arquitectura
- **Data:** OHLCV minuto a minuto (Databento GLBX.MDP3 + BINANCE.SPOT)
- **Features:** SRSI, volatilidad, tendencia, momentum, volumen, estructura, régimen, correlaciones
- **Labeling:** Triple-Barrier + Meta-Labeling
- **Modelos:** LightGBM + Optimización Bayesiana/Genética
- **Validación:** Walk-Forward + Purged K-Fold + Embargo
- **Visualización:** Lightweight Charts / DXCharts

## Instalación
```bash
git clone git@github.com:TUUSER/srsi-mlp-pipeline.git
cd srsi-mlp-pipeline
pip install -r requirements.txt
cp .env.example .env   # agrega tu DATABENTO_API_KEY
