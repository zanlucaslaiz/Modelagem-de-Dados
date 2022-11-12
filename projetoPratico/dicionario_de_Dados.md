# Dicionario de Dados

## Entidades


| Entidade     	| Relacionamento   	| Nome do Relacionamento 	| Descrição                                                               	|
|--------------	|------------------	|------------------------	|-------------------------------------------------------------------------	|
| Departamento 	| Professor        	| Pertence               	| Tabela para cadastro dos departamentos da faculdade                     	|
|              	| Disciplina       	| Responsável            	|                                                                         	|
|              	| Curso            	| Controla               	|                                                                         	|
| Professor    	| Departamento     	| Pertence               	| Tabela para cadastro dos professores da faculdade                       	|
|              	| Prof_Disciplina  	| Leciona                	|                                                                         	|
| Turma        	| Curso            	| Gera                   	| Tabela para registro de turmas em andamento e encerradas                	|
|              	| Aluno            	| Pertence               	|                                                                         	|
| Curso        	| Departamento     	| Controla               	| Tabela para cadastro de cursos da faculdade                             	|
|              	| Curso_Disciplina 	| Possui                 	|                                                                         	|
|              	| Turma            	| Gera                   	|                                                                         	|
|              	| Aluno            	| Matriculado            	|                                                                         	|
| Aluno        	| Curso            	| Matriculado            	| Tabela para cadastro dos alunos da faculdade                            	|
|              	| Turma            	| Pertence               	|                                                                         	|
|              	| Disciplina       	| Cursa                  	|                                                                         	|
|              	| Histórico        	| Pertence               	|                                                                         	|
| Disciplina   	| Departamento     	| Responsável            	| Tabela para cadastro das disciplinas que compoe  os cursos da faculdade 	|
|              	| Prof_Disciplina  	| É Lecionada            	|                                                                         	|
|              	| Aluno            	| Cursa                  	|                                                                         	|
|              	| Curso_Disciplina 	| Pertence               	|                                                                         	|
|              	| Disc_Histórico   	| Compoe                 	|                                                                         	|
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

## Atributos

