# Análise Comparativa de Modelos para Previsão de Séries Temporais

Este projeto compara diferentes técnicas de previsão de séries temporais: ARIMA/SARIMA, KNN, CNN 1D (VGG-1D) e modelos híbridos. O objetivo é avaliar qual abordagem apresenta melhor desempenho em diferentes tipos de dados.

## Datasets

Foram analisadas três séries temporais:

- **dengue_pernambuco.xlsx**: casos semanais de dengue em Pernambuco
- **household_consumption.xlsx**: consumo de energia residencial (dados horários)
- **solar france.xlsx**: produção de energia solar na França (dados horários)

## Metodologia

### Divisão dos Dados
Os dados foram divididos temporalmente em:
- Treino: 50%
- Validação: 25%
- Teste: 25%

### Modelos Utilizados

**ARIMA/SARIMA**
- Método tradicional de Box & Jenkins
- Seleção de parâmetros por AIC
- Validação com teste de Ljung-Box

**KNN (K-Nearest Neighbors)**
- Features: lags e estatísticas móveis
- Otimização de hiperparâmetros por validação

**VGG-1D (CNN 1D)**
- Rede neural convolucional 1D
- Janelas de 12 e 24 timesteps
- Early stopping

**Modelos Híbridos**
- Residual: ARIMA + modelo ML nos resíduos
- Ensemble: combinação ponderada de modelos

### Métricas
- MSE (Mean Squared Error)
- MAPE (Mean Absolute Percentage Error)

## Resultados

### Dengue em Pernambuco

| Modelo                   | MSE Test | MAPE Test (%) |
|:-------------------------|----------:|--------------:|
| HÍBRIDO-ENSEMBLE         | 120.606   | 22.15         |
| VGG1D(w=12, f=64, d=0.0) | 142.787   | 25.53         |
| ARIMA                    | 175.078   | 27.59         |
| HÍBRIDO-RESIDUAL         | 187.221   | 36.77         |
| KNN                      | 584.605   | 33.34         |

### Consumo de Energia

| Modelo                   | MSE Test  | MAPE Test (%) |
|:-------------------------|----------:|--------------:|
| HÍBRIDO-ENSEMBLE         | 0.138     | 18.70         |
| VGG1D(w=12, f=32, d=0.0) | 0.141     | 20.15         |
| ARIMA                    | 0.161     | 15.70         |
| HÍBRIDO-RESIDUAL         | 0.188     | 23.57         |
| KNN                      | 0.192     | 17.79         |

### Geração Solar

| Modelo                   | MSE Test  |
|:-------------------------|----------:|
| HÍBRIDO-ENSEMBLE         | 13.461    |
| ARIMA                    | 21.512    |
| VGG1D(w=24, f=64, d=0.2) | 23.071    |
| HÍBRIDO-RESIDUAL         | 28.467    |
| KNN                      | 144.300   |

Os resultados mostram que o modelo híbrido ensemble teve o melhor desempenho nos três datasets. Os gráficos e tabelas completas estão disponíveis nas pastas `out_dengue/`, `out_consumo_energia/` e `out_geracao_energia/`.

## Requisitos

- Python 3.8+
- pandas, numpy, matplotlib
- scikit-learn
- statsmodels
- tensorflow (para VGG-1D)
- openpyxl

Instalar com:
```bash
pip install pandas numpy matplotlib scikit-learn statsmodels tensorflow openpyxl
```

## Estrutura do Projeto

```
series_temporais_projeto/
├── main.ipynb
├── README.md
├── data/
│   ├── dengue_pernambuco.xlsx
│   ├── household_consumption.xlsx
│   ├── solar france.xlsx
│   └── chuva_fortaleza.xlsx
├── out_dengue/
├── out_consumo_energia/
└── out_geracao_energia/
```

## Como Executar

1. Coloque os arquivos de dados na pasta `data/`
2. Abra o notebook `main.ipynb`
3. Execute as células em ordem
4. O notebook vai perguntar qual dataset usar
5. Os resultados são salvos automaticamente nas pastas `out_*/`

Os arquivos gerados incluem:
- Gráficos de previsão (`.png`)
- Tabela de métricas (`metrics_summary.csv`)
- Resumo em markdown (`presentation.md`)