# Banco de Dados E‑Commerce

Este projeto faz parte do Bootcamp Klabin – Transforme Dados em Insights Estratégicos e foi desenvolvido como desafio prático de modelagem e implementação de banco de dados relacional.  

---

## Contexto do Projeto

O sistema foi modelado para representar as principais operações de uma loja online:  
- cadastro de clientes (PF e PJ);  
- produtos, categorias e fornecedores;  
- pedidos compostos por múltiplos itens e respectivos pagamentos;  
- entregas com status e rastreamento;  
- possibilidade de devoluções/cancelamentos conforme regras do domínio.

---

## Estrutura e Propósito

| Tipo | Nome / Caminho |
|------|-----------------|
| **DDL** | [`01_DDL_ecommerce.sql`](scripts/01_DDL_ecommerce.sql) |
| **DML** | [`02_DML_ecommerce.sql`](scripts/02_DML_ecommerce.sql) |
| **DQL** | [`03_DQL_ecommerce.sql`](scripts/03_DQL_ecommerce.sql) |
| **Diagrama Relacional** | [`diagram_ecommerce.svg`](diagramas/diagram_ecommerce.svg) |

---

## Estrutura Lógica e Modelagem

O banco de dados é composto por entidades centrais que refletem o fluxo de um e‑commerce:

- **Cliente** → entidade base, especializada em `Cliente_PF` e `Cliente_PJ`.  
- **Produto** → item comercializado, com vínculo a **Categoria**.  
- **Pedido** → entidade transacional que relaciona cliente aos **ItensPedido**.  
- **Pagamento** → controle de valores, formas de pagamento e status financeiro por pedido.  
- **Entrega** → informações de envio, status e código de rastreio.  
- **Categoria** e **Fornecedor** → catálogos de apoio para organização e suprimento.

O modelo foi projetado para refletir a operação de uma loja virtual, com integridade entre clientes e pedidos, rastreabilidade de itens e controle de fluxo financeiro e logístico por pedido.

---

## Consultas Analíticas (KPIs)

As consultas DQL desenvolvidas exploram os dados do banco e simulam indicadores de gestão, como:

- Ticket médio por pedido e por cliente;  
- Faturamento por período (dia/mês);  
- Produtos mais vendidos e categorias com maior receita;  
- Participação por forma de pagamento;  
- Ranking de clientes por valor total e volume de pedidos;  
- Distribuição PF x PJ;  
- Status de entrega e taxa de cancelamento/devolução.

---

## Estrutura de Diretórios

```
ecommerce-database/
│
├── README.md
│
├── diagramas/
│   └── modelo_relacional_ecommerce.svg
│
├── scripts/
│   ├── 01_create_database_ecommerce.sql
│   ├── 02_insert_data_ecommerce.sql
│   └── 03_queries_ecommerce.sql

```