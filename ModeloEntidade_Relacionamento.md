# Modelo Entidade-Relacionamento

Também conhecido pela sigla MER, trata-se de um modelo conceitual usado para descrever objetos envolvido no domínio de um sistema a ser construído, incluindo seus atributos e relacionamentos.

MER, cria um diagrama entidade-relacionamento a partir das especificações do negócio ou narrativas do usuário. Permite ilustrar as entidades em um negócio e também relacionamentos entre elas. 

Construímos o MER durante a fase de análise no ciclo de vida de desenvolvimento do sistema.

Um MER separa a informação necessária ao negócio das atividades que são realizadas no negócio.

Após o levantamento dos requisitos, estes são transformados em um Modelo Entidade-Relacionamento(MER), o qual consiste dos seguintes elementos:

* Entidades - algo significativo, sobre o qual devemos possuir informações. como exemplos, temos clientes, funcionários, pedidos e produtos.
* Relacionamentos - trata-se de uma associação nomeada entre entidades, com um grau de associação. Por exemplo, clientes podem estar associados a pedidos.
* Atributos - Algo que descreve au qualifica uma entidade. Por exemplo, a entidade cliente possui atributos que descrevem seu nome, endereço, telefone, número de identificação, entre outros. Atributos podem ser obrigatórios ou opcionais.

O modelo é posteriormente refinado com o uso de técnicas especificas, e finalmente implementado em um banco de dados físico.

## COMPONENTES DO MER
 
 ### ENTIDADES 

* Algo de importância para um usuário ou organização que precisa ser representado em um banco de dados.
* Representa um tema, tópico ou conceito de negócio.
* Cada objeto de uma entidade é denominado de Instância de Entidade.
* Uma entidade pode ter existência física ou abstrata. Ex: Empregados, Livros, Vendas, produtos.
* Nomeamos as entidades usando substantivos que representam de forma clara e objetiva sua função. Por exemplo, podemos ter em um sistema as entidades PRODUTO, CLIENTE, VENDA, ESTOQUE, CATALOGO, entre outras.
* uma entidade em si é uma descrição da estrutura e formato das ocorrências da entidade, como um a "receita", ou "planta".
* uma instância de entidade é uma ocorrência especifica de uma entidade.

Representamos as entidades em um der por meio do retângulos contendo o nome da entidade.

### Algumas regras de nomeação

* nomes de entidades:
    * devem começar com um letra;
    * usar palavra no singular;
    * não podem ter espaços ou alguns caracteres especiais;
    * alguns caracteres como "$", "#" e "_" são permitidos em alguns banco de dados.
* os nomes de colunas devem ser únicos dentro de uma tabela.
* os nomes de entidades / tabelas devem ser únicos dentro do esquema.


### ATRIBUTOS 

* Os atributos descrevem características da entidade, como por exemplo: fabricante, modelo, cor. placa, etc.
* Os atributos possuem um tipo de dados(domínio) nome e valor especifico.

* Os atributos podem ser representados por uma elipse contendo o seu nome, ligada a entidade que qualifica.
* Opcionalmente, podemos representar um atributo apenas pelo seu nome ligado a entidade, sem utilizar a elipse.

### Tipos de Atributos

* Simples - não possui características especiais, e são indivisíveis. Ex.: CPF, CNPJ, nome da empresa.

* Composto - é formado por itens menores; pode ser subdividido em outros atributos. ex.: endereço da empresa (rua, cep, bairro) 
via de regra tem que desmembrar em atributos simples. isso vai ajudar em uma futura busca.

* Multivalorado - pode conter mais de valor para um mesmo registro (informação). ex.: telefone da empresa. colocar um * antes do nome multivalorado.

* determinante - define de forma única as instâncias de uma entidade. não podem existir duas instâncias com o mesmo valor nesse atributo. ex.: CNPJ da empresa, código de produto. 'colocar um sublinhado.'

* Identificador (chave)- uma chave identifica uma instância especifica na classe de entidade. ex.: CPF, codigoProduto, Matricula, ID_Setor 
    As chaves podem ser únicas ou não-únicas:
	* únicas: o valor dos dados da chave é único na entidade.
	* Não-única: usada para agrupar instancias de classe em categorias.
	As chaves podem ser compostas, consistindo de dois ou mais atributos combinados.


### RELAÇÃO

Tabela bidimensional com características especificas, compostas por linhas e colunas, criada a partir de uma entidade.
"toda relação é uma tabela, mas nem toda tabela é uma relação."

### Características de uma relação:

* Registros - linhas contém dados sobre instâncias de uma entidade;
* Campos - colunas contém dados sobre atributos da entidade;
* Domínio - Todos os valores em uma coluna são do mesmo tipo;
* Cada célula da tabela armazena um único valor;
* Cada coluna possui um nome único;
* Não há duas linhas idênticas;
* As relações geralmente geram tabelas no banco;

### ENTIDADE x RELAÇÃO

* Uma entidade é um conceito do mundo real, como por exemplo um cliente ou um produto;
* Uma relação é um conjunto de registros (tuplas) que representam um modelo de uma entidade;
* Cada registro representa uma instância de entidade, e o conjunto de todas as instâncias, com seus atributos, é chamado de relação.

### RELACIONAMENTO 

As Entidades podem ser conectadas entre si por meio de Relacionamentos. Trata-se de uma estrutura que indica a associação de elementos de uma ou mais entidades.

### Porque precisamos de relacionamento?

Como os dados de diferentes entidades são armazenados em tabelas distintas, geralmente precisamos combinar duas ou mais tabelas para responder as perguntas especificas dos usuários.

Por exemplo, podemos querer saber quais produtos, e em qual quantidade, foram adquiridos por um cliente em particular. Precisaremos então de dados das tabelas de clientes, de pedidos e produtos para obter essa informação.

Representamos relacionamentos por meio de um losango que conecta uma ou mais entidades.

### Grau de um relacionamento

O grau de um relacionamento define o número de entidades que participam do relacionamento. Assim, um relacionamento pode ser: 
* Unário (recursivo ou autorrelacionamento);
* Binário;
* Ternário.

Os relacionamentos mais comuns são os de grau (binários)

### EFETUANDO relacionamentos entre múltiplas tabelas

* Cada linha de dados em uma tabela deve ser identificada de forma única usando-se uma Chave Primaria (identificador exclusivo)
* Usamos uma chave estrangeira para relacionar os dados entre múltiplas tabelas.
* Usamos para isso o relacionamento entre chave primaria de uma tabela com a chave estrangeria em outra tabela.



### Abreviações

* MER: Lista de entidades, Atributos e relacionamentos, que traz informações sobre tipos de dados, restrições descrições de entidades e outras.
* DER: representação gráfica associada ao MER (ou parte dele).



