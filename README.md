# Previsão de Mortes por Armas na Austrália

Este projeto tem como objetivo comparar diferentes abordagens de previsão de séries temporais aplicadas à quantidade de mortes por armas de fogo na Austrália. O workflow foi desenvolvido usando Python (Jupyter Notebook) e abrange desde a preparação dos dados até a análise comparativa dos modelos preditivos.

## Objetivos

- Realizar uma previsão **1 passo à frente** das mortes por armas na Austrália.
- Comparar técnicas tradicionais e modernas de séries temporais, além de modelos híbridos.
- Avaliar modelos quanto à estabilidade, variância e desempenho usando **10 execuções** com diferentes seeds.

## Dados

- **Fonte:** `morte_armas_australia.xlsx`
- **Descrição:** Série temporal com índices de datas e valores numéricos representando o número de mortes por armas de fogo na Austrália.

## Metodologia

### 1. Divisão dos Dados

A série é dividida de forma temporal em três conjuntos:
- **Treino:** 50%
- **Validação:** 25%
- **Teste:** 25%

### 2. Abordagens de Modelagem

Foram avaliadas quatro abordagens principais, todas testadas em 10 execuções para análise de variância:

- **ARIMA** (Box & Jenkins): Seleção de parâmetros usando validação.
- **Aprendizado de Máquina (AM) Clássico:**
  - **SVR** (Support Vector Regression)
  - **Random Forest**
- **Aprendizado Profundo (AP):**
  - **MLPRegressor** (Perceptron Multi-Camadas)
- **Modelo Híbrido:** ARIMA para tendência e MLP nos resíduos.

### 3. Features

Para os métodos de ML, foram usados **lags** como atributos (quantidade depende da frequência identificada na série) e variáveis de sazonalidade (mês, trimestre).

### 4. Avaliação

- Métricas: **MSE** (Erro Quadrático Médio) e **MAPE** (Erro Percentual Absoluto Médio).
- Avaliação é feita em **treino, validação e teste**.
- Resultados em tabelas e gráficos.

### 5. Repetição (10 rodadas)

Os modelos SVR, Random Forest, MLP e Híbrido foram rodados 10 vezes cada com seeds distintas para avaliar dispersão e robustez dos resultados.

## Requisitos

- Python 3.11+
- Jupyter Notebook
- Principais bibliotecas: pandas, numpy, matplotlib, scikit-learn, statsmodels, scipy.

## Como Executar

1. Instale os requisitos em um ambiente virtual (recomendado).
2. Coloque o arquivo `morte_armas_australia.xlsx` na pasta `data/`.
3. Execute o notebook em sequência de células para reproduzir os resultados.

## Resultados

Cada técnica foi avaliada por suas métricas de erro (MSE/MAPE). Ao fim, as melhores execuções de cada grupo são comparadas para encontrar o **modelo com melhor desempenho geral**.

## Apresentação

Sugestões para apresentação dos resultados:
- Mostre o gráfico da série original destacando frequência e sazonalidade.
- Explique resumidamente a metodologia Box & Jenkins utilizada no ARIMA.
- Mostre como os lags foram inseridos como features.
- Analise as tabelas geradas nas 10 execuções e discuta a estabilidade de cada abordagem.
- Ressalte o vencedor geral e traga possíveis motivos para seu melhor desempenho.

## Licença

Livre para uso acadêmico e teste. Cite a fonte e os autores em produções derivadas.