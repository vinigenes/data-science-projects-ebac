# Projeto de Dashboard de E-commerce

## Descrição do Projeto

Este projeto tem como objetivo aplicar conceitos de **análise de dados, SQL e visualização** em um cenário real de e-commerce. A proposta consiste em integrar dados de transações com informações de clientes para gerar insights relevantes e construir um dashboard interativo.

---

## Objetivos

- Realizar tratamento e integração de dados utilizando SQL
- Consolidar informações de múltiplas tabelas
- Exportar dados para análise
- Criar um dashboard interativo com métricas de negócio

---

## Base de Dados

O projeto utiliza duas tabelas principais:

### Tabela de Transações
Contém informações sobre as compras realizadas:

- ID da transação
- ID do cliente
- Categoria
- Preço
- Tipo de cartão

### Tabela de Clientes
Contém dados pessoais dos clientes:

- ID do cliente
- Nome
- Gênero
- Profissão
- Estado

---

## Integração dos Dados

Foi realizado um **INNER JOIN** entre as tabelas utilizando a coluna `id_client`.

```sql
SELECT
    t.id_client,
    t.Category,
    t.Price,
    t.[Card Type],
    c.First_name,
    c.Gender,
    c.Job_Title,
    c.state_name
FROM tb_transacoes t
INNER JOIN tb_clientes c
ON t.id_client = c.Id_client;