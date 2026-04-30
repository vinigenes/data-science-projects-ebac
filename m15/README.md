# Análise Exploratória de Dados - Churn em Telecomunicações

## Objetivo

Este projeto tem como objetivo realizar a análise exploratória de dados (EDA) em uma base de churn de telecomunicações, identificando padrões, outliers e variáveis relevantes para a previsão de cancelamento de clientes.

---

## Base de Dados

A base utilizada contém informações sobre clientes de serviços de telecomunicação, incluindo dados demográficos, contratuais e financeiros.

---

## Tecnologias Utilizadas

- Python  
- pandas  
- numpy  
- matplotlib  
- seaborn  
- plotly  

---

## Etapas da Análise

### 1. Análise Univariada

Foi utilizada a função `describe()` para obter estatísticas descritivas das variáveis numéricas.

Principais insights:

- Predominância de clientes não idosos  
- Presença de clientes novos (1 mês) e antigos (até 72 meses)  
- Diferença entre média e mediana em variáveis financeiras, indicando assimetria  
- Indícios de valores extremos em `monthly_payment` e `total_paid`  

---

### 2. Identificação de Outliers

As variáveis com possíveis outliers foram:

- monthly_payment  
- total_paid  

Foi utilizada a técnica do IQR para detecção.

Decisão:

Os outliers foram mantidos, pois representam clientes reais e relevantes para o problema de churn, especialmente aqueles com maior valor financeiro.

---

### 3. Análise Univariada com Visualizações

Foram utilizados gráficos para entender a distribuição das variáveis:

- Boxplot de `total_paid`: alta dispersão e assimetria positiva  
- Boxplot de `monthly_payment`: distribuição moderada sem outliers extremos  
- Histograma de `tenure_months`: concentração em clientes novos e antigos  
- Countplot de `senior_citizen`: variável desbalanceada  

---

### 4. Balanceamento de Variáveis Booleanas

A variável `senior_citizen` apresenta desbalanceamento, com predominância de clientes não idosos.

---

### 5. Análise Bivariada

#### Tempo de permanência vs churn

Clientes com maior tempo de permanência apresentam menor taxa de churn.

---

#### Pagamento mensal vs churn

Clientes que cancelam tendem a ter pagamentos mensais ligeiramente maiores.

---

#### Idade (idoso) vs churn

Clientes idosos apresentam maior proporção de churn, apesar de serem minoria.

---

#### Total pago vs churn

Clientes que permanecem possuem maior valor total pago, indicando maior tempo de relacionamento.

---

#### Correlação entre variáveis numéricas

- Forte correlação entre `tenure_months` e `total_paid`  
- Correlação moderada entre `monthly_payment` e `total_paid`  
- Baixa correlação entre `tenure_months` e `monthly_payment`  

---

## Principais Insights

- Tempo de permanência é um dos fatores mais importantes para churn  
- Clientes novos possuem maior probabilidade de cancelamento  
- Clientes com maior pagamento mensal tendem a cancelar mais  
- Clientes idosos apresentam comportamento de churn diferenciado  
- Valor total pago está diretamente ligado à retenção  

---

## Conclusão

A análise exploratória permitiu identificar padrões relevantes para o problema de churn, destacando variáveis importantes que poderão ser utilizadas em modelos preditivos.

---
