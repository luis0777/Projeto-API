# AutorCriacaoDto
Propósito: Serve como um objeto de transferência de dados (DTO) para a criação de um autor.

Propriedades:

Nome: Nome do autor.

Sobrenome: Sobrenome do autor.

# AutorEdicaoDto
Propósito: É usado como DTO para editar um autor existente.

Propriedades:

Id: Identificador único do autor.

Nome: Nome atualizado do autor.

Sobrenome: Sobrenome atualizado do autor.

# LivroCriacaoDto
Propósito: Usado como DTO para criar um novo livro.

Propriedades:

Titulo: Título do livro.

Autor: Um objeto AutorVinculoDto que representa o autor vinculado ao livro.

# LivroEdicaoDto

Propósito: Usado como DTO para editar as informações de um livro existente.

Propriedades:

Id: Identificador único do livro.

Titulo: Título atualizado do livro.

Autor: Um objeto AutorVinculoDto que representa o autor vinculado ao livro.

# AutorVinculoDto
Propósito: Usado para vincular as informações básicas de um autor com outros objetos, como um livro.

Propriedades:

Id: Identificador do autor.

Nome: Nome do autor.

Sobrenome: Sobrenome do autor.

# Conclusão
Esses DTOs são usados para transferir dados entre as camadas da aplicação sem expor diretamente os modelos do banco de dados, facilitando operações como criação e edição de autores e livros.
