# Relatório de Análise de Série Temporal

**Arquivo:** dengue_pernambuco.xlsx  
**Planilha:** PE  
**Descrição:** Dados semanais de casos de dengue em Pernambuco  
**Data da Análise:** 11/10/2025 19:49:18

---

## 🔍 Características da Série Temporal

### Tipo de Variável: Univariada
Série univariada porque utiliza apenas uma variável numérica (valor) para análise temporal.

### Tipo de Continuidade: Contínua
Série contínua pois o tempo é regular com intervalo mais comum de 7 days 00:00:00.

### Sazonalidade: Sazonal
Série apresenta sazonalidade com coeficiente de variação de 2.08, indicando padrões que se repetem ao longo do tempo.

---

## 📊 Informações Gerais dos Dados

- **Total de registros:** 887
- **Coluna temporal:** semana
- **Coluna de valores:** valor
- **Período de dados:** 2000-01-08 00:00:00 até 2016-12-31 00:00:00
- **Duração total:** 6202 days 00:00:00

---

## 📈 Estatísticas Descritivas

### Medidas de Tendência Central
- **Média:** 551.2593
- **Mediana:** 164.0000

### Medidas de Dispersão
- **Desvio Padrão:** 1144.4633
- **Variância:** 1309796.2487
- **Coeficiente de Variação:** 2.0761

### Medidas de Posição
- **Valor Mínimo:** 1.0000
- **1º Quartil (Q1):** 74.0000
- **2º Quartil (Q2/Mediana):** 164.0000
- **3º Quartil (Q3):** 493.0000
- **Valor Máximo:** 11703.0000
- **Amplitude:** 11702.0000
- **Amplitude Interquartil (IQR):** 419.0000

### Medidas de Forma
- **Assimetria (Skewness):** 4.9435
  - *Distribuição assimétrica à direita (cauda longa à direita)*

- **Curtose (Kurtosis):** 31.8637
  - *Distribuição leptocúrtica (mais pontiaguda que a normal)*

---

## 📋 Qualidade dos Dados

- **Valores ausentes:** 0 (0.00%)
- **Outliers detectados:** 103 (11.61%)

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

1. **Variabilidade:** O coeficiente de variação de 2.08 indica alta variabilidade nos dados.

2. **Distribuição:** A série apresenta assimetria significativa.

3. **Qualidade:** Excelente qualidade dos dados com 0.0% de valores ausentes.

4. **Outliers:** Presença significativa de outliers (11.6% dos dados).

---

## 📁 Arquivos Gerados

- `relatorio_analise.md` - Este relatório completo
- `graficos/analise_completa.png` - Painel com todas as visualizações

---

*Relatório gerado automaticamente pelo sistema de análise de séries temporais.*
