# Níveis da modelagem de dados

O processo de modelagem de dados é classificado em três níveis:

 * Modelo conceitual (alto nivel) - MCD
 * Modelo lógico - MLD
 * Modelo físico (baixo nivel) – MFD

## MODELO CONCEITUAL

Está é a primeira fase da modelagem, onde representaremos o mundo real por meio de uma visão simplificada dos dados e seus relacionamentos. Assim poderemos determinar quais informações serão armazenadas de banco de dados.
Neste nível o projeto é independente de SGBD.

Exemplo: 
Cadastro de produtos em uma loja
Dados necessários: Nome do produto, categoria de produto (limpeza, higiene, etc), código do fornecedor, tipo de embalagem, tamanho, quantidade.

Neste nível, detalhes da implementação não aparecem, porém é suficientemente detalhado para a ponto de ser possível descrever os tipos de dados requeridos, seus relacionamentos entre si e regras de consistência.

## MODELO LÓGICO

Aquele em que os objetos, suas características e relacionamentos têm a representação de acordo com as regras de implementação e limitações impostas por algum tipo de tecnologia. Essa representação é independente dos dispositivos ou meios de armazenamento físico das estruturas de dados por elas definidas. Modelo relacionado ao projeto de banco de dados.

Um modelo lógico possui conceitos que os usuários são capazes de entender, ao mesmo tempo em que não está distante do modelo físico de banco de dados.

Neste nível o projeto é independente do SGBD.

Consiste na especificação lógica dos dados em um formato adequado ao SGBD escolhido. Os tipos de dados são completamente definidos.

## MODELO FISICO

A partir de um modelo lógico nós derivamos o modelo físico, onde se detalham os componentes de estrutura física do banco de dados, incluindo as tabelas, campos, tipos de valores, restrições, etc.

É a representação dos objetos feita sob o foco do nível físico de implementação das ocorrências, ou instâncias das entidades e seus relacionamentos. O conhecimento do modo físico de implementação das estruturas de dados é ponto básico para o domínio desse tipo de modelo. Depende especificamente de cada SGBD.