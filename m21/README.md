# Projeto de Credit Score - Árvore de Decisão

## Descrição do Projeto

Este projeto tem como objetivo aplicar o algoritmo de **Árvore de Decisão** em uma base de dados de crédito, com o intuito de prever o **Credit Score** dos clientes.

A base utilizada já passou por etapas anteriores de tratamento, balanceamento de classes, transformação de variáveis categóricas e separação em conjuntos de treino e teste.

---

## Etapas do Projeto

### 1. Validação dos Dados

Inicialmente, foram carregadas as bases de treino e teste:

- Verificação do número de linhas entre X e y
- Conferência das colunas
- Validação da variável alvo
- Análise do balanceamento das classes

---

### 2. Aplicação da Árvore de Decisão

Foi utilizado o modelo de árvore de decisão com:

- Critério: **Gini**
- `random_state = 0`

O modelo foi treinado utilizando os dados de treino, aprendendo padrões entre as variáveis preditoras e o **Credit Score**.

---

### 3. Avaliação do Modelo

#### Métricas utilizadas:

- Acurácia
- Matriz de Confusão
- Precision, Recall e F1-score

#### Resultados:

- **Acurácia treino:** 1.00  
- **Acurácia teste:** ~0.97  

#### Análise:

O modelo apresentou excelente desempenho, com alta capacidade de generalização. A pequena diferença entre treino e teste indica um leve overfitting, comum em árvores de decisão.

A matriz de confusão mostrou poucos erros, demonstrando boa capacidade de classificação entre as classes.

---

### 4. Visualização da Árvore

A árvore foi plotada para análise interpretável do modelo.

#### Insights:

- A variável **Income** foi a mais importante na primeira divisão
- **Home Ownership_Rented** também teve forte influência
- Nós finais com **gini = 0** indicam alta pureza nas classificações

---

### 5. Importância das Variáveis

As duas principais features identificadas foram:

- Income
- Home Ownership_Rented

---

### 6. Modelo com Top 2 Features

Foi treinado um novo modelo utilizando apenas as duas variáveis mais importantes.

#### Resultados:

- Acurácia manteve-se alta, porém ligeiramente inferior ao modelo completo

#### Conclusão:

Apesar da boa performance, o modelo com todas as variáveis apresentou melhor capacidade preditiva.

---

### 7. Comparação com Naive Bayes

| Modelo            | Acurácia Teste |
|------------------|---------------|
| Naive Bayes      | 1.00          |
| Árvore de Decisão| ~0.97         |

#### Conclusão:

- O **Naive Bayes** apresentou melhor desempenho nos dados de teste
- A **Árvore de Decisão** se destacou pela interpretabilidade

---

## Conclusão Final

Ambos os modelos apresentaram resultados excelentes para previsão de Credit Score.

- **Naive Bayes**: melhor desempenho preditivo  
- **Árvore de Decisão**: melhor interpretabilidade  

A escolha do modelo depende do objetivo do projeto:

- Máxima precisão → Naive Bayes  
- Explicabilidade → Árvore de Decisão  

---

## Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Seaborn
- Matplotlib
- Scikit-learn

---