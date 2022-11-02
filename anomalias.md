# Anomalias de Atualização

Anomalias são problemas que ocorrem em bancos de dados mal planejados e não-normalizados, geralmente ocorrendo por excesso de dados armazenados em uma mesma tabela.
São causadas pelas dependências parciais e transitivas.
As anomalias de atualização são classificadas em anomalias de inserção, de exclusão e de modificação.

## Anomalia de Inclusão 

Não deve ser possível adicionar um dado a não ser que outro dado esteja disponível. Por exemplo, não deve ser permitido cadastrar um novo livro sem que um autor já esteja cadastrado.

## Anomalia de exclusão

Ao excluirmos um registro, dados referentes em outra tabela são excluídos. Por exemplo, se excluirmos um autor, os livros desse autor devem ser excluídos também.

## Anomalia de modificação

Ao alterar um dado em uma tabela, dados em outras tabelas precisam ser alterados. Por exemplo, se o código de um autor for modificado na tabela de autores e na de livros também, para manter o relacionamento entre livros e seus autores corretos.

## Eliminar anomalias

Projetar os esquemas de relações (tabelas) no banco de dados de modo que nenhuma anomalia de inserção, exclusão ou modificação esteja presente nas relações. Para isso usamos o processo de Normalização.
