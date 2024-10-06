# ILivroInterface
A interface define os métodos que o serviço de livros deve implementar:

ListarLivros: Retorna todos os livros.

BuscarLivroPorId: Busca um livro pelo seu ID.

BuscarLivroPorIdAutor: Busca livros de um autor específico pelo ID.

CriarLivro: Adiciona um novo livro.

EditarLivro: Atualiza as informações de um livro existente.

ExcluirLivro: Remove um livro do banco de dados.

# LivroService
Implementa a interface ILivroInterface e realiza operações com o banco de dados:

BuscarLivroPorId

Descrição: Busca um livro pelo ID.

Resultado: Retorna o livro encontrado ou uma mensagem de erro.

BuscarLivroPorIdAutor

Descrição: Busca todos os livros de um autor específico.

Resultado: Retorna a lista de livros ou uma mensagem se nenhum livro for encontrado.

CriarLivro

Descrição: Cria um novo livro no banco de dados.

Resultado: Retorna a lista atualizada de livros ou uma mensagem de erro se o autor não existir.

EditarLivro

Descrição: Atualiza as informações de um livro existente.

Resultado: Retorna a lista de livros ou uma mensagem se o livro ou o autor não forem encontrados.

ExcluirLivro

Descrição: Remove um livro do banco de dados pelo ID.

Resultado: Retorna a lista de livros restantes ou uma mensagem se o livro não for encontrado.

ListarLivros

Descrição: Retorna todos os livros do banco de dados.

Resultado: Retorna a lista de livros ou uma mensagem de erro
