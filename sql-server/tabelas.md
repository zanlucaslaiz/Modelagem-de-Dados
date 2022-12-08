# ALTERAR TABELAS 

É possível alterar a estrutura de uma tabela após ter sido criada, acrescentando ou excluindo atributos(campos)

| Comando     | Descrição                                           |
|-------------|-----------------------------------------------------|
| ALTER TABLE | Para alterar a tabela                               |
| DROP        | excluir uma coluna                                  |
| ADD         | adicionar coluna                                    |
| ADD PRIMARY KEY | Adicionar uma chave primária |

Estrutura:

    ALTER TABLE nome_da_tabela
    DROP COLUMN nome_da_coluna 
 
Pode-se excluir uma constraint:

    ALTER TABLE nome_da_tabela
    DROP CONSTRAINT nome_CONSTRAINT
 
Podemos adicionar uma coluna:

    exemplo ALTER TABLE tbl_livro
    ADD id_autor SMALLINT NOT NULL
    CONSTRAINT fk_id_autor FOREIGN KEY (id_autor)
    REFERENCES tbl_autores
 
Alterar uma coluna:

    ALTER TABLE tbl_livro
    ALTER COLUMN id_autor SMALLINT
 
Adicionar uma chave primária:

    ALTER TABLE cliente
    ADD PRIMARY KEY (id_cliente)

* obs. A coluna id_cliente deve existir antes de ser transformada em chave primária.
A coluna id_cliente receber a a constraint "PRIMARY KEY", e passará a ser a chave primária da tabela.

Excluir uma tabela:

    DROP TABLE tbl_livro

* caso a tabela tenha dados ao exclui-la perdemos todos.
* caso a tabela esteja ligada por algum relacionamento a outra tabela primeiro devemos excluir o relacionamento e depois excluir a tabela.
