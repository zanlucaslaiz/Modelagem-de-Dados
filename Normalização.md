# Normalização 

Normalização consiste em um processo de análise de uma relação para assegurar que seja bem formada.

Decompor relações com anomalias para produzir relações menores e bem-estruturadas, ou seja, em uma relação normalizada podemos inserir, excluir ou modificar registros sem criar anomalias.

O processo de normalização, proposto por Codd em 1972, aplica a um esquema de relação uma série de testes para certificar que ele satisfaça uma Forma Normal (FN).

Codd propôs originalmente 3 formas normais (1ªFN, 2ªFN, 3ªFN), posteriormente a 3FN foi revisada e uma definição mais robusta for proposta por Boyce e Codd, denominada Forma Normal de Boyce Codd (FNBC).

## Objetivos da Normalização

Analisar esquemas de relação (tabelas) com base em suas dependências funcionais e chaves primárias para: 
1. Minimizar redundâncias.
2. Minimizar anomalias de inserção, exclusão e modificação.

As relações são decompostas em esquemas de relações menores que atendem aos testes de forma normal.

O ideal é que o projeto do banco de dados relacional alcance a FNBC ou a 3FN para cada tabela.

Não é adequado normalizar apenas até a 1FN ou à
2FN, pois na verdade essas formas normais são usadas para se chegar à 3FN ou FNBC.

## Primeira Forma Normal

Definida historicamente para reprovar atributos multivalorados, compostos e suas combinações.

O domínio de um atributo deve incluir apenas valores atômicos (indivisíveis), e o valor de qualquer atributo em uma tupla deve ser único valor do domínio desse atributo.

Uma tabela está na 1ª forma normal quando:
* Somente possui valores atômicos;
* Não há grupos de atributos repetidos (há apenas um dado por coluna nas linhas);
* Existe uma chave primária;
* Relação não possui atributos multivalorados ou relações aninhadas.

Exemplo: um campo de Endereço possui subdomínios Rua, Número e CEP. Esses itens devem ser separados no processo de normalização. Cada informação deve ser colocada em um campo diferente.

### Dados Atômicos

* Elementos de dados que representam o nível mais baixo de detalhamento.
* Então, campos não-atômicos são aqueles que podem ser subdivididos em mais de um campo, pois eles escondem detalhes, como por exemplo o nome de uma pessoa, que contém o primeiro nome e o sobrenome.

## Segunda Forma Normal

Baseada no conceito de Dependência Funcional Total.
Um esquema de relação R está na 2FN se cada atributo não-chave de R for total e funcionalmente dependente da chave primária de R.
Para Testar a 2FN, testamos as dependências funcionais cujo atributos fazem parte da chave primária.
Caso a chave primária tenha um único atributo, esse teste não precisa ser aplicado.

### Tabela na 2ª FN

Uma tabela está na 2ª FN se:
* Está na 1ªFN;
* Todos os atributos não-chave são funcionalmente dependentes de todas as partes da chave primária;
* Não existem dependência parciais;
* Caso contrário, deve-se gerar uma nova tabela com os dados.
    * Deve-se criar uma nova relação para cada chave PK ou combinação de atributos que forem determinantes em uma dependência funcional.
    * Esse atributo será a PK na nova tabela.
    * Mova os atributos não-chaves dependentes desta PK para a nova tabela.

obs.: Um atributo-chave é um atributo que é uma PK ou parte de uma PK composta.

## Terceira forma normal

* Baseada no conceito de Dependência Transitiva.
* A relação não deve ter um atributo não-chave determinado funcionalmente por outro atributo não-chave (ou conjunto).
* Não deve haver dependência transitiva de um tributo não-chave sobre a PK.
* Deve-se decompor e montar uma nova relação que inclua os atributos não-chave que determinam funcionalmente outros atributos não-chave.

### Tabela na 3ª FN

Uma tabela está na 3FN se:
* Estiver na 2FN;
* Não existirem dependências transitivas.
* se nenhuma coluna não-chave depender de outra coluna não-chave.
    * Para cada atributo (ou grupo) não-chave que for uma determinante na relação, crie uma nova tabela.
    * Esse tributo será a PK na nova relação.
    * Mova então todos os atributos que são dependentes funcionalmente do atributo chave para a nova tabela.
    * O atributo (PK na nova relação) fica também na tabela original, e servirá como uma chave estrangeira para associar as duas relações.

obs.: Uma dependência transitiva em uma tabela é uma dependência funcional entre dois ou mais atributo não-chave.

## Passos da normalização

Tabela não-normalizada -> Remover atributos multivalorados e compostos (1FN) -> Remover dependências parciais (2FN)-> Remover dependência transitivas (3FN)


## Forma Normal de Boyce-Codd

A definição original de 3FN de Codd não lidava adequadamente como uma relação que:
* Tivesse duas ou mais chaves candidatas.
* Essas chaves candidatas fossem compostas.
* Elas tivessem superposição (atributos em comum).

Caso a combinação das condições acima não ocorra em uma tabela, basta aplicar a 3FN.

### Uma relação está em FNBC:

* Se e somente se os únicos determinantes são chaves candidatas.
* Cada relação na FNBC também está na 3FN, mas uma relação na 3FN não está necessariamente na FNBC (a maioria está).
* Na FNBC as chaves candidatas não possuem dependências parciais por outros atributos.
* Uma relação R está na FNBC sempre que uma dependência funcional não-trivial X -> A se mantiver em R, assim X é uma superchave de R.

### FNBC - Pontos a considerar

Determinante: "lado esquerdo" de uma DF, como o X em X -> Y (Y é "dependente"); X determina funcionalmente Y. 
Dependência Funcional Trivial: dependência que não pode deixar de ser satisfeita. Uma DF é trivial se o lado direito da expressão é um subconjunto do lado esquerdo. 
A -> B é uma DF trivial se B for um subconjunto de A.
Exemplo: {ID_Func, Nome_Func} -> ID_Func é uma DF trivial pelo ID_Func é um subconjunto de {ID_Func, Nome_Func}

### FNBC - Normalizando

Para normalizar uma tabela até a FNBC devemos decompor a tabela com os passos a seguir:
* Encontrar uma dependência funcional não-trivial X -> Y que viole a condição de FNBC. X não deve ser uma superchave.
* Dividir a tabela em duas: 
** Uma com os atributos XY, ou seja, todos os atributos da dependência.
** outra com os atributos X juntamente com os atributos restantes da tabela original.
