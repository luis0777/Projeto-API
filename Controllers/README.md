# AutorController:

## Propósito
Gerencia as operações relacionadas aos autores.

## Métodos:
ListarAutores: Lista todos os autores.
BuscarAutorPorId: Busca um autor pelo seu ID.
BuscarAutorPorIdLivro: Busca o autor de um livro específico pelo ID do livro.
CriarAutor: Cria um novo autor com base nos dados fornecidos.
EditarAutor: Edita as informações de um autor existente.
ExcluirAutor: Exclui um autor com base no ID fornecido.

## Estrutura:
O controlador usa a interface IAutorInterface, que se conecta ao serviço responsável por lidar com as operações do banco de dados.

## LivroController:

## Propósito: 
Gerencia as operações relacionadas aos livros.

## Métodos:
ListarLivros: Lista todos os livros.
BuscarLivroPorId: Busca um livro pelo seu ID.
BuscarLivroPorIdAutor: Busca livros de um autor específico usando o ID do autor.
CriarLivro: Cria um novo livro com base nos dados fornecidos.
EditarLivro: Edita as informações de um livro existente.
ExcluirLivro: Exclui um livro com base no ID fornecido.

## Estrutura:
O controlador usa a interface ILivroInterface, que, assim como no caso dos autores, se conecta ao serviço que interage com o banco de dados.

Ambos os controladores seguem um padrão similar, onde recebem as requisições HTTP, invocam os métodos das respectivas interfaces para interagir com os serviços e retornam os resultados apropriados (como lista de autores ou livros, dados individuais ou status de sucesso/erro).
