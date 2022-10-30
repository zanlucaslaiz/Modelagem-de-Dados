# Modelos de Banco de dados

## Modelo Hierárquico
* Neste modelo os dados são organizados de forma hierárquica, com conjuntos de tipos de registros interconectados por meio de ligações.
* Uma ligação representa uma relação entre dois tipos de registros: pai e filho.
* Um esquema no modelo hierárquico é um diagrama de estrutura em árvore.
* O acesso aos dados é sempre unidirecional, a partir do pai ao filho.

## Modelo em Rede
* No modelo em redes os dados são organizados em tipos e ligações entre dois registros.
* Não há restrição hierárquica.
* Tanto o esquema quanto ocorrência de dados são visualizados como um grafo direcionado.

## Modelo Relacional
* Os princípios do modelo relacional foram esboçados por E.F. Codd (IBM) em um artigo publicado em junho de 1970, intitulado "A rational model of data for large shared data banks", no qual o Dr. Codd propôs o modelo relacional para sistemas de bancos de dados.
* Antes disso eram usados modelos como o hierárquico e o modelo em rede.
* Neste modelo os dados são separados em entidades, conforme cada assunto, e registrados como atributos dessas entidades.
* As entidades se relacionam entre si e permitem que os dados sejam armazenados e recuperados de forma rápida e segura.
* No modelo relacional os dados são organizados em coleções de tabelas bidimensionais.
* Essas tabelas são também chamadas de "relações".
* Relação é uma forma de se organizar os dados em linhas e colunas.
* Baseados em lógica e teoria de conjuntos.

### Componentes do modelo relacional

O modelo relacional é composto, basicamente, por: 
* Coleções de objetos ou relações que armazenam os dados.
* Um conjunto de operadores que agem nas relações, produzindo outras relações.
* Integridade de dados, para precisão e consistência.

## Orientado a objeto

Bancos de Dados Orientados a Objetos (BDOOs) podem ser utilizados como alternativa aos Bancos de Dados Relacionais para armazenar objetos compartilhados entre diferentes aplicações.

Partem de uma premissa simples: o que se persiste são os objetos e, portanto, o seu “estado”, representado pelos atributos. Os atributos seriam equivalentes aos campos – ou colunas – de uma tabela. Já as associações entre objetos (atributos que referenciam outros objetos) podem ser comparadas aos relacionamentos em SGBDRs, criados como restrições de integridade referencial (“chaves estrangeiras”). Assim, o correspondente a uma “tabela-filha” em um BDOO seria um atributo que tenha como valor outro objeto.

## Não-relacional

Um banco de dados não relacional é um banco de dados que não usa o esquema de tabela de linhas e colunas encontrado na maioria dos sistemas de banco de dados tradicionais. Em vez disso, os bancos de dados não relacionais usam um modelo de armazenamento otimizado para os requisitos específicos do tipo de dados que está sendo armazenado. Por exemplo, os dados podem ser armazenados como pares chave/valor simples, como documentos JSON ou como um gráfico que consiste em bordas e vértices.
