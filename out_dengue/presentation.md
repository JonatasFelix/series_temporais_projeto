# Projeto – Análise de Séries Temporais e Regressão

## Série utilizada

- Arquivo: `dengue_pernambuco.xlsx`

- Coluna temporal detectada: `semana`

- Coluna alvo detectada: `valor`

## Metodologia

- Split temporal: **50% / 25% / 25%** (ordem preservada)

- **ARIMA/SARIMA (Box–Jenkins)** – Seleção via AIC e teste de Ljung–Box

- **KNN** – Lags + estatísticas móveis; parâmetros ajustados por validação

- **VGG-1D** – CNN 1D com janelas deslizantes; early stopping via validação

- **Híbridos** – Residual Stacking e Ensemble ponderado (pesos via validação)

## Comparação (MSE / MAPE)

| Modelo                   |   MSE_train |   MAPE_train |   MSE_val |   MAPE_val |   MSE_test |   MAPE_test |
|:-------------------------|------------:|-------------:|----------:|-----------:|-----------:|------------:|
| ARIMA                    |     47957.3 |      63.9104 |   11057.8 |    44.8365 |     175078 |     27.5904 |
| KNN                      |         0   |       0      |   45881.3 |    36.4702 |     584605 |     33.3393 |
| VGG1D(w=12, f=64, d=0.0) |     45192.7 |      31.2954 |   10469.3 |    28.8701 |     142787 |     25.5326 |
| HÍBRIDO-RESIDUAL         |       nan   |     nan      |     nan   |   nan      |     187221 |     36.7694 |
| HÍBRIDO-ENSEMBLE         |       nan   |     nan      |     nan   |   nan      |     120606 |     22.1469 |