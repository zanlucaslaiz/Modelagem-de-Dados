# Banco de dados relacional

Um banco de dados relacional é uma coleção de relações, que são tabelas bidimensionais, onde os dados são armazenados. Como por exemplo, podemos querer armazenar dados sobre os clientes de uma loja. Para isso, criamos tabelas para guardar diferentes conjuntos de dados relacionados a esses clientes, como dados pessoais, dados de compras, créditos e outras.

## Componentes de um banco de dados relacional

### TABELA

Estrutura básica de armazenamento no SGBDR. Armazena todos os dados necessários sobre algo do mundo real, como clientes, pedidos ou produtos. Também chamada de Relação. Um banco de dados relacional pode conter uma ou mais Tabelas.

### TUPLA

Tupla ou linha/registro, representa todos os dados requeridos por uma determinada ocorrência de entidade em particular. Por exemplo, os dados de um cliente especifico. Cada linha em uma tabela deve ser identificada por uma chave primária, de modo a não haver duplicação de registros.

### COLUNA

Unidade que armazena um tipo especifico de dado (valor) - ou não armazena nada, com valor nulo. Esta é uma coluna não-chave, significando que seu valor pode se repetir em outras linhas da tabela.

### RELACIONAMENTO 

Associação entre as entidades (tabelas), conectadas por chave primárias e chaves estrangeiras.

### OUTROS
indices, Stored Procedure, Triggers, etc.

### CHAVE PRIMARIA

Coluna (atributo) que identifica um registro de forma exclusiva na tabela. por exemplo, o CPF de um cliente, contendo um valor que não se repete na relação.

### CHAVE ESTRANGEIRA

Coluna que define como as tabelas se relacionam umas com as outras. Uma FK se refere a uma PK ou uma chave única em outra tabela (ou na mesma tabela!). por exemplo, na tabela de pedidos podemos ter uma chave estrangeira efetuando o relacionamento com a chave primária na tabela de clientes.
