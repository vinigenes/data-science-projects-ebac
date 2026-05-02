# Projeto de Classificação de Qualidade de Vinhos com Random Forest

## Descrição
Este projeto tem como objetivo prever a qualidade de vinhos tintos com base em suas características físico-químicas, utilizando o algoritmo de Random Forest para classificação multiclasse.

A proposta é analisar como diferentes variáveis influenciam a qualidade do vinho e avaliar o desempenho do modelo em um problema real.

---

## Base de Dados
A base utilizada foi a Wine Quality (Red Wine), contendo variáveis químicas dos vinhos.

### Variáveis (Features):
- fixed acidity
- volatile acidity
- citric acid
- residual sugar
- chlorides
- free sulfur dioxide
- total sulfur dioxide
- density
- pH
- sulphates
- alcohol

### Variável Target:
- quality (pontuação de 0 a 10)

---

## Etapas do Projeto

### 1. Pré-processamento
- Verificação de tipos de dados
- Análise de valores faltantes (não foram identificados)
- Dados considerados consistentes

---

### 2. Análise Exploratória
- Estatísticas descritivas com describe
- Avaliação do balanceamento da variável target
- Construção da matriz de correlação

Principais observações:
- alcohol apresentou correlação positiva com a qualidade
- volatile acidity apresentou correlação negativa
- sulphates e citric acid mostraram influência moderada
- density apresentou correlação negativa

Variáveis selecionadas para modelagem:
- alcohol
- volatile acidity
- sulphates
- citric acid
- total sulfur dioxide
- density

---

### 3. Preparação dos Dados
- Separação em X (features) e y (target)
- Divisão em treino e teste (80% treino / 20% teste)

---

### 4. Modelagem
- Algoritmo utilizado: Random Forest Classifier
- Parâmetros iniciais:
  - n_estimators = 100
  - random_state = 42

---

### 5. Avaliação do Modelo

Resultados iniciais:
- Accuracy aproximada: 64%

Análise:
- Melhor desempenho nas classes 5 e 6
- Desempenho moderado na classe 7
- Classes 3, 4 e 8 não foram bem previstas
- Evidência de desbalanceamento impactando o modelo

---

### 6. Otimização com Random Search

Hiperparâmetros testados:
- n_estimators
- max_depth
- min_samples_split
- min_samples_leaf
- bootstrap

Resultados após otimização:
- Accuracy aproximada: 65.9%

Conclusão da otimização:
- Pequena melhoria no desempenho geral
- Modelo mais estável
- Desbalanceamento ainda impacta os resultados

---

## Conclusão
O modelo Random Forest apresentou desempenho moderado, sendo mais eficiente nas classes com maior número de observações.

O ajuste de hiperparâmetros contribuiu para melhoria, porém não foi suficiente para resolver o problema de desbalanceamento.

---

## Possíveis Melhorias
- Aplicação de técnicas de balanceamento (SMOTE, oversampling, undersampling)
- Uso de class_weight no modelo
- Teste de outros algoritmos (XGBoost, LightGBM)
- Engenharia de atributos
- Redução de dimensionalidade

---

## Tecnologias Utilizadas
- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

