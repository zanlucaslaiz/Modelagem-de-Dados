# 12 dicas de boas práticas:

## 01) Nomes de objetos

Use apenas nomes significativos para os objetos do banco, como tabelas, colunas e procedimentos armazenados.
Os nomes devem ser descritivos. Evite abreviações e siglas obscuras que possam atrapalhar a compreensão da finalidade do objeto.

## 02) Tipos corretos de dados

Usar os menores valores possíveis
A performance do banco é melhorada se usarmos os menores valores possíveis para os dados que os requisitos permitem.

## 03) Normalizar as tabelas

A normalização de doas é um princípio base dos bancos de dados relacionais, no qual os dados são organizados para minimizar ou eliminar a redundância.
Normalizar até a 3ª forma normal.
Desnormalizar se necessário.

## 04) Usar e Nomear Constraints 

Ao nomear restrições, use prefixos que as descrevam, como por exemplo "PK" para chave primaria ou "FK" para chave estrangeira, seguidos do nome da tabela (ou tabelas) envolvidas.

## 05) Identificação dos elementos do MER

Identifique os elementos de um modelo de entidade relacionamento no seguinte ordem:
1 - Entidade primeiro
2 - Relacionamentos na sequência
3 - Atributos de entidades por último
4 - Atributos de relacionamentos, se houver

## 06) Tabelas Associativas

Prestar sempre muita atenção em relacionamentos muito-para-muitos (N:M)
Sempre que um relacionamento desse tipo ocorrer, simplificá-lo criando uma tabela associativa.

## 07) Relacionamentos n-ários

Também prestar sempre muita atenção quando surgirem relacionamentos n-ários, como ternários ou quaternários.
Sempre que um relacionamento desse tipo ocorrer, simplificá-lo criando tabelas associativas.

## 08) Documentação

Documentar o processo de modelagem é de crucial importância.
* Criar o DER detalhado.
* Criar Dicionário de Dados.
* Na codificação, usar comentários para descrever os scripts.

## 09) Prefixos de nomes de objetos

Prefixar nomes de objetos para identificar sua categoria:
* tb ou tbl para tabela
* vw para view
* db para banco de dados
* sp para procedimento armazenado
* tg para trigger
etc

## 10) Nomes de tabelas e Colunas Use termos no singular para nomes de tabelas - por exemplo, tblCliente em vez tblClientes, pois uma tabela representa uma coleção de entidades.
Idem para colunas - NomeLivro em vez de NomesLivros.

Procure não usar acentuação, espaços e caracteres especiais.

## 11) Levantamento e Análise de Requisitos

Extremamente importante. Saiba levantar todas as informações necessárias para iniciar o processo de modelagem.
Pergunte o máximo que puder, e anote toda informação fornecida pelo cliente / usuário. Interação sempre!
Na dúvida sobre a regra de negócio, contate o cliente e pergunte de novo.

## 12) Campos de chave primaria

* Tabelas sempre devem possuir uma chave primária
* Procure usar chaves naturais, sempre que possível
* Entre uma chave composta ou surrogada, prefira esta última
* Procure usar tipos numéricos em vez de caractere, para economizar recursos e aumentar a performance de busca.
