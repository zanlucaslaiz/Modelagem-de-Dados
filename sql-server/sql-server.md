# SQL SERVER - Strutured Query language

* SQL é uma Linguagem de Consulta Estruturada padrão para acesso a Bancos de Dados.
* Usada em inúmeros sistemas, como MySQL, SQL Server, Oracle, Sybase, Access, DB2, PostgreSQL, etc.
* Cada um desses sistemas pode utilizar um “dialeto” diferente do SQL, como T-SQL (SQL Server), PL/SQL (Oracle), JET SQL (Access), etc.


## Funções do SQL 

* Permite o acesso a dados em SGBDR.
* Permite definir os dados no banco de dados e manipulá-los.
* Pode ser embutido em outras linguagens usando módulos SQL, bibliotecas, etc.
* Permite criar e excluir bancos de dados e tabelas.
* Permite a criação de Visões (Exibições), Stored Procedures e Funções em um banco de dados.
* Permite configurar permissões de acesso em tabelas, procedimentos e visões.

## Grupos de comando

Os comandos SQL podem ser divididos em quatro grupos principais:

* DDL - Data Definition Language
* DML - Data manipulation language
* DCL - Data Control language
* DQL - Data Query Language

### DDL - Data Definition Language
| comando |                          descrição                                                     |
| --------|----------------------------------------------------------------------------------------|
| CREATE  | Cria uma nova tabela, visão ou outro objeto no BD.                                     |
| ALTER   | Modifica um objeto existente no BD, como uma tabela.                                   |
| DROP    |Exclui uma tabela inteira, uma exibição de uma tabela ou outro objeto no banco de dados.|

### DML - Data manipulation language

| Comando   | Descrição                 |
|-----------|---------------------------|
| INSERT    | Cria um registro (linha)  |
| UPDATE    | Modifica registros        |
| DELETE    |Exclui registros           |

### DCL - Data Control language

| Comando   | Descrição                                  |
|-----------|--------------------------------------------|
| GRANT     | Dá privilégios a um usuário                |
| REVOKE    | Retira privilégios fornecidos a um usuário |


### DQL - Data Query Language

| Comando   | Descrição                                           |
|-----------|-----------------------------------------------------|
| SELECT    |obtém registros especificados de uma ou mais tabelas.|

## SGBDR
* Sistema gerenciador de banco de dados relacional 
* Trata-se de um sistema de gerenciamento de banco de dados baseado no modelo relacional introduzido por E.F. Codd.

### Composição de um banco de dados
Tabelas
campos (colunas)
registros (linhas)

### TABELAS 
* Objetos onde são armazenados os dados em um banco de dados relacional.
* Uma tabela é uma coleção de entradas de dados relacionados e consiste em linhas e colunas.

### CAMPO 
* São entidades que representam os atributos dos dados, como nome, data de nascimento, salario, preço, etc.
* Um campo é uma coluna em uma tabela que mantém informações especificas sobre cada registro.

### REGISTRO
* linha, ou tuplas
* Cada entrada individual em uma tabela. Trata-se de um conjunto de campos relacionados que caracterizam os dados de uma entidade única.

Comentários no SQL Server:
-- mais o comentário.

### USE

O comando USE instrui o SGBDR a utilizar o banco de dados especificado para rodar os comandos.
Eventualmente pode acabar rodando no banco de dados errado, o comando USE evita isso.

Sintaxe:
    
    USE nome do banco_de_dados

sp_helpdb:

Informa o tamanho, taxa de crescimento, e local do banco de dados. 

Sintaxe:

    sp_helpdb nome_do_banco_de_dados

Informa os indices:

    sp_help + NomeDaTabela

informa os indices, chaves e campos, atributos tipos de atributos de uma tabela (stored procedures, comandos pré-programados)