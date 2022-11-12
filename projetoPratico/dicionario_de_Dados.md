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
|              	| Disciplina       	| Cursa                  	|                                                                         	|
|              	| Histórico        	| Pertence               	|                                                                         	|
|--------------	|------------------	|------------------------	|-------------------------------------------------------------------------	|
| Disciplina   	| Departamento     	| Responsável            	| Tabela para cadastro das disciplinas que compoe  os cursos da faculdade 	|
|              	| Prof_Disciplina  	| É Lecionada            	|                                                                         	|
|              	| Aluno            	| Cursa                  	|                                                                         	|
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

## Atributos - Departamento

| Atributo          	| Tipo de dados 	| Comprimento 	| Restrições   	| Descrição                               	|
|-------------------	|---------------	|-------------	|--------------	|-----------------------------------------	|
| Cod_Departamento  	| Inteiro       	| 4 bytes     	| PK. NOT NULL 	| Código de identificação do departamento 	|
| Nome_Departamento 	| Caractere     	| 40 bytes    	| NOT NULL     	| Nome do departamento                    	|
| Localização       	| Caractere     	| 20 bytes    	| NOT NULL     	| Localização do departamento             	|

## Atributos - Professor

| Atributo            	| Tipo de dados 	| Comprimento 	| Restrições   	| Descrição                                       	|
|---------------------	|---------------	|-------------	|--------------	|-------------------------------------------------	|
| Cod_Professor       	| Inteiro       	| 4 bytes     	| PK. NOT NULL 	| Código de identificação do Professor            	|
| Nome_Professor      	| Caractere     	| 40 bytes    	| NOT NULL     	| Nome do Professor                               	|
| Sobrenome_Professor 	| Caractere     	| 40 bytes    	| NOT NULL     	| Sobrenome do professor                          	|
| Cod_Departamento    	| Inteiro       	| 4 bytes     	| FK. NOT NULL 	| Código de identificação do Departamento         	|
| Status              	| Booleano      	| 1 bytes     	| NOT NULL     	| Status do professor (Lecionando/Não Lecionando) 	|

## Atributos - Turma

| Atributo    	| Tipo de dados 	| Comprimento 	| Restrições   	| Descrição                               	|
|-------------	|---------------	|-------------	|--------------	|-----------------------------------------	|
| Cod_Turma   	| Inteiro       	| 4 bytes     	| PK. NOT NULL 	| Código de identificação da turma        	|
| Cod_Curso   	| Inteiro       	| 4 bytes     	| FK. NOT NULL 	| Código de identificação do Curso        	|
| Período     	| Caractere     	| 10 bytes    	| NOT NULL     	| Período da turma (manhã, tarde, noite)  	|
| Num_Alunos  	| Inteiro       	| 2 bytes     	| NOT NULL     	| Números de alunos matriculados na turma 	|
| Data_inicio 	| Data          	| 4 bytes     	| NOT NULL     	| Data de inicio do turma                 	|
| Data_Fim    	| Data          	| 4 bytes     	| NOT NULL     	| Date de fim da turma                    	|

## Atributos - Curso

| Atributo         	| Tipo de dados 	| Comprimento 	| Restrições   	| Descrição                               	|
|------------------	|---------------	|-------------	|--------------	|-----------------------------------------	|
| Cod_Curso        	| Inteiro       	| 4 bytes     	| PK. NOT NULL 	| Código de Identificação do curso        	|
| Nome_Curso       	| Caractere     	| 40 bytes    	| NOT NULL     	| Nome do curso                           	|
| Cod_Departamento 	| Inteiro       	| 4 bytes     	| FK. NOT NULL 	| Código de Identificação do Departamento 	|

## Atributos - Aluno

| Atributo        |        | Tipo de dados | Comprimento | Restrições   | Descrição                                             |
|-----------------|--------|---------------|-------------|--------------|-------------------------------------------------------|
| RA              |        | Inteiro       | 8 bytes     | PK. NOT NULL | Código de identificação do aluno                      |
| Nome_Aluno      |        | Caractere     | 25 bytes    | NOT NULL     | Nome do Aluno                                         |
| Sobrenome_Aluno |        | Caractere     | 40 bytes    | NOT NULL     | Sobrenome do aluno                                    |
| CPF             |        | Caractere     | 40 bytes    | NOT NULL     | CPF do aluno                                          |
| Telefone        |        | Caractere     | 40 bytes    | NOT NULL     | Telefone* do aluno                                    |
| Status          |        | Caractere     | 1 bytes     | NOT NULL     | Status da matricula do aluno (S para sim, N para não) |
| Contato         |        | Caractere     | 40 bytes    | NOT NULL     | Formas de contato com o aluno                         |
| Cod_Turma       |        | inteiro       | 4 bytes     | FK. NOT NULL | Código de identificação da turma                      |
| Cod_Curso       |        | inteiro       | 4 Bytes     | FK. NOT NULL | Código de identificação do curso                      |
| Sexo            |        | Caractere     | 1 bytes     | NOT NULL     | Sexo do aluno                                         |
| Filiação        |        | Caractere     | 80 bytes    | NOT NULL     | Nome dos pais do aluno                                |
| Endereço        | Rua    | Caractere     | 80 bytes    | NOT NULL     | Endereço do aluno divido em Rua, número e CEP         |
|                 | número | Caractere     | 10 bytes    | NOT NULL     |                                                       |
|                 | CEP    | Caractere     | 10 bytes    | NOT NULL     |                                                       |

## Atributos - Disciplina 

| Atributo         | Tipo de dados | Comprimento | Restrições   | Descrição                                 |
|------------------|---------------|-------------|--------------|-------------------------------------------|
| Cod_Disciplina   | inteiro       | 4 bytes     | PK. NOT NULL | Código de identificação da disciplina     |
| Nome_Disciplina  | Caractere     | 30 bytes    | NOT NULL     | Nome da disciplina                        |
| Descrição        | Caractere     | 200 bytes   | NULL         | Descrição sobre a disciplina              |
| Cod_departamento | inteiro       | 4 bytes     | FK. NOT NULL | Código de identificação do departamento   |
| Carga_Horaria    | inteiro       | 4 bytes     | NOT NULL     | Carga horária da disciplina               |
| Num_Alunos       | inteiro       | 4 bytes     | NOT NULL     | Números de alunos que cursam a disciplina |

## Atributos - Histórico

| Atributo           	| Tipo de dados 	| Comprimento 	| Restrições  	| Descrição                                    	|
|--------------------	|---------------	|-------------	|-------------	|----------------------------------------------	|
| cod_histórico      	| inteiro       	| 4 bytes     	| PK. NOT NUL 	| Código do historico do aluno                 	|
| RA                 	| inteiro       	| 8 bytes     	| FK. NOT NUL 	| Código de identificação do aluno             	|
| periodo_realização 	| inteiro       	| 4 bytes     	| NOT NULL    	| Período de realização da disciplina em meses 	|


## Atributos - disc_historico

| Atributo       	| Tipo de dados 	| Comprimento 	| Restrições       	| Descrição                             	|
|----------------	|---------------	|-------------	|------------------	|---------------------------------------	|
| cod_histórico  	| inteiro       	| 4 bytes     	| PK. FK. NOT NULL 	| Código do historico do aluno          	|
| cod_disciplina 	| inteiro       	| 4 bytes     	| PK. FK. NOT NULL 	| Código de identificação da disciplina 	|
| nota           	| decimal       	| 8 bytes     	| NOT NULL         	| Nota da disciplina                    	|
| frequencia     	| inteiro       	| 4 bytes     	| NOT NULL         	| numero de falta na disciplina         	|

## Atributos - Curso_disciplina

| Atributo       	| Tipo de dados 	| Comprimento 	| Restrições       	| Descrição                             	|
|----------------	|---------------	|-------------	|------------------	|---------------------------------------	|
| cod_curso      	| inteiro       	| 4 bytes     	| PK. FK. NOT NULL 	| Código de identificação do curso      	|
| cod_disciplina 	| inteiro       	| 4 bytes     	| PK. FK. NOT NULL 	| Código de identificação da disciplina 	|

## Atributos - Prof_disciplina

| Atributo       	| Tipo de dados 	| Comprimento 	| Restrições       	| Descrição                             	|
|----------------	|---------------	|-------------	|------------------	|---------------------------------------	|
| cod_professor  	| inteiro       	| 4 bytes     	| PK. FK. NOT NULL 	| Código de identificação do professor  	|
| cod_disciplina 	| inteiro       	| 4 bytes     	| PK. FK. NOT NULL 	| Código de identificação da disciplina 	|