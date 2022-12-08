# Selecionar

Consulta simples:

    SELECT coluna FROM tabela

Consultar todas as colunas:

    SELECT * FROM tabela

Consultar só um campo da coluna:

    SELECT nome_do_campo FROM coluna

Especificando colunas:

    SELECT coluna FROM tabela 

Selecionar itens e inserir em outra tabela:

    SELECT INTO

    SELECT colunas
    INTO nova_tabela
    FROM tabela_atual

* seleciona dados de uma ou mais tabelas e os insere em uma tabela diferente.
* pode ser usada para criar cópias de backup de tabelas.

Apresentando valores diferentes:

    SELECT DISTINCT

    SELECT DISTINCT colunas
    FROM tabela

* é usado para apresentar valores diferentes.
* algumas colunas podem conter valores duplicados. para exibir apenas valores diferentes, use a palavra-chave DISTINCT:

Especificando o número de registros:

    SELECT TOP

    SELECT TOP numero|percentual colunas
    FROM tabela

* Usado para especificar o número de resgitros a retornar.
* útil para tabelas com muitos registros.

Alias - Alterar nome de uma tabela ou coluna na consulta:

    SELECT colunas
    AS nome_alias
    FROM tabela

* pode-se dar um nome diferente a uma coluna ou tabela em uma consulta.

Operador UNION:

    SELECT colunas FROM tabela1
    UNION 
    SELECT colunas FROM tabela2

* permite combinar duas ou mais declarações SELECT.
* Cada declaração SELECT deve ter o mesmo número de colunas, tipos de dados e ordem das colunas.

Operadores lógicos:
    
    AND e OR

* Usados para filtrar registros baseados em mais de uma condição.
* O operador AND mostra um registro se ambas as condições forem verdadeiras.
* o operador OR mostra um registro se pelo menos uma das condições for verdadeira.

Ordenar o conjunto:

    SELECT * FROM tabela
    ORDER BY nome_da_coluna ASC

* A palavra-chave ORDER BY é usada para ordenar o conjunto conjunto-resultado de registros.
* ASC - Ordem ascendente
* DESC - Ordem descendente (inversa)

Cláusula WHERE:

    SELECT colunas FROM tabela WHERE coluna = valor 

* Permite filtrar registros em uma consulta.

Comando UPDATE:

    UPDATE tabela
    SET coluna = valor
    WHERE "filtro"

* Atualizar registro dentro de uma tabela.

Atualizar mais de uma tabela:

    UPDATE tabela
    SET coluna = valor, coluna = valor
    WHERE "filtro"

* Clausura WHERE específica o dado a ser alterado. Caso esqueça de usá-la todos os dados serão alterado. E isso pode gerar um problema enorme.
