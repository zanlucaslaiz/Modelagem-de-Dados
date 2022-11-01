# Dependências 

As dependências, em banco de dados relacionais, são restrições aplicadas sobre atributos, ou que definem a relação entre dois ou mais atributos em uma tabela. As dependências ocorrem quando uma coluna em uma tabela é determinada por outra coluna, ou seja, quando uma coluna depende de outra para fazer sentido.

## Dependência Funcional 

Seja E uma entidade, e X e Y dois atributos quaisquer de E.
Dizemos que Y é funcionalmente dependente de X se e somente se cada valor de X tiver associado a ele exatamente um valor de Y.

Ex.: O prazo de entrega de um pedido depende do número do pedido considerado:
Numero_Pedido  Prazo_Entrega_Pedido
O atributo que determina o valor é chamado de Determinante.
O outro atributo é chamado de Dependente.
Uma chave primária em uma relação determina funcionalmente todo os outros atributos não-chave na linha.
 
## Dependência Funcional Total

Em uma relação com uma PK composta, um atributo não-chave que dependa dessa PK como um todo, e não somente de parte dela, é dito como possuindo Dependência Funcional Total.
Obs.: A dependência funcional total só pode ocorrer em tabela com chave primária composta.

## Dependência Funcional Parcial

Uma dependência funcional é parcial quando os atributos não-chave não dependem funcionalmente de toda a PK quando esta for composta, ou seja, existe uma dependência funcional, mas somente de uma parte da chave primária.

## Dependência funcional transitiva

Este tipo de dependência ocorre quando uma campo não-chave não depende diretamente da chave primária da tabela (nem mesmo parcialmente), mas depende de uma outro campo não-chave na tabela.

## Dependência Multivalorada

Ocorre quando, para cada valor de um atributo A, existe um conjunto de valores para outros atributos B e C que estão associados a ele, mas que são independentes entre sí.

## Conclusão

Entender as dependências é fundamental durante a processo de modelagem de dados, pois, dependendo do tipo de dependência encontrada será necessário tomar determinadas decisões, como eliminar atributos, criar novas tabelas ou mover atributos entre tabelas, o que ficará bem evidente quando estudamos os processos de Normalização de Banco de Dados.
