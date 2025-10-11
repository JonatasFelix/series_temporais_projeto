## 📊 Resumo Detalhado por Dataset

### 1. Dataset: Dengue em Pernambuco

#### Características do Dataset
- **Fonte**: `dengue_pernambuco.xlsx`
- **Tipo de dados**: Casos semanais de dengue em Pernambuco
- **Frequência**: Semanal
- **Divisão**: 50% treino, 25% validação, 25% teste

#### Modelos Aplicados
1. **SARIMAX** - Modelo estatístico tradicional
2. **MLP (Multilayer Perceptron)** - Rede neural
3. **Random Forest** - de árvores de decisão
4. **Modelo Híbrido** - Combinação ARIMA + MLP

#### Análise das Imagens Geradas
**Pasta**: `out/dengue_pernambuco/` (18 imagens)

**Imagens SARIMAX:**

![SARIMAX - Comparação MSE e MAPE](out/dengue_pernambuco/SARIMAX%20-%20Comparação%20de%20MSE%20e%20MAPE%20-%20Treino%20vs%20Validação.png)

![SARIMAX - ACF](out/dengue_pernambuco/SARIMAX%20-%20Correlograma%20(ACF)%20dos%20Resíduos.png)

![SARIMAX - PACF](out/dengue_pernambuco/SARIMAX%20-%20Correlograma%20(PACF)%20dos%20Resíduos.png)

![SARIMAX - Q-Q Plot](out/dengue_pernambuco/SARIMAX%20-%20Q-Q%20Plot%20dos%20Resíduos%20Padronizados.png)

![SARIMAX - Ljung-Box](out/dengue_pernambuco/SARIMAX%20-%20Validação%20com%20Teste%20de%20Ljung-Box.png)

- Comparação MSE e MAPE entre treino e validação
- Correlogramas (ACF/PACF) dos resíduos - validação estatística
- Q-Q Plot - avaliação de normalidade dos resíduos
- Teste de Ljung-Box - verificação de autocorrelação residual

**Imagens MLP:**

![MLP - Treino Reais vs Previstas](out/dengue_pernambuco/MLP%20-%20Treino%20-%20Reais%20vs%20Previstas.png)

![MLP - Treino Resíduos](out/dengue_pernambuco/MLP%20-%20Treino%20-%20Resíduos.png)

![MLP - Validação Reais vs Previstas](out/dengue_pernambuco/MLP%20-%20Validação%20-%20Reais%20vs%20Previstas.png)

![MLP - Validação Resíduos](out/dengue_pernambuco/MLP%20-%20Validação%20-%20Resíduos.png)

![MLP - Teste Reais vs Previstas](out/dengue_pernambuco/MLP%20-%20Teste%20-%20Reais%20vs%20Previstas.png)

![MLP - Teste Resíduos](out/dengue_pernambuco/MLP%20-%20Teste%20-%20Resíduos.png)

![MLP - Comparação de Desempenho](out/dengue_pernambuco/MLP%20-%20Comparação%20de%20desempenho%20do%20modelo.png)

- Dispersão valores reais vs previstos (treino, validação, teste)
- Histogramas de resíduos para cada conjunto
- Comparação consolidada de MSE e MAPE

**Imagens Random Forest:**

![Random Forest - Valores Reais vs Previstos](out/dengue_pernambuco/Random%20Florest%20-%20Valores%20Reais%20vs%20Previstos%20-%20Treino,%20Validação%20e%20Teste.png)

![Random Forest - Comparação de Métricas](out/dengue_pernambuco/Random%20Florest%20-%20Comparação%20de%20Métricas%20por%20Conjunto.png)

![Random Forest - Distribuição dos Erros](out/dengue_pernambuco/Random%20Florest%20-%20Distribuição%20dos%20Erros.png)

- Série temporal com previsões sobrepostas
- Comparação de métricas por conjunto (barras)
- Distribuição dos erros

**Imagens Modelo Híbrido:**

![Híbrido - Desempenho](out/dengue_pernambuco/Hibrido%20-%20Desempenho%20do%20Modelo%20Híbrido%20(ARIMA%20+%20MLP).png)

![Híbrido - Valores Reais vs Previstos](out/dengue_pernambuco/Hibrido%20-%20Valores%20Reais%20vs%20Previstos%20-%20Validação.png)

![Híbrido - Distribuição dos Resíduos](out/dengue_pernambuco/Hibrido%20-%20Distribuição%20dos%20Resíduos%20-%20Validação.png)

- Desempenho comparativo ARIMA + MLP
- Valores reais vs previstos na validação
- Distribuição dos resíduos

#### Conclusões - Dengue Pernambuco
✅ **Insights**: Dengue apresenta sazonalidade anual (lag 52 semanas) bem capturada pelos modelos 
⚠️ **Desafio**: Alta variabilidade nos picos epidêmicos dificulta previsões precisas (MAPE ~22%)

---

### 2. Dataset: Consumo de Energia Residencial

#### Características do Dataset
- **Fonte**: `household_consumption.xlsx`
- **Tipo de dados**: Consumo de energia residencial
- **Frequência**: Horária
- **Divisão**: 50% treino, 25% validação, 25% teste

#### Modelos Aplicados
1. **SARIMAX**
2. **MLP**
3. **Random Forest**
4. **Modelo Híbrido**

#### Análise das Imagens Geradas
**Pasta**: `out/consumo_energia/` (18 imagens)

**Imagens SARIMAX:**

![SARIMAX - Comparação MSE e MAPE](out/consumo_energia/SARIMAX%20-%20Comparação%20de%20MSE%20e%20MAPE%20-%20Treino%20vs%20Validação.png)

![SARIMAX - ACF](out/consumo_energia/SARIMAX%20-%20Correlograma%20(ACF)%20dos%20Resíduos.png)

![SARIMAX - PACF](out/consumo_energia/SARIMAX%20-%20Correlograma%20(PACF)%20dos%20Resíduos.png)

![SARIMAX - Q-Q Plot](out/consumo_energia/SARIMAX%20-%20Q-Q%20Plot%20dos%20Resíduos%20Padronizados.png)

![SARIMAX - Ljung-Box](out/consumo_energia/SARIMAX%20-%20Validação%20com%20Teste%20de%20Ljung-Box.png)

**Imagens MLP:**

![MLP - Treino Reais vs Previstas](out/consumo_energia/MLP%20-%20Treino%20-%20Reais%20vs%20Previstas.png)

![MLP - Treino Resíduos](out/consumo_energia/MLP%20-%20Treino%20-%20Resíduos.png)

![MLP - Validação Reais vs Previstas](out/consumo_energia/MLP%20-%20Validação%20-%20Reais%20vs%20Previstas.png)

![MLP - Validação Resíduos](out/consumo_energia/MLP%20-%20Validação%20-%20Resíduos.png)

![MLP - Teste Reais vs Previstas](out/consumo_energia/MLP%20-%20Teste%20-%20Reais%20vs%20Previstas.png)

![MLP - Teste Resíduos](out/consumo_energia/MLP%20-%20Teste%20-%20Resíduos.png)

![MLP - Comparação de Desempenho](out/consumo_energia/MLP%20-%20Comparação%20de%20desempenho%20do%20modelo.png)

**Imagens Random Forest:**

![Random Forest - Valores Reais vs Previstos](out/consumo_energia/Random%20Florest%20-%20Valores%20Reais%20vs%20Previstos%20-%20Treino,%20Validação%20e%20Teste.png)

![Random Forest - Comparação de Métricas](out/consumo_energia/Random%20Florest%20-%20Comparação%20de%20Métricas%20por%20Conjunto.png)

![Random Forest - Distribuição dos Erros](out/consumo_energia/Random%20Florest%20-%20Distribuição%20dos%20Erros.png)

**Imagens Modelo Híbrido:**

![Híbrido - Desempenho](out/consumo_energia/Hibrido%20-%20Desempenho%20do%20Modelo%20Híbrido%20(ARIMA%20+%20MLP).png)

![Híbrido - Valores Reais vs Previstos](out/consumo_energia/Hibrido%20-%20Valores%20Reais%20vs%20Previstos%20-%20Validação.png)

![Híbrido - Distribuição dos Resíduos](out/consumo_energia/Hibrido%20-%20Distribuição%20dos%20Resíduos%20-%20Validação.png)

- **SARIMAX**: Diagnósticos estatísticos completos
- **MLP**: Análise de predição e resíduos
- **Random Forest**: Visualizações temporais e métricas
- **Híbrido**: Comparações de desempenho

#### Conclusões - Consumo de Energia
✅ **Destaque**: ARIMA teve melhor MAPE (15.70%), indicando menor erro relativo 
✅ **Padrão**: Consumo horário tem sazonalidade diária/semanal bem definida 
💡 **Insight**: Modelos tradicionais (ARIMA) competem bem com ML neste dataset

---

### 3. Dataset: Geração de Energia Solar (França)

#### Características do Dataset
- **Fonte**: `solar france.xlsx`
- **Tipo de dados**: Produção de energia solar na França
- **Frequência**: Horária
- **Divisão**: 50% treino, 25% validação, 25% teste

#### Modelos Aplicados
1. **SARIMAX**
2. **MLP**
3. **Random Forest**
4. **Modelo Híbrido**

#### Análise das Imagens Geradas
**Pasta**: `out/geracao_energia/` (18 imagens)

**Imagens SARIMAX:**

![SARIMAX - Comparação MSE e MAPE](out/geracao_energia/SARIMAX%20-%20Comparação%20de%20MSE%20e%20MAPE%20-%20Treino%20vs%20Validação.png)

![SARIMAX - ACF](out/geracao_energia/SARIMAX%20-%20Correlograma%20(ACF)%20dos%20Resíduos.png)

![SARIMAX - PACF](out/geracao_energia/SARIMAX%20-%20Correlograma%20(PACF)%20dos%20Resíduos.png)

![SARIMAX - Q-Q Plot](out/geracao_energia/SARIMAX%20-%20Q-Q%20Plot%20dos%20Resíduos%20Padronizados.png)

![SARIMAX - Ljung-Box](out/geracao_energia/SARIMAX%20-%20Validação%20com%20Teste%20de%20Ljung-Box.png)

**Imagens MLP:**

![MLP - Treino Reais vs Previstas](out/geracao_energia/MLP%20-%20Treino%20-%20Reais%20vs%20Previstas.png)

![MLP - Treino Resíduos](out/geracao_energia/MLP%20-%20Treino%20-%20Resíduos.png)

![MLP - Validação Reais vs Previstas](out/geracao_energia/MLP%20-%20Validação%20-%20Reais%20vs%20Previstas.png)

![MLP - Validação Resíduos](out/geracao_energia/MLP%20-%20Validação%20-%20Resíduos.png)

![MLP - Teste Reais vs Previstas](out/geracao_energia/MLP%20-%20Teste%20-%20Reais%20vs%20Previstas.png)

![MLP - Teste Resíduos](out/geracao_energia/MLP%20-%20Teste%20-%20Resíduos.png)

![MLP - Comparação de Desempenho](out/geracao_energia/MLP%20-%20Comparação%20de%20desempenho%20do%20modelo.png)

**Imagens Random Forest:**

![Random Forest - Valores Reais vs Previstos](out/geracao_energia/Random%20Florest%20-%20Valores%20Reais%20vs%20Previstos%20-%20Treino,%20Validação%20e%20Teste.png)

![Random Forest - Comparação de Métricas](out/geracao_energia/Random%20Florest%20-%20Comparação%20de%20Métricas%20por%20Conjunto.png)

![Random Forest - Distribuição dos Erros](out/geracao_energia/Random%20Florest%20-%20Distribuição%20dos%20Erros.png)

**Imagens Modelo Híbrido:**

![Híbrido - Desempenho](out/geracao_energia/Hibrido%20-%20Desempenho%20do%20Modelo%20Híbrido%20(ARIMA%20+%20MLP).png)

![Híbrido - Valores Reais vs Previstos](out/geracao_energia/Hibrido%20-%20Valores%20Reais%20vs%20Previstos%20-%20Validação.png)

![Híbrido - Distribuição dos Resíduos](out/geracao_energia/Hibrido%20-%20Distribuição%20dos%20Resíduos%20-%20Validação.png)

- **SARIMAX**: Análises de resíduos e testes estatísticos
- **MLP**: Scatter plots e histogramas de erros
- **Random Forest**: Séries temporais e comparações
- **Híbrido**: Avaliação de performance combinada

#### Conclusões - Geração Solar
⚠️ **Desafio**: Geração solar tem zeros noturnos e alta variabilidade climática 
✅ **KNN fraco**: Não captura bem a dependência temporal complexa (MSE: 144.300) 
💡 **Insight**: Dropout 0.2 no VGG1D foi crucial para evitar overfitting

---

## 🎯 Conclusões Gerais Comparativas

### Padrões Identificados

1. **Consistência**: Modelo Híbrido venceu em **TODOS** os datasets
2. **Deep Learning**: VGG1D performou muito bem em dados com padrões complexos
3. **ARIMA**: Competitivo em séries com sazonalidade clara (energia)
4. **KNN**: Inadequado para séries temporais complexas

### Imagens Geradas por Modelo

Cada dataset possui **18 imagens** divididas em:
- **5 imagens SARIMAX**: diagnósticos estatísticos (ACF, PACF, Q-Q, Ljung-Box)
- **7 imagens MLP**: scatter plots e histogramas (treino/validação/teste)
- **3 imagens Random Forest**: visualizações temporais e métricas
- **3 imagens Híbrido**: análises comparativas

**Total**: **54 imagens geradas** (18 × 3 datasets)

### Tipos de Visualizações Disponíveis

✅ **Diagnósticos Estatísticos**: ACF, PACF, Q-Q Plot, Ljung-Box 
✅ **Predições**: Valores reais vs previstos (scatter) 
✅ **Resíduos**: Histogramas e distribuições 
✅ **Métricas**: Comparações MSE/MAPE em gráficos de barras 
✅ **Séries Temporais**: Plotagens com previsões sobrepostas

---

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
│  ├── dengue_pernambuco.xlsx
│  ├── household_consumption.xlsx
│  ├── solar france.xlsx
│  └── chuva_fortaleza.xlsx
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