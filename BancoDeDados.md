# CONCEITOS IMPORTANTES

## DADOS X INFORMAÇÃO

DADOS - são fatos em uma forma primária, que podem ser armazenados em algum meio.
Ex.: CPF, Nome, Data

INFORMAÇÃO - são os fatos organizados de maneira a produzir um significado -> Dados colocados em contexto. 
Ex.: lista de clientes com seus números de CPF, ORDENADOS.

## METADADOS
* Definimos metadados como sendo "Dados sobre os dados".
* Permitem efetuar a representação e identificação dos dados. garantindo sua consistência e persistência.
* Os Metadados são mantidos no Dicionário de Dados (ou em um Catálogo de Dados).

## BANCO DE DADOS

* Um banco de dados (BD) é uma coleção organizada de dados. Esses dados são organizados de modo a modelar aspectos do mundo real, para que seja possível efetuar processamento que gere informações relevantes para os usuários a partir desses dados.
* Um BD é composto por diversos objetos, tais como: Tabelas, esquemas, visões, consultas, relatórios, procedimentos, triggers, entre outros.

## APLICAÇÕES DE BANCO DE DADOS

Bancos de dados encontram aplicações em inúmeras áreas, como:
* Sistemas bancários;
* Reservas em hotéis;
* Controle de estoque em supermercados;
* Catálogo de livros em bibliotecas;
* E-commerce;
* Receita federal;
* YouTube;

## SGBD - Sistema de gerenciamento de banco de dados 
* Um SGBD é uma coleção de softwares que permite aos usuários criarem e manterem um ou mais bancos de dados.
* São usados nas tarefas de definição, construção, manipulação e compartilhamento dos bancos de dados entre aplicações e usuários.
* Permitem proteger o banco de dados e mantê-lo ao longe de tempo.

EXEMPLOS:
* oracle Database - https://www.oracle.com/database/
* microsoft SQL server - https://www.microsoft.com/pt-br/sql-server/
* mySQL - https://www.mysql.com/
* IBM DB2 - https://www.ibm.com/products/db2
* SAP Sybase - https://www.sap.com/brazil/products/technology-platform/sybase-ase.html
* MongoDB - https://www.mongodb.com/
* Teradata - https://www.teradata.com/
* PostgreSQL - https://www.postgresql.org/
* SQLite - https://www.sqlite.org/index.html

## SISTEMA DE BANCO DE DADOS

É um sistema que relaciona os usuários --> aplicativos --> SGBD --> banco de dados

## USUARIOS DE BANCO DE DADOS
* Administrador (DBA)
* Projetista / desenvolvedor
* Usuário final

## CARACTERISTIAS E FUNCIONALIDADES
* Controle de redundância --> evitar duplicidade
* Múltiplas visões dos dados --> exibições diferentes
* Controle de concorrência --> gerenciar o acesso
* Backup e restauração
* Autenticação e autorização de acesso
* Restrições de integridade --> garantir a autenticidade dos dados.


## MODELOS

* Um modelo é uma estrutura que ajuda a comunicar os conceitos que estão na mente do projetista. Podemos usá-los para tarefas como descrever, analisar, especificar e comunicar ideias.
* O modelo deve possuir detalhes suficientes para que um desenvolvedor consiga construir o banco de dados de acordo com a necessidade do projeto.

MODELAGEM DE DADOS

* Modelagem de dados é o processo de criação de um Modelo de Dados para um sistema de informação, com a aplicação de técnicas especificas de modelagem.
* Trata-se de processos para definir a analisar requisitos de dados necessários para suportar processos de negócio com sistemas informatizados em organizações.
* Um modelo de dados fornece uma estrutura para os dados usados em um Sistema de Informação, com definições e formatos específicos.

## IDENTIFICADOR UNICO (UID)

* Um identificador unico é qualquer combinação de atributos ou relacionamentos que são usados para distinguir ocorrências de uma entidade. cada ocorrência da entidade deve ser identificavel de forma exclusiva.

## MODELAGEM DE DADOS - NIVEIS

Classificamos o processo de modelagem de dados em três níveis:
* modelo conceitual (alto nivel) - MCD
* modelo lógico - MLD
* modelo físico (baixo nivel) – MFD

## ARQUITETURA DE TRÊS NIVEIS

Mundo observado ---> modelo conceitual -> modelo ógico -> modelo fisico

## ESQUEMA DE BANCO DE DADOS

* Um esquema é uma definição do banco de dados especificada durante o projeto, armazenada no Dicionário de dados. 
* Um esquema (Schema) raramente muda durante a vida do  banco de dados
* Trata-se da organização dos dados em um plano que mostra como o banco é construido. 
* O esquema define tabelas, campos, relacionamentos, visões, funções e muitos outros elementos que comp~em o banco de dados.

## ETAPAS DO DESENVOLVIMENTO DE UM BANCO DE DADOS
1. Especificação e analise de requisitos 
	* Os requisitos são documentados
2. Projeto conceitual
	* Baseado nos requisitos
3. Projeto lógico
	* Expresso em um modelo de dados, como o relacional 
4. Projeto fisico
	* Especificações para armezenar e acessar o banco de dados
	* Implementação do banco de dados, inserção de dados reais e manutenção.

## TAREFAS PARA MODELAGEM

As tarefas a seguir devem ser realizadas para que seja possivel efetuar modelagem de dados e projetos de banco de dados funcional:
* Identificar os tipo de entidade;
* Identificar atributos;
* Identificar relacionamentos;
* Criar e associar chaves;
* Normalizar para reduzir redundância;
* Desnormalizar para aumentar performasse;

## Dicionário de Dados

Um dicionário de dados é um documento usado para armazenar informações sobre o conteúdo, formato e a estrutura de um banco de dados, assim como os relacionamentos entre os seus elementos.
É importante manter um dicionário de dados para limitar erros ao criar a estrutura física do banco de dados no computador.
Também chamado de "Repositório de metadados".



