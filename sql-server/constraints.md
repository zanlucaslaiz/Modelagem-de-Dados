# SQL constraints (restrições)

* Restrições são regras aplicadas nas colunas de uma tabela.
* São usados para imitar os tipos de dados que são inseridos.
* Podem ser especificadas no momento de criação da tabela (CREATE) ou após a tabela der sido criada (ALTER)

Principais:

- NOT NULL
- UNIQUE
- PRIMARY KEY
- FOREIGN KEY
- CHECK
- DEFAULT

### UNIQUE 

* A restrição UNIQUE identifica de forma única cada registro em uma tabela de um banco de dados.
* As constraints UNIQUE e PRIMARY KEY garantem a unicidade em uma coluna ou conjunto de colunas.
* Uma constraint PRIMARY KEY automaticamente possui uma restrição UNIQUE definida.
* Você pode ter várias contraints UNIQUE em uma tabela, mas apenas uma Chave primária por tabela.

### NOT NULL
* A constraint NOT NULL impõe a uma coluna a NÃO aceitar valores NULL.
* A contraint NOT NULL obriga um campo a sempre possuir um valor.
* Deste modo, não é possível inserir um registro (ou atualizar) sem entrar com um valor neste campo.

### PRIMARY KEY

* A PRIMARY KEY  identifica de forma única cada registro em uma tabela de banco de dados.
* Chaves primarias devem conter valores únicos.
* Uma coluna de chave primária não pode conter valores NULL
* cada tabela deve ter uma chave primaria e apenas uma.

### FOREIGN KEY 

* uma FOREIGN KEY (chave estrangeira) em um tabela é uma campo que aponta para uma chave primária em outra tabela.

Exemplo:
CONSTRAINT fk_ID_autor FOREIGN KEY (ID_Autor) 
REFERENCES tbl_autores(ID_Autor)

Neste exemplo a chave primaria esta na tabela tbl_autores e uma chave estrangeira de nome ID_Autor foi criada na tabela atual, usando o nome fk_ID_Autor

### CHECK 

* A constraint CHECK é usada para limitar uma faixa de valores que podem ser colocados em uma coluna.
* Se uma constraint CHECK for definida em uma única coluna ela permitirá apensa determinados valores para a coluna.
* Se a constraint CHECK for definida para a tabela, ela poderá limitar os valores em algumas colunas com base nos valores de outras colunas do registro.


### DEFAULT

* A restrição DEFAULT é usada para inserir um valor padrão em uma coluna.
* O valor padrão será adicionado a todos os novos registros caso nenhum outro valor seja especificado.

### AUTO INCREMENT (IDENTITY)

* O auto incremento permite que um número único seja gerado quando um novo registro é inserido em uma tabela.
* em SQL SERVER trata-se da palavra chave IDENTITY (identidade), cujo valor inicial padrão é 1, e se incrementa em 1.
* para que o valor de IDENTITY inicie em 100 e se incremente de 2 em 2, use IDENTITY(100,2).
* ao inserir valores na tabela, não é necessário especificar o valor para a coluna de autoincremento.
* não é possível alterar uma coluna existente para configurar IDENTITY.
* se necessário, crie uma nova tabela com IDENTITY e exclua a atual.
* só é permitido usar uma coluna de identidade por tabela.
