# Integridade de dados 

Manutenção e garantia da consistência e precisão dos dados, sendo um aspecto crítico no design, implementação e uso de sistemas de armazenamento de dados.
A integridade é atingida por meio da aplicação de Restrições de Integridade.

# Restrições de Integridade

Cinco principais:
* Integridade Referencial; 
* Integridade de Domínio;
* Integridade de Vazio;
* Integridade de Chave;
* Integridade Definida pelo Usuário.

## Integridade de Domínio

Valores inseridos em uma coluna devem sempre obedecer a definição dos valores que são permitidos para essa coluna - os valores do domínio. Ex.: em uma coluna que armazena preços de mercadorias, os valores admitidos são do domínio numérico - ou seja, apenas números.

### Fatores 
* Tipo de Dados do campo
* Representação interna do tipo de dado
* Presença ou não do dado
* Intervalos de valores no domínio
* Conjuntos de valores discretos

## Integridade Referencial

Uma restrição de Integridade Referencial assegura que valores de uma coluna em uma tabela são válidos baseados nos valores em uma outra tabela relacionada. ex.: Se um produto de ID 523 foi cadastrado em uma tabela de Vendas, então um produto com ID 523 deve existir na tabela de Produtos relacionada.

### Atualização e Exclusão de Dados

Se um registro for excluído em uma tabela, então os registros relacionados em outras tabelas que o referenciam talvez precisem ser excluídos.
Caso contrário ocorrerá erro.
O mesmo se dá com atualização de registros.

## Integridade de Vazio

Este tipo de integridade informa se a coluna é obrigatória ou opcional - ou seja, se é possível não inserir um valor na coluna.
Uma coluna de chave primária, por exemplo, sempre deve ter dados inseridos, e nunca pode estar vazia, para nenhum registro.

### Valores Nulos (NULL)

Um valor NULL significa que não existem dados.
É diferente de zero, espaço, string vazia ou tabulação.
Os nulos podem ser problemáticos, pois indicam:
* O valor da coluna não é apropriado;
* O valor não foi inserido;
* O valor é desconhecido.

Ex.: Suponha uma tabela de cadastro de alunos.
Todo aluno deverá ter um nome cadastrado, de modo que esse campo é obrigatório (atributo não-nulo).
Nem todo aluno possui telefone, portanto esse campo não é obrigatório.

## Integridade de Chave

Os valores inseridos na coluna de chave primariam (PK) devem ser sempre únicos, não admitindo-se repetições nesses valores.
Desta forma, as tuplas (registros) serão sempre distintas.
Os valores de chave primária também não podem ser nulos.

## Integridade Definida pelo Usuário

Diz respeito a regras de negócio específicas que são definidas pelo usuário do banco de dados. Por exemplo, pode-se definir que uma coluna somente aceitará um conjunto restrito de valores.
