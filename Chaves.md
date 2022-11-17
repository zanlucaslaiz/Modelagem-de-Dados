# CHAVES

Uma Chave consiste em uma ou mais colunas de uma relação cujos valores são usados para identificar de forma exclusiva uma linha ou conjunto de linha.
Pode ser única (identifica uma única linha) ou não-única (identifica um conjunto de linhas).
Usadas para definir restrições de integridade no banco de dados.
Também usada para estabelecer relacionamentos entre tabelas no banco de dados.

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

## Chaves Naturais

* Chaves baseadas em valores encontrados no mundo real;
* Refletem como um objeto é identificado fora do sistema.
* Exemplos incluem: Números de documentos, placas de automóveis, endereços, coordenas geográficas, entre outros.


## Chave Surrogada / Substituta (Surrogate Key)

* Valor numérico, único, adicionado a uma tabela para servir como chave primária.
* Não possui significado para os usários e geralmente fica escondida nas aplicações.
* São frequentemente usadas no lugar de uma chave primária composta.
* Também conhecidas com chaves sintéticas ou Pseudo Chaves.

### Características

* Seu valor nunca é reutilizado;
* O valor é gerado pelo sistema;
* O valor não é manipulável pelo usuário ou aplicação;
* O valor não contém significado semântico;
* O valor não é visível para o usuário ou para a aplicação;
* O valor não é composto por mais de um valor de domínios diferentes.

### Vantagens de uma chave substituta

* Há a garantia de que valores não serão repetidos.
* Pode acelerar operações de junção entre tabelas (joins).
* Performance de BD é melhorada, pois geralmente os valores da chave são menores. Menos operações de E/S são requeridas ao acessar índices de colunas.
* Como não há lógica de negócio aplicada à chave, mudanças nas regras de negócios não a afetam.

### Desvantagens de uma chave substituta

* Seu valor não pode ser (normalmente) usado como chave de consulta.
* Por não ter relação semântica com o resto da tabela, viola a 3FN
* Ocupa espaço extra no banco e necessita de operações extras de E/S, por ser diferentes dependendo do sistema SGBD empregado.

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