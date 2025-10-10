# Projeto – Análise de Séries Temporais e Regressão

## Série utilizada

- Arquivo: `household_consumption.xlsx`

- Coluna temporal detectada: `Date and Hour`

- Coluna alvo detectada: `Consumption`

## Metodologia

- Split temporal: **50% / 25% / 25%** (ordem preservada)

- **ARIMA/SARIMA (Box–Jenkins)** – Seleção via AIC e teste de Ljung–Box

- **KNN** – Lags + estatísticas móveis; parâmetros ajustados por validação

- **VGG-1D** – CNN 1D com janelas deslizantes; early stopping via validação

- **Híbridos** – Residual Stacking e Ensemble ponderado (pesos via validação)

## Comparação (MSE / MAPE)

| Modelo                   |   MSE_train |   MAPE_train |     MSE_val |   MAPE_val |   MSE_test |   MAPE_test |
|:-------------------------|------------:|-------------:|------------:|-----------:|-----------:|------------:|
| ARIMA                    |    0.319886 |      26.6423 |   0.0864718 |    10.007  |   0.161364 |     15.7006 |
| KNN                      |    0        |       0      |   0.0989582 |    11.6223 |   0.191735 |     17.793  |
| VGG1D(w=12, f=32, d=0.0) |    0.189416 |      18.8206 |   0.0718918 |    11.1916 |   0.14143  |     20.1538 |
| HÍBRIDO-RESIDUAL         |  nan        |     nan      | nan         |   nan      |   0.188189 |     23.5678 |
| HÍBRIDO-ENSEMBLE         |  nan        |     nan      | nan         |   nan      |   0.137798 |     18.6984 |