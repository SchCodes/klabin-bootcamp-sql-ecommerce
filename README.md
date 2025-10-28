# 🧩 Projeto SQL E-commerce — Klabin Bootcamp DIO

> **Desafio de projeto** desenvolvido no Bootcamp **Klabin - Data & Analytics com SQL**, com o objetivo de replicar e aprimorar o modelo de banco de dados de um sistema de e-commerce, aplicando fundamentos de modelagem relacional, criação de schema e elaboração de consultas analíticas (KPIs).

---

## 🧭 Objetivo do Projeto

O projeto foi desenvolvido como **exercício acadêmico** para consolidar conhecimentos em **modelagem e manipulação de dados com SQL**.  
Partindo de um modelo de referência apresentado no desafio, foi proposta uma **versão expandida e organizada** do banco de dados, com o acréscimo de elementos técnicos e consultas analíticas que simulam cenários comuns em aplicações de e-commerce.

Todos os dados utilizados neste projeto são **totalmente fictícios** e foram criados **exclusivamente para fins de aprendizado**.

---

## 🧱 Estrutura do Repositório

| Arquivo | Descrição |
|----------|------------|
| [`01_DDL_ecommerce.sql`](./01_DDL_ecommerce.sql) | Criação completa do esquema de banco de dados (tabelas, chaves, constraints e triggers). |
| [`02_DML_ecommerce.sql`](./02_DML_ecommerce.sql) | Inserção de dados simulados (clientes PF/PJ, produtos, pedidos, entregas). |
| [`03_DQL_ecommerce.sql`](./03_DQL_ecommerce.sql) | Consultas analíticas e indicadores de desempenho (KPIs financeiros, de clientes, produtos e logística). |
| [`diagram_ecommerce.svg`](./diagram_ecommerce.svg) | Diagrama EER exportado do MySQL Workbench, com layout organizado. |

---

## 🧩 Diagrama do Banco de Dados

Visualização da modelagem lógica e dos relacionamentos entre as entidades:

![Diagrama do Banco de Dados](./diagram_ecommerce.svg)

---

## 🚀 Melhorias Implementadas

Durante o desenvolvimento, o projeto foi **além da simples replicação** do modelo de referência, incorporando ajustes estruturais e analíticos que reforçam a integridade e a coerência dos dados.

### 🔹 Modelagem e Integridade
- Separação clara entre **ClientePF** e **ClientePJ**, mantendo relacionamento 1:1 com `Cliente`.  
- Inclusão de **chaves estrangeiras e constraints** com `ON DELETE CASCADE`.  
- Uso de **tipos ENUM** para padronizar status de pedidos e entregas.  
- Criação de **tabela de Log_Acoes** e **triggers** para registrar exclusões e anonimizações (simulação de práticas de auditoria e LGPD).

### 🔹 Dados e Diversificação
- Expansão do conjunto de registros para **16 clientes (PF e PJ)**.  
- Inclusão de **clientes sem pedidos** para permitir análise de inatividade.  
- Adição de **25 pedidos** com diferentes status (Pago, Enviado, Entregue, Cancelado).  
- Variedade ampliada de **produtos e categorias**, cobrindo cenários de vendas e estoque.  

### 🔹 Consultas Analíticas (KPIs)
- Adição de **KPI combinado** para exibir taxa e número de cancelamentos.  
- Inclusão de **KPI de clientes sem pedidos**, permitindo avaliar engajamento.

---

## 📊 Indicadores de Desempenho (KPIs)

| Categoria | Indicadores |
|------------|-------------|
| **Financeiro** | Valor total de vendas, valor perdido por cancelamento, ticket médio, receita mensal, taxa e número de cancelamentos. |
| **Clientes** | Clientes ativos, top 5 clientes por gasto, gasto médio, clientes acima da média, distribuição PF/PJ, clientes sem pedidos. |
| **Produtos** | Produtos mais vendidos, produtos com maior receita, categorias mais rentáveis, produtos sem vendas. |
| **Logística** | Entregas por status, percentual concluído, tempo médio de entrega, pendências, clientes com mais entregas. |

---

## 🧠 Ferramentas e Tecnologias

- **MySQL Workbench 8.0** — modelagem EER e execução de scripts SQL.  
- **SQL (DDL, DML e DQL)** — criação, inserção e análise de dados.  
- **GitHub** — versionamento e documentação do projeto.  
- **Exportação SVG** — representação vetorial do diagrama relacional.

---

## 🧩 Autor

**Ericson Schmidt Bicalho**  
📎 GitHub: [@SchCodes](https://github.com/SchCodes)

---

> *Este projeto é parte de um exercício educacional do Bootcamp Klabin (DIO).  
Todos os dados e entidades foram criados apenas para fins de estudo e prática de SQL, sem qualquer correspondência com dados reais.*
