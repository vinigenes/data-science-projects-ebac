# Operações Básicas com SQL

## Descrição do Projeto

Este projeto tem como objetivo aplicar conceitos fundamentais de **SQL** utilizando uma base de dados de vendas. A atividade foi desenvolvida em ambiente Python com SQLite, permitindo a execução de consultas diretamente em memória.

O foco principal está na utilização de operações básicas como:

- SELECT
- DISTINCT
- COUNT
- WHERE
- GROUP BY
- ORDER BY
- LIMIT
- Funções agregadas

---

## Tecnologias Utilizadas

- Python
- Pandas
- SQLite
- SQL

---

## Preparação do Ambiente

Os dados foram carregados a partir de um arquivo CSV e inseridos em uma base SQLite em memória para execução das consultas.

---

## Consultas Realizadas

### 1. Produtos Distintos

Retorna todos os produtos únicos presentes na base:

```sql
SELECT DISTINCT PRODUTO
FROM tb_vendas;