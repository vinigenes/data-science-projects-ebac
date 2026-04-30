# Regressão Linear - Previsão de Valor de Aluguel

## Objetivo

Este projeto tem como objetivo desenvolver modelos de regressão linear simples e múltipla para prever o valor de aluguel de imóveis com base em características estruturais, como metragem, número de quartos e outras variáveis relevantes.

---

## Base de Dados

A base contém informações sobre imóveis disponíveis para aluguel:

- Valor_Aluguel: Valor total do aluguel  
- Valor_Condominio: Valor do condomínio  
- Metragem: Tamanho do imóvel (m²)  
- N_Quartos: Número de quartos  
- N_Banheiros: Número de banheiros  
- N_Suites: Número de suítes  
- N_Vagas: Número de vagas  

---

## Tecnologias Utilizadas

- Python  
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  

---

## Etapas do Projeto

### 1. Pré-processamento dos Dados

- Verificação dos tipos de dados  
- Identificação e tratamento de valores faltantes  
- Garantia de consistência da base  

---

### 2. Análise Exploratória

- Uso de estatísticas descritivas (`describe`)  
- Identificação de possíveis outliers  
- Análise da distribuição das variáveis  

#### Tratamento de Outliers

- Aplicação do método IQR  
- Remoção de valores extremos para melhorar o ajuste do modelo  

Justificativa:
- Outliers podem distorcer o modelo de regressão  
- A remoção melhora a estabilidade das previsões  

---

### 3. Análise Bivariada

Principais insights:

- Existe relação positiva entre metragem e valor do aluguel  
- Imóveis com mais quartos tendem a ter maior valor  
- O valor do condomínio também influencia o preço final  

---

### 4. Correlação

- Análise da matriz de correlação  
- Identificação das variáveis mais relevantes para o modelo  

---

### 5. Separação Treino e Teste

- Divisão da base em 80% treino e 20% teste  
- Garantia de avaliação consistente do modelo  

---

## Modelo 1: Regressão Linear Simples

### Variável utilizada:
- Metragem  

### Equação da Reta

Valor_Aluguel = 34.47 * Metragem - 97.00

### Avaliação

- R² Treino: 0.52  
- R² Teste: 0.57  

### Insights

- Relação positiva entre metragem e valor do aluguel  
- Ajuste moderado  
- Indicação de que outras variáveis influenciam o preço  

---

## Modelo 2: Regressão Linear Múltipla

### Variáveis utilizadas:

- Metragem  
- Valor_Condominio  
- Número de Quartos  
- Número de Banheiros  
- Número de Suítes  
- Número de Vagas  

### Avaliação

- R² Treino: Aproximadamente 0.60  
- R² Teste: 0.63  

### Insights

- Melhor desempenho em relação ao modelo simples  
- Capacidade maior de explicar a variação dos dados  
- Consideração de múltiplos fatores melhora a previsão  

---

## Comparação dos Modelos

| Modelo                  | R² Treino | R² Teste |
|------------------------|----------|----------|
| Regressão Simples      | 0.52     | 0.57     |
| Regressão Múltipla     | 0.60     | 0.63     |

Conclusão:

O modelo de regressão múltipla apresentou melhor desempenho por considerar múltiplas variáveis que influenciam o valor do imóvel, tornando a previsão mais precisa.

---

## Conclusão

- A metragem é um fator importante, mas não suficiente isoladamente  
- A inclusão de múltiplas variáveis melhora significativamente o modelo  
- O modelo múltiplo apresenta melhor capacidade preditiva e generalização  

---

