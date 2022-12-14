# Dicionario de Dados

## Entidades


| Entidade     	| Relacionamento   	| Nome do Relacionamento 	| Descrição                                                               	|
|--------------	|------------------	|------------------------	|-------------------------------------------------------------------------	|
| Departamento 	| Professor        	| Pertence               	| Tabela para cadastro dos departamentos da faculdade                     	|
|              	| Disciplina       	| Responsável            	|                                                                         	|
|              	| Curso            	| Controla               	|                                                                         	|
|--------------	|------------------	|------------------------	|-------------------------------------------------------------------------	|
| Professor    	| Departamento     	| Pertence               	| Tabela para cadastro dos professores da faculdade                       	|
|              	| Prof_Disciplina  	| Leciona                	|                                                                         	|
|--------------	|------------------	|------------------------	|-------------------------------------------------------------------------	|
| Turma        	| Curso            	| Gera                   	| Tabela para registro de turmas em andamento e encerradas                	|
|              	| Aluno            	| Pertence               	|                                                                         	|
|--------------	|------------------	|------------------------	|-------------------------------------------------------------------------	|
| Curso        	| Departamento     	| Controla               	| Tabela para cadastro de cursos da faculdade                             	|
|              	| Curso_Disciplina 	| Possui                 	|                                                                         	|
|              	| Turma            	| Gera                   	|                                                                         	|
|              	| Aluno            	| Matriculado            	|                                                                         	|
|--------------	|------------------	|------------------------	|-------------------------------------------------------------------------	|
| Aluno        	| Curso            	| Matriculado            	| Tabela para cadastro dos alunos da faculdade                            	|
|              	| Turma            	| Pertence               	|                                                                         	|
|              	| ALuno_disc       	| Cursa                  	|                                                                         	|
|              	| Histórico        	| Pertence               	|                                                                         	|
|              	| Telefone_aluno  	| Possui                   	|                                                                         	|
|--------------	|------------------	|------------------------	|-------------------------------------------------------------------------	|
| Disciplina   	| Departamento     	| Responsável            	| Tabela para cadastro das disciplinas que compoe  os cursos da faculdade 	|
|              	| Aluno_disc      	| cursa                 	|                                                                         	|
|              	| Prof_Disciplina  	| É Lecionada            	|                                                                         	|
|              	| Disciplina       	| Depende                  	|                                                                         	|
|              	| Curso_Disciplina 	| Pertence               	|                                                                         	|
|              	| Disc_Histórico   	| Compoe                 	|                                                                         	|
|--------------	|------------------	|------------------------	|-------------------------------------------------------------------------	|
| Histórico    	| Aluno            	| Pertence               	| Tabela para geração de histórico de aluno                                	|
|              	| Disc_Histórico   	| É Composto             	|                                                                         	|

## Entidades Associativas

| Entidades        	| Relacionamento 	| Nome do Relacionamento 	| Descrição                                       	|
|------------------	|----------------	|------------------------	|-------------------------------------------------	|
| Disc_Histórico   	| Disciplina     	| Compoe                 	| Tabela Associativa entre Disciplina e Histórico 	|
|                  	| Histórico      	| É composto             	|                                                 	|
|------------------	|----------------	|------------------------	|-------------------------------------------------	|
| Curso_Disciplina 	| Curso          	| Possui                 	| Tabela Associativa entre Curso e Disciplina     	|
|                  	| Disciplina     	| Pertence               	|                                                 	|
|------------------	|----------------	|------------------------	|-------------------------------------------------	|
| Prof_Disciplina  	| Professor      	| Leciona                	| Tabela associativa entre Professor e Disciplina 	|
|                  	| Disciplina     	| É lecionada            	|                                                 	|
|------------------	|----------------	|------------------------	|-------------------------------------------------	|
| Aluno_Disc    	| Aluno         	| cursa                 	| Tabela associativa entre aluno e Disciplina 	    |
|                  	| Disciplina     	| É cursada              	|                                                 	|
|------------------	|----------------	|------------------------	|-------------------------------------------------	|
| Endereço_aluno  	| aluno           	| possui                	| Tabela para registro do endereço dos alunos   	|
|                  	| tipo_logradouro  	| É do tipo             	|                                                 	|
|------------------	|----------------	|------------------------	|-------------------------------------------------	|
| Tipo_logradouro  	| Endereço_aluno   	| compoe                 	| Tabela para regitro dos tipos de logradouro 	    |
|------------------	|----------------	|------------------------	|-------------------------------------------------	|
| Telefone_aluno  	| aluno           	| possui                	| Tabela para registro dos telefones dos alunos   	|
|                  	| tipo_telefone  	| pertence               	|                                                 	|
|------------------	|----------------	|------------------------	|-------------------------------------------------	|
| Tipo_telefone  	| Telefone_aluno   	| define                 	| Descrição dos tipos de telefone aceito    	    |

## Atributos - Departamento

| Atributo          	| Tipo de dados 	| Comprimento 	| Restrições   	| Descrição                               	|
|-------------------	|---------------	|-------------	|--------------	|-----------------------------------------	|
| Cod_Departamento  	| Inteiro       	| 2 bytes     	| PK. NOT NULL 	| Código de identificação do departamento 	|
| Nome_Departamento 	| Caractere     	| 20 bytes    	| NOT NULL     	| Nome do departamento                    	|

## Atributos - Professor

| Atributo            	| Tipo de dados 	| Comprimento 	| Restrições   	| Descrição                                       	|
|---------------------	|---------------	|-------------	|--------------	|-------------------------------------------------	|
| Cod_Professor       	| Inteiro       	| 2 bytes     	| PK. NOT NULL 	| Código de identificação do Professor            	|
| Nome_Professor      	| Caractere     	| 20 bytes    	| NOT NULL     	| Nome do Professor                               	|
| Sobrenome_Professor 	| Caractere     	| 50 bytes    	| NOT NULL     	| Sobrenome do professor                          	|
| Cod_Departamento    	| Inteiro       	| 2 bytes     	| FK. NOT NULL 	| Código de identificação do Departamento         	|
| Status              	| Booleano      	| 1 bit     	| NOT NULL     	| Status do professor (Lecionando/Não Lecionando) 	|

## Atributos - Turma

| Atributo    	| Tipo de dados 	| Comprimento 	| Restrições   	| Descrição                               	|
|-------------	|---------------	|-------------	|--------------	|-----------------------------------------	|
| Cod_Turma   	| Inteiro       	| 2 bytes     	| PK. NOT NULL 	| Código de identificação da turma        	|
| Cod_Curso   	| Inteiro       	| 2 bytes     	| FK. NOT NULL 	| Código de identificação do Curso        	|
| Período     	| Caractere     	| 5 bytes    	| NOT NULL     	| Período da turma (manhã, tarde, noite)  	|
| Num_Alunos  	| Inteiro       	| 2 bytes     	| NOT NULL     	| Números de alunos matriculados na turma 	|
| Data_inicio 	| Data          	| 4 bytes     	| NOT NULL     	| Data de inicio do turma                 	|
| Data_Fim    	| Data          	| 4 bytes     	| NOT NULL     	| Date de fim da turma                    	|

## Atributos - Curso

| Atributo         	| Tipo de dados 	| Comprimento 	| Restrições   	| Descrição                               	|
|------------------	|---------------	|-------------	|--------------	|-----------------------------------------	|
| Cod_Curso        	| Inteiro       	| 2 bytes     	| PK. NOT NULL 	| Código de Identificação do curso        	|
| Nome_Curso       	| Caractere     	| 40 bytes    	| NOT NULL     	| Nome do curso                           	|
| Cod_Departamento 	| Inteiro       	| 2 bytes     	| FK. NOT NULL 	| Código de Identificação do Departamento 	|

## Atributos - Aluno

| Atributo        | Tipo de dados | Comprimento | Restrições      | Descrição                                             |
|-----------------|---------------|-------------|--------------   |-------------------------------------------------------|
| RA              | Caractere     | 8 bytes     | PK. NOT NULL    | Código de identificação do aluno                      |
| Nome_Aluno      | Caractere     | 20 bytes    | NOT NULL        | Nome do Aluno                                         |
| Sobrenome_Aluno | Caractere     | 50 bytes    | NOT NULL        | Sobrenome do aluno                                    |
| CPF             | Caractere     | 11 bytes    | NOT NULL UNIQUE | CPF do aluno                                          |
| Status          | Caractere     | 1 bit       | NOT NULL        | Status da matricula do aluno (S para sim, N para não) |
| whatsapp        | Caractere     | 11 bytes    | NULL            | Whatsapp do aluno                                     |
| e-mail          | Caractere     | 60 bytes    | NOT NULL        | E-mail do aluno                                       |
| Cod_Turma       | inteiro       | 2 bytes     | FK. NOT NULL    | Código de identificação da turma                      |
| Cod_Curso       | inteiro       | 2 Bytes     | FK. NOT NULL    | Código de identificação do curso                      |
| Sexo            | Caractere     | 1 bytes     | NOT NULL        | Sexo do aluno                                         |
| Mãe             | Caractere     | 80 bytes    | NULL            | Nome da mãe do aluno                                  |
| Pai             | Caractere     | 80 bytes    | NULL            | Nome do pai do aluno                                  |


## Atributos - Disciplina 

| Atributo         | Tipo de dados | Comprimento | Restrições   | Descrição                                 |
|------------------|---------------|-------------|--------------|-------------------------------------------|
| Cod_Disciplina   | inteiro       | 2 bytes     | PK. NOT NULL | Código de identificação da disciplina     |
| Nome_Disciplina  | Caractere     | 30 bytes    | NOT NULL     | Nome da disciplina                        |
| Descrição        | Caractere     | 200 bytes   | NULL         | Descrição sobre a disciplina              |
| Cod_departamento | inteiro       | 2 bytes     | FK. NOT NULL | Código de identificação do departamento   |
| Carga_Horaria    | inteiro       | 2 bytes     | NOT NULL     | Carga horária da disciplina               |
| Num_Alunos       | inteiro       | 2 bytes     | NOT NULL     | Números de alunos que cursam a disciplina |

## Atributos - Histórico

| Atributo           	| Tipo de dados 	| Comprimento 	| Restrições  	| Descrição                                    	|
|--------------------	|---------------	|-------------	|-------------	|----------------------------------------------	|
| cod_histórico      	| inteiro       	| 2 bytes     	| PK. NOT NUL 	| Código do historico do aluno                 	|
| RA                 	| Caractere       	| 6 bytes     	| FK. NOT NUL 	| Código de identificação do aluno             	|
| data_inicio        	| data             	| 4 bytes     	| NOT NULL    	| Data de inicio                             	|
| data_fim          	| data             	| 4 bytes     	| NULL         	| Data de fim                                	|

## Atributos - disc_historico

| Atributo       	| Tipo de dados 	| Comprimento 	| Restrições       	| Descrição                             	|
|----------------	|---------------	|-------------	|------------------	|---------------------------------------	|
| cod_histórico  	| inteiro       	| 2 bytes     	| PK. FK. NOT NULL 	| Código do historico do aluno          	|
| cod_disciplina 	| inteiro       	| 2 bytes     	| PK. FK. NOT NULL 	| Código de identificação da disciplina 	|
| nota           	| decimal       	| 8 bytes     	| NOT NULL         	| Nota da disciplina                    	|
| frequencia     	| inteiro       	| 2 bytes     	| NOT NULL         	| numero de falta na disciplina         	|

## Atributos - Curso_disciplina

| Atributo       	| Tipo de dados 	| Comprimento 	| Restrições       	| Descrição                             	|
|----------------	|---------------	|-------------	|------------------	|---------------------------------------	|
| cod_curso      	| inteiro       	| 2 bytes     	| PK. FK. NOT NULL 	| Código de identificação do curso      	|
| cod_disciplina 	| inteiro       	| 2 bytes     	| PK. FK. NOT NULL 	| Código de identificação da disciplina 	|

## Atributos - Prof_disciplina

| Atributo       	| Tipo de dados 	| Comprimento 	| Restrições       	| Descrição                             	|
|----------------	|---------------	|-------------	|------------------	|---------------------------------------	|
| cod_professor  	| inteiro       	| 2 bytes     	| PK. FK. NOT NULL 	| Código de identificação do professor  	|
| cod_disciplina 	| inteiro       	| 2 bytes     	| PK. FK. NOT NULL 	| Código de identificação da disciplina 	|

## Atributo - Aluno_Disc

| Atributo       	| Tipo de dados 	| Comprimento 	| Restrições       	| Descrição                             	|
|----------------	|---------------	|-------------	|------------------	|---------------------------------------	|
| RA             	| caractere      	| 8 bytes     	| PK. FK. NOT NULL 	| Código de identificação do aluno      	|
| cod_disciplina 	| inteiro       	| 2 bytes     	| PK. FK. NOT NULL 	| Código de identificação da disciplina 	|

## Atributo - telefone_aluno

| Atributo       	    | Tipo de dados 	| Comprimento 	| Restrições       	| Descrição                             	    |
|-----------------------|---------------	|-------------	|------------------	|---------------------------------------	    |
| cod_telefone_aluno	| inteiro       	| 1 byte     	| PK. NOT NULL   	| Código de identificação telefone      	    |
| RA                	| caractere       	| 8 bytes     	| FK. NOT NULL   	| Código de identificação do aluno       	    |
| cod_tipo_telefone    	| inteiro       	| 1 byte     	| FK. NOT NULL  	| Código de identificação do tipo de telefone   |
| num_telefone       	| caractere       	| 11 bytes     	| NOT NULL      	| Numero de telefone do aluno            	    |

## Atributo - tipo_telefone

| Atributo       	    | Tipo de dados 	| Comprimento 	| Restrições       	| Descrição                             	     |
|-----------------------|---------------	|-------------	|------------------	|---------------------------------------	     |
| cod_tipo_telefone	    | inteiro       	| 1 byte     	| PK. NOT NULL 	    | Código de identificação do tipo de telefone    |
| tipo_telefone         | caractere       	| 12 bytes     	| NOT NULL   	    | Tipo de telefone                         	     |

## Atributo - endereço_aluno

| Atributo           | Tipo de dados | Comprimento | Restrições         | Descrição                                             |
|------------------- |---------------|-------------|--------------      |-------------------------------------------------------|
| RA                 | caractere     | 8 bytes     | PK. FK. NOT NULL   | Código de identificação do aluno                      |
| cod_endereço_aluno | inteiro       | 1 byte      | PK NOT NULL        | código do endereço do aluno                           |
| cod_tipo_logradouro| Inteiro       | 1 byte      | FK NOT NULL        | Código do tipo de logradouro                          |
| nome_rua           | Caractere     | 50 bytes    | NOT NULL           | Nome da rua que o aluno mora                          |
| núm_rua            | inteiro       | 10 bytes    | NOT NULL           | Número da casa que o aluno mora                       |
| Bairro             | Caractere     | 10 bytes    | NOT NULL           | Bairro que o aluno mora                               |
| Complemento        | Caractere     | 20 bytes    | NULL               | Complemento da casa do aluno                          |
| CEP                | Caractere     | 8 bytes     | NOT NULL           | CEP                                                   |
| Estado             | Caractere     | 1 byte      | NOT NULL           | estado que o aluno mora                               |
| Cidade             | Caractere     | 10 bytes    | NOT NULL           | cidade que o aluno mora                               |

## Atributo - tipo_lougradouro

| Atributo           | Tipo de dados | Comprimento | Restrições   | Descrição                                             |
|------------------- |---------------|-------------|--------------|-------------------------------------------------------|
| cod_tipo_logradouro| Inteiro       | 1 byte      | PK NOT NULL  | Código do tipo de logradouro                          |
| tipo_lougradouro   | caractere     | 10 bytes    | NOT NULL     | tipo de logradouro                                    |