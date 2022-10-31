# CHAVES

Uma Chave consiste em uma ou mais colunas de uma relação cujos valores são usados para identificar de forma exclusiva uma linha ou conjunto de linha.
Pode ser única (identifica uma única linha) ou não-única (identifica um conjunto de linhas).

* Únicas (Unique) - Candidata, Composta, Primária, Surrogada
* Não-única (Non-Unique) – Estrangeira

## Chave Candidata
* Atributo ou grupo de atributos com o potencial para se tornarem uma chave primária.
* Uma chave candidata que não seja usada como chave primária será conhecida como Chave Alternativa.
Ex.: Campos Num_Matrícula e CPF em uma tabela de registro de alunos.

## Chave Primária
* Chave candidata escolhida para ser a chave principal na relação.
* Identifica de forma exclusiva os registros em uma tabela, não podendo ter repetição de valores nem tampouco valor nulo.
* Primary Key / PK

## Chave Estrangeira
* Coluna de uma tabela que estabelece um Relacionamento com a chave primária (PK) de outra tabela.
* É a partir de chave estrangeira que sabemos com qual registro em outra tabela um registro está relacionado.
* chave estrangeira - Foreign key (FK)

## Chave Composta

* Chave que é composta de dois ou mais atributos (colunas).
* Geralmente empregada quando não é possível utilizar uma única coluna de uma tabela para identificar de forma exclusiva seus registros.

## Chave Surrogada / Substituta

* Valor numérico, único, adicionado a uma relação para servir como chave primária.
* Não possui significado para os usuários e geralmente fica escondida nas aplicações.
* As chaves substitutas são frequentemente usadas no lugar de uma chave primária composta.

# Instruções para criação de chaves primárias e estrangeiras

* Não é possível haver valores duplicados em uma chave primária.
* No geral, não é possível alterar o valor de uma chave primária.
* Chaves estrangeiras são baseadas em valores de dados, classificadas como ponteiros lógicos.
* Um valor de uma chave estrangeira deve corresponder a um valor existente em uma chave primária associada (ou valor de chave única). Caso contrário, deve ser nulo (NULL).
* Uma chave estrangeira deve referenciar uma chave primária ou uma coluna de chave única.

## O conceito de Domínio

* Definir tipos de dados.
* Especificar valores válidos em um campo.

Exemplo: Campo (CPF_Cliente); 
Tipo de Dados (caractere);
Tamanho (11 caracteres).