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
