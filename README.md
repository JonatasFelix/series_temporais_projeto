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


## Análise Detalhada: Household Consumption

### Notebooks Disponíveis

Foi desenvolvida uma análise completa para o dataset `household_consumption.xlsx` com 4 modelos diferentes:

**Notebooks em `models/household_consumption/`:**
- **`SARIMAX.ipynb`**: Modelo estatístico clássico
  - ACF, PACF, Box-Cox, decomposição sazonal
  - Grid search para hiperparâmetros (p,d,q)×(P,D,Q,s)
  - Validação cruzada temporal
  - Diagnósticos de resíduos (Ljung-Box, normalidade)
  - 8 gráficos analíticos

- **`MLP.ipynb`**: Rede neural feedforward
  - Engenharia de features (24 lags, rolling stats, encoding cíclico)
  - Normalização e GridSearchCV com TimeSeriesSplit
  - Arquiteturas testadas (50 a 100-50-25 neurônios)
  - Análise de overfitting e curvas de aprendizado
  - Feature importance por permutação

- **`Random Forest.ipynb`**: Ensemble de árvores
  - Features: 36 lags + rolling stats (janelas até 96)
  - Grid search: n_estimators, max_depth, min_samples
  - Feature importance (top 20)
  - Treinamento paralelo otimizado

- **`Hibrido (ARIMA + MLP).ipynb`**: Combinação de modelos
  - ARIMA captura componente linear → gera resíduos
  - MLP modela os resíduos (padrões não-lineares)
  - Previsão final = ARIMA + MLP(resíduos)
  - Sinergia entre estatística clássica e machine learning

- **`Comparacao.ipynb`**: Análise comparativa
  - Agrega métricas dos 4 modelos
  - Tabela comparativa (RMSE, MAE, MAPE, R²)
  - Gráfico de barras comparativo
  - Insights sobre força de sazonalidade/tendência

### Resultados Salvos

**Estrutura de saída em `out/household_consumption/`:**
```
out/household_consumption/
├── SARIMAX/
│   ├── sarimax_results.json           # Métricas e parâmetros
│   ├── sarimax_predictions.csv        # Previsões com intervalos
│   └── *.png (8 gráficos)             # Análise completa
├── MLP/
│   ├── mlp_results.json
│   ├── mlp_predictions.csv
│   └── *.png (5 gráficos)
├── RandomForest/
│   ├── rf_results.json
│   ├── rf_predictions.csv
│   └── *.png (2 gráficos)
├── Hibrido/
│   ├── hybrid_results.json
│   ├── hybrid_predictions.csv
│   └── *.png (1 gráfico)
├── comparacao_metricas.csv            # Tabela comparativa final
├── comparacao_metricas.png            # Gráfico de barras
└── comparacao_insights.txt            # Análise textual
```

### 📚 Arquivos de Apresentação

**Documentação completa disponível em arquivos Markdown:**

1. **`APRESENTACAO_HOUSEHOLD_CONSUMPTION.md`** (~1000 linhas)
   - Documentação técnica completa
   - Explicação detalhada de cada modelo
   - Interpretação de todos os gráficos
   - Metodologia passo a passo
   - **Use para**: Documentação, referência técnica, estudo profundo

2. **`APRESENTACAO_RESUMIDA.md`** (~500 linhas)
   - Material otimizado para slides
   - Bullets objetivos e tabelas
   - Seções delimitadas (prontas para PowerPoint)
   - **Use para**: Apresentações de 20-30 minutos, seminários

3. **`SUMARIO_EXECUTIVO.md`** (~300 linhas)
   - Overview executivo rápido
   - Top 5 insights e recomendações
   - Matriz de escolha de modelos
   - **Use para**: Briefing executivo, pitch de 5-10 minutos

4. **`INDICE_APRESENTACOES.md`**
   - Guia visual de navegação
   - Comparação de profundidade dos arquivos
   - Fluxogramas de decisão
   - **Use para**: Escolher qual arquivo ler

**Escolha rápida:**
- 5 minutos? → `SUMARIO_EXECUTIVO.md`
- Vai apresentar? → `APRESENTACAO_RESUMIDA.md`
- Quer tudo? → `APRESENTACAO_HOUSEHOLD_CONSUMPTION.md`
- Não sabe por onde começar? → `INDICE_APRESENTACOES.md`

### Como Executar

1. **Instalar dependências:**
   ```bash
   pip install -r requirements.txt
   ```

2. **Executar notebooks individualmente:**
   - Abra cada notebook em `models/household_consumption/`
   - Execute células em ordem
   - Resultados salvos automaticamente em `out/household_consumption/`

3. **Gerar comparação final:**
   - Execute `models/household_consumption/Comparacao.ipynb` por último
   - Gera tabela e gráfico comparativo

4. **Consultar resultados:**
   - Métricas: Arquivos JSON em cada pasta de modelo
   - Previsões: Arquivos CSV
   - Visualizações: Arquivos PNG
   - Resumo: `comparacao_metricas.csv`
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