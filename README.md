# Primeiros Passos MySQL

Este repositório contém atividades realizadas no MySQL para praticar conceitos básicos de manipulação de dados em um banco de dados.

## Atividades Realizadas:

Antes de iniciar as atividades devemos criar o DATABASE ao qual vamos usar nesse projeto introdutório:

CREATE DATABASE IF NOT EXISTS conceitos_basicos;
USE conceitos_basicos;

### 1. Consulta para Exibir Todos os Dados de uma Tabela Específica

Para visualizar todos os dados da tabela `CLIENTES`, foi executada a seguinte consulta:

```sql
SELECT * FROM CLIENTES;
