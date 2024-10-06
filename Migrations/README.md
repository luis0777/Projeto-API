# CriandoBancoDeDados (Classe parcial Migration)
Propósito: Representa uma migração que cria as tabelas de autores e livros no banco de dados.
Métodos:

Up: Método que define o que será feito na migração. Neste caso:

Cria a tabela Autores com as colunas Id, Nome, e Sobrenome.

Cria a tabela Livros com as colunas Id, Titulo, e AutorId (chave estrangeira que faz referência à tabela Autores).

Configura o relacionamento entre Livros e Autores, onde cada livro está associado a um autor e, se o autor for excluído, seus livros também são excluídos (Cascade).

Down: Método que define o que será revertido, removendo as tabelas Livros e Autores.

# AppDbContextModelSnapshot (Classe gerada automaticamente)
Propósito: Representa um instantâneo do modelo de dados no contexto do banco de dados.

Detalhes:

Autores: Define a estrutura da tabela Autores, incluindo as colunas Id, Nome, e Sobrenome, além da chave primária Id.

Livros: Define a estrutura da tabela Livros, incluindo as colunas Id, Titulo, e AutorId, além da chave primária Id e o índice na coluna AutorId.

# Conclusão
Configura o relacionamento entre as tabelas Livros e Autores, definindo que cada livro tem um autor vinculado (Autor) e que um autor pode ter muitos livros associados.
Essas classes garantem a criação e manutenção da estrutura do banco de dados conforme o modelo da aplicação evolui.
