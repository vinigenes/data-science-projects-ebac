# Projeto de Classificação de Incêndios com Validação Cruzada

## Descrição
Este projeto tem como objetivo prever a ocorrência de incêndios com base em variáveis ambientais coletadas por sensores, utilizando um modelo de classificação avaliado por validação cruzada (cross-validation).

A proposta é garantir uma avaliação mais robusta do modelo, reduzindo a dependência de uma única divisão entre treino e teste.

---

## Base de Dados
O dataset contém informações ambientais coletadas em tempo real por sensores.

### Variáveis:
- UTC: tempo em segundos
- Temperature[C]: temperatura do ar
- Humidity[%]: umidade do ar
- TVOC[ppb]: compostos orgânicos voláteis
- eCO2[ppm]: concentração de CO2 equivalente
- Raw H2: hidrogênio bruto
- Raw Ethanol: etanol bruto
- Pressure[hPA]: pressão do ar
- PM1.0: material particulado fino
- PM2.5: material particulado médio
- NC0.5, NC1.0, NC2.5: contagem de partículas
- CNT: contador de amostras

### Variável Target:
- fire_alarm: indicador de incêndio (0 = não, 1 = sim)

---

## Etapas do Projeto

### 1. Pré-processamento
- Padronização dos nomes das colunas
- Verificação de tipos de dados
- Verificação de valores nulos (não foram identificados)
- Remoção de variáveis não relevantes (quando aplicável)

---

### 2. Escolha do Modelo
Foi utilizada a Regressão Logística.

Justificativa:
- Problema de classificação binária
- Modelo simples e eficiente como baseline
- Boa interpretação e desempenho com variáveis numéricas

---

### 3. Preparação dos Dados
- Separação em X (features) e y (target)
- Instanciação do modelo com ajuste de iterações

---

### 4. Validação Cruzada

- Técnica utilizada: K-Fold Cross Validation
- Número de folds: 5
- Métricas avaliadas:
  - Accuracy
  - Precision
  - Recall
  - F1-score

---

### 5. Resultados por Fold

Resumo dos resultados:

- Fold 1:
  - Acurácia: 0.8038
  - Precisão: 0.7846
  - Recall: 1.0000
  - F1-score: 0.8793

- Fold 2:
  - Acurácia: 0.9717
  - F1-score: 0.9806

- Fold 3:
  - Acurácia: 0.9284
  - Recall menor (0.8999)

- Fold 4:
  - Desempenho perfeito (1.0000 em todas as métricas)

- Fold 5:
  - Acurácia: 0.8998
  - F1-score: 0.9258

---

### 6. Resultado Final (Média)

- Acurácia média: 0.9207
- Precisão média: 0.9460
- Recall médio: 0.9548
- F1-score médio: 0.9466

---

## Análise dos Resultados
- O modelo apresentou desempenho elevado em todas as métricas
- Boa capacidade de identificar corretamente casos positivos (alto recall)
- Equilíbrio consistente entre precisão e recall
- Variação entre folds indica sensibilidade à divisão dos dados

---

## Conclusão
A validação cruzada demonstrou que o modelo possui boa capacidade de generalização, apresentando desempenho consistente na maioria dos folds.

Apesar de algumas variações, os resultados indicam que a Regressão Logística é uma abordagem adequada para este problema.

---

## Possíveis Melhorias
- Aplicar padronização dos dados (StandardScaler)
- Testar outros modelos (Random Forest, Gradient Boosting)
- Ajuste de hiperparâmetros
- Análise de importância das variáveis
- Balanceamento de classes (se necessário)

---

## Tecnologias Utilizadas
- Python
- Pandas
- Scikit-learn

