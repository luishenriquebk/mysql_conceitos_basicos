# Conceitos Básicos MySQL 🐬

Este repositório contém atividades realizadas no MySQL para praticar conceitos básicos de manipulação de dados em um banco de dados.
#### Link do projeto: 
https://drive.google.com/file/d/1U2HTin1kEvvbyufu3iesRQeBVP6JE0Al/view?usp=sharing

## Atividades Realizadas:

Antes de iniciar as atividades devemos criar o DATABASE ao qual vamos usar nesse projeto introdutório:

```sql
CREATE DATABASE IF NOT EXISTS conceitos_basicos;
USE conceitos_basicos;
```

### 1. Consulta para Exibir Todos os Dados de uma Tabela Específica:

Para visualizar todos os dados da tabela `CLIENTES`, foi executada a seguinte consulta:

```sql
CREATE TABLE CLIENTES (
	id_cliente INT PRIMARY KEY AUTO_INCREMENT,
    nome_cliente VARCHAR(100) NOT NULL,
    sexo_cliente VARCHAR(1),
    idade_cliente INT UNSIGNED NOT NULL 
); -- CRIANDO TABLE CLIENTES;

SELECT * 
FROM CLIENTES; -- CONSULTA COM TODOS OS DADOS DA TABLE CLIENTES;
```



### 2. Inserindo alguns valores na Tabela ClIENTES:

Para inserir os valores dentro da tabela `CLIENTES` foram executados os seguinte comandos:

```sql
INSERT INTO CLIENTES (NOME_CLIENTE, SEXO_CLIENTE, IDADE_CLIENTE) -- INSERINDO VALORES TABLE CLIENTES;
VALUES ('LUIS HENRIQUE', 'M', 25),
	   ('LUCAS', 'F', 23),
	   ('SAMUEL', '',  20);

| id_cliente | nome_cliente | sexo_cliente | idade_cliente |
| 1          | LUIS HENRIQUE| M            | 25            |
| 2          | LUCAS        | F            | 23            |
| 3          | SAMUEL       |              | 20            |
```

### 3. Atualize o valor de uma coluna em um registro específico:

Para atualizar um valor específico na tabela `CLIENTES` foram utilizando os seguintes comandos:

```sql
UPDATE CLIENTES
SET SEXO_CLIENTE = 'M'
WHERE NOME_CLIENTE = 'LUCAS'; -- ATUALIZANDO O SEXO_CLIENTE PARA 'M' PARA O CLIENTE 'LUCAS';

UPDATE CLIENTES
SET SEXO_CLIENTE = 'M'
WHERE NOME_CLIENTE = 'SAMUEL'; -- ATUALIZANDO O SEXO_CLIENTE PARA 'M' PARA O CLIENTE 'SAMUEL';

| id_cliente | nome_cliente | sexo_cliente | idade_cliente |
| 1          | LUIS HENRIQUE| M            | 25            |
| 2          | LUCAS        | M            | 23            |
| 3          | SAMUEL       | M            | 20            |
```

### 4. Excluir um registro da tabela:

Para excluir um registro(row) da tabela `CLIENTES` foi executado o seguinte comando:

```sql
DELETE FROM CLIENTES
WHERE NOME_CLIENTE = 'SAMUEL'; -- DELETANDO UM REGISTRO DO CLIENTE 'SAMUEL' DA TABLE 'CLIENTES';

| id_cliente | nome_cliente | sexo_cliente | idade_cliente |
| 1          | LUIS HENRIQUE| M            | 25            |
| 2          | LUCAS        | M            | 23            |
```
