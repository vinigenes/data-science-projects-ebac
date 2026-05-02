# Projeto de Clusterização com K-Means - Pinguins

## Descrição
Este projeto tem como objetivo aplicar o algoritmo de **K-Means** para segmentar dados biológicos de pinguins com base em suas características físicas.

Diferente de aplicações tradicionais em marketing e vendas, este projeto explora o uso de **clusterização em dados científicos**, demonstrando a versatilidade do algoritmo.

---

## Base de Dados
A base utilizada foi o dataset **penguins**, disponível na biblioteca Seaborn, contendo informações sobre três espécies:

- Adelie  
- Chinstrap  
- Gentoo  

### Variáveis disponíveis:
- `bill_length_mm`: comprimento do bico  
- `bill_depth_mm`: profundidade do bico  
- `flipper_length_mm`: comprimento da nadadeira  
- `body_mass_g`: massa corporal  
- `species`: espécie (categórica)  
- `island`: ilha  
- `sex`: sexo  
- `year`: ano  

---

## Etapas do Projeto

### 1. Pré-processamento
- Verificação de valores missing
- Remoção de dados faltantes
- Exclusão de variáveis categóricas (não utilizadas no K-Means)

---

### 2. Análise Exploratória
- Utilização de **pairplot**
- Identificação visual de possíveis agrupamentos

### Insights:
- A espécie **Gentoo** forma um grupo bem separado
- Adelie e Chinstrap apresentam sobreposição
- Indício de **2 a 3 clusters naturais**

---

### 3. Padronização dos Dados
- Aplicação do **RobustScaler**
- Importante para evitar influência de escalas diferentes

---

### 4. Modelagem com K-Means
- Definição de **K = 3 clusters**
- Treinamento do modelo
- Criação da variável `cluster`

---

### 5. Visualização dos Clusters
- Gráficos de dispersão com:
  - `bill_length_mm` vs `bill_depth_mm`
  - `flipper_length_mm` vs `body_mass_g`
- Identificação dos centróides

---

## Resultados
- O modelo conseguiu separar bem um dos grupos (Gentoo)
- Os outros dois clusters apresentaram leve sobreposição
- O K-Means capturou padrões coerentes com as espécies reais

---

## Conclusão
O algoritmo K-Means mostrou-se eficaz na identificação de padrões em dados biológicos.

Mesmo sem utilizar a variável target (species), o modelo conseguiu aproximar bem os agrupamentos reais, demonstrando sua utilidade em problemas não supervisionados.

---

## Aplicações de Clusterização

### 1. Saúde
Agrupamento de pacientes com características clínicas semelhantes para diagnóstico e medicina personalizada.

### 2. Vendas
Segmentação de clientes para campanhas de marketing mais eficientes.

### 3. Agricultura
Identificação de padrões em solo e clima para otimização de produção agrícola.

---

## Tecnologias Utilizadas
- Python
- Pandas
- Seaborn
- Matplotlib
- Scikit-learn

