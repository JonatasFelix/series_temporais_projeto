# Relatório de Análise de Série Temporal

**Arquivo:** household_consumption.xlsx  
**Planilha:** Sheet1  
**Descrição:** Consumo doméstico por minuto  
**Data da Análise:** 11/10/2025 19:50:39

---

## 🔍 Características da Série Temporal

### Tipo de Variável: Univariada
Série univariada porque utiliza apenas uma variável numérica (Consumption) para análise temporal.

### Tipo de Continuidade: Contínua
Série contínua pois o tempo é regular com intervalo mais comum de 0 days 00:01:00.

### Sazonalidade: Sazonal
Série apresenta sazonalidade com coeficiente de variação de 0.76, indicando padrões que se repetem ao longo do tempo.

---

## 📊 Informações Gerais dos Dados

- **Total de registros:** 5,000
- **Coluna temporal:** Date and Hour
- **Coluna de valores:** Consumption
- **Período de dados:** 2006-12-16 16:24:00 até 2006-12-20 03:43:00
- **Duração total:** 3 days 11:19:00

---

## 📈 Estatísticas Descritivas

### Medidas de Tendência Central
- **Média:** 1.7181
- **Mediana:** 1.6260

### Medidas de Dispersão
- **Desvio Padrão:** 1.3018
- **Variância:** 1.6947
- **Coeficiente de Variação:** 0.7577

### Medidas de Posição
- **Valor Mínimo:** 0.1940
- **1º Quartil (Q1):** 0.3800
- **2º Quartil (Q2/Mediana):** 1.6260
- **3º Quartil (Q3):** 2.5020
- **Valor Máximo:** 7.8400
- **Amplitude:** 7.6460
- **Amplitude Interquartil (IQR):** 2.1220

### Medidas de Forma
- **Assimetria (Skewness):** 0.7995
  - *Distribuição assimétrica à direita (cauda longa à direita)*

- **Curtose (Kurtosis):** 0.5626
  - *Distribuição leptocúrtica (mais pontiaguda que a normal)*

---

## 📋 Qualidade dos Dados

- **Valores ausentes:** 0 (0.00%)
- **Outliers detectados:** 44 (0.88%)

---

## 📊 Visualizações Geradas

As seguintes visualizações foram criadas e salvas na pasta `graficos/`:

1. **Série Temporal Principal** - Gráfico de linha mostrando a evolução temporal dos dados
2. **Histograma de Distribuição** - Distribuição de frequências dos valores
3. **Box Plot** - Visualização dos quartis e outliers
4. **Análise de Tendência** - Série original com média móvel
5. **Análise Sazonal** - Padrões por período (quando aplicável)

---

## 🎯 Resumo Executivo

Esta série temporal é caracterizada como **Univariada**, **Contínua** e **Sazonal**.

### Principais Insights:

1. **Variabilidade:** O coeficiente de variação de 0.76 indica alta variabilidade nos dados.

2. **Distribuição:** A série apresenta assimetria significativa.

3. **Qualidade:** Excelente qualidade dos dados com 0.0% de valores ausentes.

4. **Outliers:** Poucos outliers detectados (0.9% dos dados).

---

## 📁 Arquivos Gerados

- `relatorio_analise.md` - Este relatório completo
- `graficos/analise_completa.png` - Painel com todas as visualizações

---

*Relatório gerado automaticamente pelo sistema de análise de séries temporais.*
