# Projeto Credit Score - Classificação com Naive Bayes

## Objetivo

Este projeto tem como objetivo aplicar o algoritmo de Naive Bayes para prever o score de crédito de clientes, classificando-os em diferentes categorias com base em características financeiras e demográficas.

---

## Contexto

O Credit Score representa a probabilidade de um cliente cumprir suas obrigações financeiras. Modelos preditivos são amplamente utilizados por instituições financeiras para apoiar decisões de concessão de crédito.

Neste projeto, utilizamos um modelo probabilístico (Naive Bayes) para realizar essa classificação.

---

## Base de Dados

A base utilizada já passou por etapas anteriores de:

- Tratamento de dados  
- Conversão de variáveis categóricas  
- Balanceamento de classes  
- Separação em treino e teste  

Arquivos utilizados:

- X_train_bal.csv  
- y_train_bal.csv  
- X_test.csv  
- y_test.csv  

---

## Tecnologias Utilizadas

- Python  
- pandas  
- numpy  
- seaborn  
- matplotlib  
- scikit-learn  

---

## Etapas do Projeto

### 1. Carregamento dos Dados

- Verificação das dimensões das bases  
- Conferência de consistência entre X e y  
- Análise do balanceamento das classes  

---

### 2. Treinamento do Modelo

- Algoritmo utilizado: Gaussian Naive Bayes  
- Treinamento realizado com base balanceada  

---

### 3. Avaliação no Treino

Métricas utilizadas:

- Acurácia  
- Recall (macro)  
- Matriz de confusão  

Resultados:

- Acurácia: 0.985  
- Recall: 0.985  

Insights:

- O modelo apresentou excelente desempenho  
- Baixa taxa de erro  
- Boa capacidade de identificar corretamente as classes  

---

### 4. Avaliação no Teste

Métricas utilizadas:

- Acurácia  
- Recall (macro)  
- Matriz de confusão  

Resultados:

- Acurácia: 1.0  
- Recall: 1.0  

Insights:

- O modelo classificou corretamente todos os registros  
- Desempenho consistente em relação ao treino  
- Forte capacidade de generalização  

---

## Interpretação dos Resultados

- O modelo apresentou alta precisão na classificação das classes  
- A consistência entre treino e teste indica ausência de overfitting  
- O Naive Bayes mostrou-se eficiente mesmo em um problema multiclasse  

---

## Conclusão

O algoritmo de Naive Bayes demonstrou excelente desempenho na previsão do score de crédito, sendo capaz de identificar corretamente os padrões nos dados e generalizar bem para novos exemplos.

Este tipo de modelo pode ser utilizado como base para sistemas de decisão em concessão de crédito, auxiliando na avaliação de risco financeiro.

---

