# Projeto de Previsão de Doenças Cardiovasculares com Regressão Logística

## Descrição
Este projeto tem como objetivo construir um modelo de Machine Learning capaz de prever a probabilidade de um paciente desenvolver doenças cardiovasculares com base em dados clínicos e comportamentais.

O modelo utilizado foi a **Regressão Logística**, amplamente aplicada em problemas de classificação binária.

---

## Base de Dados
A base contém informações reais de pacientes, incluindo:

- `age`: idade  
- `gender`: gênero (1 = masculino, 2 = feminino)  
- `height`: altura  
- `weight`: peso  
- `gluc`: nível de glicose  
- `cholesterol`: nível de colesterol  
- `smoke`: fumante (1 = sim, 0 = não)  
- `alco`: consumo de álcool (1 = sim, 0 = não)  
- `active`: atividade física (1 = sim, 0 = não)  
- `cardio_disease`: presença de doença cardiovascular (target)  

---

## Etapas do Projeto

### 1. Pré-processamento
- Conversão de tipos de dados
- Tratamento de valores inconsistentes
- Identificação e tratamento de outliers
- Verificação de dados faltantes

### 2. Análise Exploratória (EDA)
- Análise bivariada entre variáveis e a variável alvo
- Identificação de padrões importantes:
  - Idade mais elevada → maior risco
  - Peso elevado → maior incidência
  - Colesterol alto → forte associação com doença

### 3. Correlação
- Construção da matriz de correlação
- Identificação de relações relevantes entre variáveis

### 4. Preparação dos Dados
- Separação em treino e teste (70/30)
- Padronização com `StandardScaler`
- Verificação de balanceamento das classes

### 5. Modelagem
- Treinamento com Regressão Logística
- Extração de coeficientes e intercepto

### 6. Avaliação
Métricas utilizadas:
- Accuracy
- Precision
- Recall
- F1-score
- Matriz de confusão
- Curva ROC
- AUC

### Resultados
- Acurácia: ~64%
- AUC: ~0.70

O modelo apresentou desempenho **razoável**, sendo capaz de distinguir entre pacientes com e sem doença cardiovascular melhor que o acaso.

---

## Conclusão
O modelo de regressão logística demonstrou ser uma abordagem eficiente para o problema proposto, embora ainda haja espaço para melhorias, como:

- Testar outros algoritmos (Random Forest, XGBoost)
- Ajuste de hiperparâmetros
- Engenharia de features
- Balanceamento com SMOTE

---

## Tecnologias Utilizadas
- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn
- Imbalanced-learn

