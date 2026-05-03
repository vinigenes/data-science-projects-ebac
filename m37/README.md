# Projeto de Previsão de Intenção de Compra em E-commerce

## Descrição
Este projeto tem como objetivo prever a intenção de compra de clientes em um ambiente de e-commerce, utilizando dados demográficos e comportamentais.

A proposta é identificar padrões que indiquem maior propensão à compra online, permitindo apoiar estratégias de marketing e tomada de decisão.

---

## Base de Dados
O dataset contém informações sobre clientes e seus comportamentos de consumo.

### Variáveis principais:
- year_birth: ano de nascimento
- education: nível de escolaridade
- marital_status: estado civil
- income: renda anual
- kidhome: número de crianças na casa
- recency: dias desde a última compra
- complain: indicador de reclamação
- mnt*: gastos por categoria de produto
- num*: comportamento de compra e visitas
- webpurchases: variável alvo (0 = não compra, 1 = compra)

---

## Etapas do Projeto

### 1. Exploração e Limpeza
- Padronização dos nomes das colunas
- Tratamento de valores nulos (substituição pela mediana)
- Criação da variável idade
- Remoção de valores inconsistentes
- Conversão de variáveis categóricas (one-hot encoding)

---

### 2. Análise Exploratória

Principais análises realizadas:
- Distribuição da variável alvo
- Idade vs compras online
- Renda vs compras online
- Gastos totais vs compras
- Visitas ao site vs compras
- Matriz de correlação

Principais insights:
- Clientes com maior renda tendem a comprar mais online
- Maior gasto total está fortemente associado à compra
- Clientes com crianças tendem a comprar menos
- Alta frequência de visitas nem sempre resulta em conversão
- Idade apresenta influência moderada

---

### 3. Pré-processamento
- Análise de correlação com a variável alvo
- Separação em X (features) e y (target)
- Divisão em treino e teste (70/30 com estratificação)
- Padronização dos dados com StandardScaler

---

### 4. Modelagem

Modelos utilizados:

#### Regressão Logística
- Modelo baseline
- Aplicado em dados padronizados

#### Random Forest
- Modelo baseado em árvores
- Maior capacidade de capturar relações não lineares

---

### 5. Avaliação dos Modelos

#### Regressão Logística:
- Accuracy: 84,97%
- Precision: 0,867
- Recall: 0,829
- F1-score: 0,848

Análise:
- Bom desempenho geral
- Equilíbrio entre precisão e recall
- Alguns erros de classificação

---

#### Random Forest:
- Accuracy: 91,96%
- Precision: 0,897
- Recall: 0,950
- F1-score: 0,923

Análise:
- Melhor desempenho em todas as métricas
- Maior capacidade de generalização
- Redução significativa de erros

---

## Comparação dos Modelos
- O Random Forest apresentou desempenho superior em relação à Regressão Logística
- Melhor capacidade de capturar padrões complexos
- Maior robustez na classificação

---

## Conclusão
O modelo Random Forest foi o mais eficiente para prever a intenção de compra dos clientes, apresentando melhor desempenho em todas as métricas avaliadas.

Os resultados indicam que variáveis relacionadas ao comportamento de consumo e renda possuem forte influência na decisão de compra.

---

## Aplicações Práticas
- Segmentação de clientes com alta propensão de compra
- Direcionamento de campanhas de marketing
- Personalização de ofertas
- Otimização da experiência do usuário

---

## Possíveis Melhorias
- Ajuste de hiperparâmetros dos modelos
- Aplicação de técnicas de balanceamento
- Engenharia de atributos
- Teste de modelos mais avançados (XGBoost, LightGBM)
- Validação cruzada

---

## Tecnologias Utilizadas
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

