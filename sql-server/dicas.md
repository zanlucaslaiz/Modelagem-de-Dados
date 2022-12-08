# Dicas 

Dicas relacionadas á programação do banco de dados usando a linguagem de consulta estruturada SQL

## 1 - Usar views

Procure usar views para ocultar complexidade, fornecer dados agregados e restringir o acesso a linhas de colunas das tabelas.

## 2 - Select *
Evite realizar consultas retornando todas as colunas de uma tabela (Select *) a não ser que sejam realmente necessárias.

O ideal é sempre retornar apenas as colunas necessárias (select [colunas]) para obter melhor performance
 
## 3 - Campos de Senha

Senha sempre devem ser guardadas criptografadas - de preferência usando algoritmos fortes e salt.
A decriptação deve ocorrer na aplicação, quando for necessário.

## 4 - Sempre utilizar procedures e views
* Aumentam a performance em consultas
* Diminuem possibilidade de erros
* Simplificam codificação da aplicação

## 5 - Usar índices em colunas muito consultadas

Índices podem aumentar significativamente a performance de acesso em consultas, casos colunas seja muito frequentemente acessada.
Crie índices sempre que detectar essa necessidade - mas cuidado com colunas que são modificadas com frequência.


