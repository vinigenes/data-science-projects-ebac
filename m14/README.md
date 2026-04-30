# Pré-processamento de Dados - Churn em Telecomunicações

## Objetivo

Este projeto tem como objetivo aplicar técnicas de limpeza e pré-processamento de dados em uma base de churn do setor de telecomunicações, preparando os dados para etapas futuras de modelagem.

---

## Base de Dados

O conjunto de dados contém informações sobre clientes de serviços de telecomunicação, incluindo:

- CustomerID: Identificador único do cliente  
- Genero: Gênero do cliente  
- Idoso: Indica se o cliente possui mais de 60 anos  
- Casado: Estado civil  
- Dependents: Indica se possui dependentes  
- Tempo_como_Cliente: Tempo de permanência na empresa (meses)  
- PhoneService: Serviço telefônico contratado  
- Servico_Internet: Tipo de internet  
- Servico_Seguranca: Serviço de segurança  
- Suporte_Tecnico: Uso de suporte técnico  
- StreamingTV: Serviço de streaming  
- Tipo_Contrato: Tipo de contrato  
- PaymentMethod: Forma de pagamento  
- Pagamento_Mensal: Valor mensal pago  
- Total_Pago: Valor total pago  
- Churn: Indica evasão do cliente  

---

## Tecnologias Utilizadas

- Python  
- pandas  
- matplotlib  
- seaborn  

---

## Etapas do Pré-processamento

### 1. Ajuste de Tipos de Dados

Conversão das variáveis para os tipos adequados, garantindo consistência e melhor desempenho nas análises.

---

### 2. Tratamento de Valores Faltantes

**Identificação:**  
Análise da quantidade e percentual de valores nulos por coluna.

**Remoção:**  
Linhas com valores ausentes em colunas críticas foram removidas.

Justificativa:
- A remoção foi aplicada apenas em variáveis essenciais  
- Algumas colunas apresentavam alto volume de dados faltantes, inviabilizando imputação  

**Imputação:**  
Valores faltantes na variável `Pagamento_Mensal` foram substituídos pela mediana.

Justificativa:
- A distribuição da variável é assimétrica  
- A mediana é menos sensível a valores extremos  

---

### 3. Padronização de Dados

Padronização de textos para minúsculo e correção de inconsistências em variáveis categóricas.

Justificativa:
- Evita duplicidade de categorias  
- Garante consistência para análises futuras  

---

### 4. Renomeação de Colunas

As colunas foram renomeadas para o padrão em inglês.

Justificativa:
- Facilita integração com bibliotecas e modelos  
- Mantém padrão mais utilizado em projetos de dados  

---

## Conclusão

As principais etapas realizadas foram:

- Correção de tipos de dados  
- Tratamento de valores faltantes  
- Padronização de categorias  
- Renomeação de variáveis  

Essas transformações garantem maior qualidade dos dados e preparam o dataset para análises mais avançadas e modelagem preditiva.

---

