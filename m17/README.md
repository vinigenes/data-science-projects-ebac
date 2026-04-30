# Projeto Credit Score - Preparação e Análise de Dados

## Objetivo

Este projeto tem como objetivo preparar e analisar uma base de dados para construção de um modelo de Credit Score, identificando padrões, relações entre variáveis e realizando o tratamento necessário para modelagem preditiva.

O Credit Score representa a probabilidade de um cliente se tornar inadimplente, sendo uma métrica essencial para tomada de decisão em instituições financeiras.

---

## Base de Dados

A base contém informações demográficas, financeiras e comportamentais dos clientes:

- Age: Idade  
- Income: Renda mensal  
- Gender: Gênero  
- Education: Escolaridade  
- Marital Status: Estado civil  
- Number of Children: Número de filhos  
- Home Ownership: Tipo de moradia  
- Credit Score: Classificação de crédito (variável alvo)  

---

## Tecnologias Utilizadas

- Python  
- pandas  
- numpy  
- matplotlib  
- seaborn  
- plotly  
- scikit-learn  
- imbalanced-learn  

---

## Etapas do Projeto

### 1. Pré-processamento dos Dados

- Conversão de tipos de dados (ex: Income para float)  
- Tratamento de valores faltantes com mediana  
- Verificação de inconsistências em variáveis categóricas  

Justificativa:
- A mediana foi utilizada por ser robusta a valores extremos  
- Evita perda de dados ao manter registros completos  

---

### 2. Análise Univariada

Principais insights:

- Idade concentrada entre 30 e 45 anos  
- Renda apresenta alta variabilidade  
- Número de filhos concentrado em valores baixos  
- Não foram identificados outliers relevantes  

---

### 3. Análise de Variáveis Categóricas

- Distribuição equilibrada entre gêneros  
- Predominância de alta escolaridade  
- Maioria dos clientes possui alto Credit Score  
- Indício de desbalanceamento na variável alvo  

---

### 4. Análise Bivariada

Principais relações identificadas:

- Idade maior associada a estado civil casado  
- Maior escolaridade associada a melhor Credit Score  
- Renda maior associada a maior score  
- Clientes com imóvel próprio tendem a ter melhor score  

---

### 5. Análises Adicionais

- Escolaridade influencia a renda  
- Pessoas casadas tendem a ter renda maior  
- Número de filhos não apresenta forte relação com o score  

---

### 6. Análise de Correlação

- Correlação moderada entre idade e renda  
- Relações coerentes com comportamento real do mercado  

---

### 7. Tratamento de Variáveis Categóricas

- Aplicação de One Hot Encoding  
- Conversão para variáveis numéricas  
- Remoção das colunas categóricas originais  

---

### 8. Correlação com Variáveis Transformadas

Principais relações:

- Renda altamente correlacionada com Credit Score alto  
- Moradia alugada associada a menor score  
- Pessoas solteiras tendem a morar de aluguel  

---

### 9. Divisão Treino e Teste

- Separação em 80% treino e 20% teste  
- Garantia de avaliação consistente do modelo  

---

### 10. Balanceamento dos Dados

- Identificação de desbalanceamento na variável alvo  
- Aplicação de RandomOverSampler  
- Balanceamento realizado apenas na base de treino  

Justificativa:
- Evita viés no modelo  
- Mantém base de teste representando o cenário real  

---

## Principais Insights

- Renda é um dos fatores mais relevantes para o Credit Score  
- Idade e estabilidade financeira influenciam o risco de crédito  
- Tipo de moradia está fortemente associado ao score  
- Variável alvo apresenta desbalanceamento significativo  

---

## Conclusão

O projeto estruturou todas as etapas necessárias para preparação dos dados, incluindo limpeza, análise e transformação, garantindo qualidade e consistência para a construção de modelos preditivos de Credit Score.

---
