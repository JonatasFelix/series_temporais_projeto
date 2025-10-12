# Relatório de Análise de Série Temporal

**Arquivo:** solar_france.xlsx  
**Planilha:** intermittent-renewables-product  
**Descrição:** Produção de energia solar na França por hora  
**Data da Análise:** 12/10/2025 15:50:56

---

## 🔍 Características da Série Temporal

### Tipo de Variável: Univariada
Série univariada porque utiliza apenas uma variável numérica (Production) para análise temporal.

### Tipo de Continuidade: Discreta
Série discreta pois os intervalos de tempo são irregulares.

### Sazonalidade: Sazonal
Série apresenta sazonalidade com coeficiente de variação de 1.45, indicando padrões que se repetem ao longo do tempo.

---

## 📊 Informações Gerais dos Dados

- **Total de registros:** 29,902
- **Coluna temporal:** Date and Hour
- **Coluna de valores:** Production
- **Período de dados:** 2020-01-01 00:00:00+01:00 até 2023-06-30 23:00:00+02:00
- **Duração total:** 1276 days 22:00:00

---

## 📈 Estatísticas Descritivas

### Medidas de Tendência Central
- **Média:** 1068.8624
- **Mediana:** 42.0000

### Medidas de Dispersão
- **Desvio Padrão:** 1547.2207
- **Variância:** 2393891.9766
- **Coeficiente de Variação:** 1.4475

### Medidas de Posição
- **Valor Mínimo:** 0.0000
- **1º Quartil (Q1):** 1.0000
- **2º Quartil (Q2/Mediana):** 42.0000
- **3º Quartil (Q3):** 1909.0000
- **Valor Máximo:** 7489.0000
- **Amplitude:** 7489.0000
- **Amplitude Interquartil (IQR):** 1908.0000

### Medidas de Forma
- **Assimetria (Skewness):** 1.4176
  - *Distribuição assimétrica à direita (cauda longa à direita)*

- **Curtose (Kurtosis):** 1.0786
  - *Distribuição leptocúrtica (mais pontiaguda que a normal)*

---

## 📋 Qualidade dos Dados

- **Valores ausentes:** 1 (0.00%)
- **Outliers detectados:** 1055 (3.53%)

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

Esta série temporal é caracterizada como **Univariada**, **Discreta** e **Sazonal**.

### Principais Insights:

1. **Variabilidade:** O coeficiente de variação de 1.45 indica alta variabilidade nos dados.

2. **Distribuição:** A série apresenta assimetria significativa.

3. **Qualidade:** Excelente qualidade dos dados com 0.0% de valores ausentes.

4. **Outliers:** Poucos outliers detectados (3.5% dos dados).

---

## 📁 Arquivos Gerados

- `relatorio_analise.md` - Este relatório completo
- `graficos/analise_completa.png` - Painel com todas as visualizações

---

*Relatório gerado automaticamente pelo sistema de análise de séries temporais.*
