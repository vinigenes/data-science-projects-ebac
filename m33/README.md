# Projeto de Segmentação de Clientes com K-Means

## Descrição
Este projeto tem como objetivo aplicar o algoritmo de K-Means para segmentar clientes de um shopping com base em características demográficas e comportamentais.

A proposta é identificar diferentes perfis de consumidores e gerar insights que possam apoiar estratégias de marketing e tomada de decisão.

---

## Base de Dados
O dataset utilizado contém informações de 200 clientes de um shopping.

### Variáveis:
- CustomerID: identificador do cliente
- Gender: gênero
- Age: idade
- Annual Income (k$): renda anual
- Spending Score (1-100): pontuação de gastos

---

## Etapas do Projeto

### 1. Exploração de Dados
- Verificação da estrutura do dataset
- Análise de valores nulos (não foram identificados)
- Estatísticas descritivas

Principais observações:
- Idade média em torno de 39 anos
- Renda média aproximada de 60 mil dólares
- Spending Score com média próxima de 50
- Boa dispersão nas variáveis, favorecendo a clusterização

---

### 2. Análise Exploratória
- Distribuição das variáveis numéricas
- Análise de relacionamento entre renda e score de gastos

Observação:
- Relação não linear entre renda e comportamento de consumo
- Indício de formação de grupos distintos de clientes

---

### 3. Tratamento dos Dados
- Remoção da variável CustomerID (não relevante para o modelo)
- Conversão da variável Gender para formato numérico
- Padronização dos dados com StandardScaler

Justificativa:
A padronização é necessária para evitar que variáveis com escalas maiores influenciem desproporcionalmente o cálculo de distância do K-Means.

---

### 4. Modelagem com K-Means

#### Modelo inicial:
- Número de clusters: 5

Resultados:
- Identificação de cinco grupos com características distintas
- Perfis variados de renda e comportamento de consumo

---

### 5. Avaliação dos Clusters

#### Silhouette Score:
- Teste com K variando de 2 a 19
- Melhor resultado observado com K = 14 (aproximadamente 0.43)
- Valores próximos entre K = 9 e K = 11 indicam estabilidade

Interpretação:
- O modelo apresenta separação moderada entre os clusters
- Existe um trade-off entre qualidade do modelo e interpretabilidade

---

### 6. Análise dos Perfis de Clientes

Principais grupos identificados:
- Clientes com alta renda e baixo consumo
- Clientes jovens com alto nível de gastos
- Clientes com renda e consumo moderados
- Clientes mais velhos com comportamento conservador
- Grupos intermediários com padrões mistos

---

## Conclusão
O algoritmo K-Means foi eficaz na segmentação dos clientes, permitindo identificar diferentes perfis com base em renda, idade e comportamento de consumo.

Apesar do melhor desempenho técnico com maior número de clusters, a escolha de K deve considerar também a interpretabilidade dos resultados.

---

## Aplicações Práticas
- Segmentação de clientes para campanhas de marketing
- Personalização de ofertas
- Identificação de clientes com alto potencial de consumo
- Estratégias de retenção e engajamento

---

## Possíveis Melhorias
- Utilizar método do cotovelo (Elbow Method) para escolha de K
- Aplicar PCA para visualização dos clusters
- Testar outros algoritmos de clusterização (DBSCAN, Hierarchical Clustering)
- Engenharia de atributos

---

## Tecnologias Utilizadas
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

