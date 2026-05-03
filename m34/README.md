# Projeto de Regressão Polinomial para Previsão de Aluguel

## Descrição
Este projeto tem como objetivo prever o valor de aluguel de imóveis com base na metragem, utilizando regressão polinomial.

A proposta é avaliar como a complexidade do modelo (grau do polinômio) impacta sua capacidade de explicar os dados e generalizar previsões.

---

## Base de Dados
A base contém informações sobre imóveis, incluindo variáveis relacionadas ao preço e características físicas.

### Variáveis utilizadas:
- Metragem: variável independente
- Valor_Aluguel: variável alvo

---

## Etapas do Projeto

### 1. Exploração de Dados
- Análise da estrutura do dataset
- Estatísticas descritivas
- Verificação de consistência dos dados

Observação:
- A variável metragem apresenta relação positiva com o valor do aluguel

---

### 2. Pré-processamento
- Seleção da variável Metragem como preditora
- Aplicação de transformação polinomial

---

### 3. Modelagem - Grau 2

- Transformação com PolynomialFeatures (degree = 2)
- Divisão em treino e teste (80/20)
- Treinamento com Regressão Linear

#### Resultados:
- R²: aproximadamente 0.57
- MAE: aproximadamente 1225
- MSE: aproximadamente 4.65 milhões

Análise:
- O modelo consegue capturar a tendência geral dos dados
- Aproximadamente 57% da variabilidade do aluguel é explicada pela metragem
- Indicação de que outras variáveis também influenciam o preço

---

### 4. Visualização
- Gráfico de dispersão com dados reais
- Curva de regressão polinomial ajustada

Observação:
- O modelo suaviza extremos e não captura totalmente a variabilidade dos dados

---

### 5. Modelagem - Grau 4

- Transformação com PolynomialFeatures (degree = 4)
- Treinamento de novo modelo

#### Resultados:
- R²: aproximadamente 0.56
- MAE: aproximadamente 1194
- MSE: aproximadamente 4.78 milhões

---

### 6. Comparação dos Modelos

Observações:
- O modelo de grau 4 apresentou leve melhora no MAE
- Houve piora no R² e aumento do MSE
- Indício de aumento de complexidade sem ganho de generalização

Conclusão:
- O modelo de grau 2 apresentou melhor equilíbrio entre simplicidade e desempenho
- O modelo de grau 4 pode estar sofrendo de overfitting

---

## Conceitos de Regularização

### Ridge Regression
Utiliza penalização L2, reduzindo a magnitude dos coeficientes sem eliminá-los. Ajuda a evitar overfitting mantendo todas as variáveis no modelo.

### Lasso Regression
Utiliza penalização L1, podendo zerar coeficientes. Realiza seleção automática de variáveis, simplificando o modelo.

### Elastic Net
Combina L1 e L2. Permite reduzir coeficientes e eliminar variáveis ao mesmo tempo. Indicado para cenários com variáveis correlacionadas.

---

## Conclusão
O modelo de regressão polinomial demonstrou capacidade moderada de previsão utilizando apenas a metragem como variável explicativa.

O aumento da complexidade do modelo não resultou em melhoria significativa, reforçando a importância do equilíbrio entre ajuste e generalização.

---

## Possíveis Melhorias
- Inclusão de novas variáveis explicativas
- Aplicação de técnicas de regularização (Ridge, Lasso, Elastic Net)
- Teste de modelos mais robustos
- Análise de outliers

---

## Tecnologias Utilizadas
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

