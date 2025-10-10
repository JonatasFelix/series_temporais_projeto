# Projeto – Análise de Séries Temporais e Regressão

## Série utilizada

- Arquivo: `solar france.xlsx`

- Coluna temporal detectada: `Date and Hour`

- Coluna alvo detectada: `Production`

## Metodologia

- Split temporal: **50% / 25% / 25%** (ordem preservada)

- **ARIMA/SARIMA (Box–Jenkins)** – Seleção via AIC e teste de Ljung–Box

- **KNN** – Lags + estatísticas móveis; parâmetros ajustados por validação

- **VGG-1D** – CNN 1D com janelas deslizantes; early stopping via validação

- **Híbridos** – Residual Stacking e Ensemble ponderado (pesos via validação)

## Comparação (MSE / MAPE)

| Modelo                   |   MSE_train |    MAPE_train |   MSE_val |      MAPE_val |   MSE_test |   MAPE_test |
|:-------------------------|------------:|--------------:|----------:|--------------:|-----------:|------------:|
| ARIMA                    |  10732      |   5.75113e+10 |  19206    |   1.26794e+11 |    21511.9 | 1.12705e+11 |
| KNN                      |     22.5075 |   5.41726e+09 |  49825.9  |   4.89194e+09 |   144300   | 1.09218e+09 |
| VGG1D(w=24, f=64, d=0.2) |   2457.54   |   1.82441e+10 |   8206.37 |   2.05438e+10 |    23071.4 | 2.10142e+10 |
| HÍBRIDO-RESIDUAL         |    nan      | nan           |    nan    | nan           |    28466.5 | 1.45634e+11 |
| HÍBRIDO-ENSEMBLE         |    nan      | nan           |    nan    | nan           |    13460.6 | 4.41365e+10 |