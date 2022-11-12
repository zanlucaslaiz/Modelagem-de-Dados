# Banco de dados para gerenciamento de uma faculdade.

## Objetivos do banco de dados:

* Realizar controle centralizado de alunos, professores, cursos, disciplinas, histórico escolar e turmas.

## Fases do Projeto

Fases:
* Levantamento dos Requisitos;
* Identificação de Entidades e Relacionamentos;
* Diagrama E-R: Cardinalidade;
* Diagrama E-R: Eliminando N:M;
* Modelo Lógico;
* Dicionário de dados;
* Normalização;
* Implementação;
* Teste Básicos;

## Levantamento dos Requisitos

### Regras do Negócio

* Um aluno só pode estar matriculado em um curso por vez;
* Alunos possuem um código de identificação (RA);
* Cursos são compostos por disciplinas;
* Cada disciplina terá no máximo 30 alunos por turma;
* As disciplinas pertencem a departamentos específicos;
* Cada disciplina possui um código de identificação;
* Alunos podem trancar matrícula, não estando então matriculados em nenhuma disciplina no semestre;
* Em cada semestre, cada aluno pode se matricular em no máxima 9 disciplinas;
* O aluno só pode ser reprovado no máximo 3 vezes na mesma disciplina;
* A faculdade terá no máximo 3.000 alunos matriculados simultaneamente, em 10 cursos distintos;
* Entram 300 alunos novos por ano;
* Existem 90 disciplinas no total disponíveis;
* Um histórico escolar traz todas as disciplinas cursadas por um aluno, incluindo nota final, frequência e período do curso realizado;
* Professores podem ser cadastrados mesmo sem lecionar disciplinas;
* Existem 40 professores trabalhando na escola;
* Cada professor é vinculado a um departamento;
* Professores são identificados por um código de professor;



Obs.: Pode ser que essas regras de negócio estejam faltando, pois o cliente pode ter esquecido de passar alguma informação ou simplesmente não sabia que determinada informação seria relevante, por isso logo do projeto algumas coisas podem acabar mudando.

## Identificação de Entidades:
* Aluno;
* Professor;
* Disciplina;
* Curso;
* Departamento;
* Turma;
* Histórico;

## Identificação de Relacionamentos:
* Aluno está matriculado em Curso;
* Aluno Cursa Disciplina;
* Aluno Realizou Disciplina;
* Aluno Pertence a Historico;
* Aluno pertence a turma;
* Disciplina Pertence a Curso;
* Professor Ministra Disciplina;
* Professor Pertence a Departamento;
* Departamento é Responsável por Disciplina;
* Departamento Controla Curso;
* Disciplina Depende de Disciplina;
* Historico pertence a aluno;
* Historico compoe disciplina;

## Idendificação de Atributos:

### Aluno:
* RA;
* Nome;
* Sobrenome;
* Endereço;
	* Rua
	* Número
	* Bairro
	* CEP
	* Cidade
	* Estado
* Código do curso;
* Telefone;

Aluno - Contato

* Status
* Filiação
* Sexo
* Contato
	* Whatsapp
	* E-mail
* Cod_Turma
* CPF

### Professor:
* Código do Professor;
* Nome;
* Sobrenome;
* Código do Departamento;
* Status.

### Disciplina:
* Código de Disciplina;
* Nome da Disciplina;
* Descrição Curricular;
* Código do Departamento;
* Número de Alunos;
* Carga Horaria;

### Curso
* Código do Curso;
* Nome do Curso;
* Código do Departamento.

### Departamento:
* Código do Departamento;
* Nome do Departamento.

### Histórico:

* Cod_Histórico;
* Notas;
* Média;
* Frequencia;
* Periodo_Realização;
* RA;
* Cod_Diciplina;

### Turma:

* Cod_turma;
* Periodo;
* Cod_Curso;
* Num_Alunos;
* Data_Inicio;
* Data_Fim;
