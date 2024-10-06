#  AutorService
Essa classe é responsável pela implementação das operações relacionadas ao Autor, como listagem, busca, criação, edição e exclusão de autores no banco de dados.

Propriedades e Métodos:
_context: Um campo privado e de somente leitura que representa o AppDbContext, que é usado para interagir com o banco de dados.

Construtor:

Recebe uma instância do AppDbContext via injeção de dependência, permitindo acesso ao banco de dados.
Métodos:

BuscarAutorPorId: Busca um autor pelo seu Id. Se o autor não for encontrado, uma mensagem é retornada. Caso contrário, os dados do autor são retornados.

BuscarAutorPorIdLivro: Busca o autor associado a um livro específico, utilizando o Id do livro.

CriarAutor: Cria um novo autor com base nos dados recebidos via AutorCriacaoDto. Após salvar no banco, retorna uma lista atualizada de autores.

EditarAutor: Edita os dados de um autor existente no banco de dados com base no AutorEdicaoDto. Atualiza e retorna a lista de autores.

ExcluirAutor: Remove um autor do banco de dados com base no Id. Após a remoção, retorna a lista atualizada de autores.

ListarAutores: Retorna uma lista de todos os autores presentes no banco de dados.

Detalhes Importantes:

Uso de ResponseModel<T>: Cada método retorna uma instância de ResponseModel<T>, onde T é o tipo de dado específico (por exemplo, AutorModel ou uma lista de AutorModel). Isso padroniza as respostas da API e facilita o manuseio de mensagens e status.

Métodos Assíncronos (async e await): A maioria dos métodos são assíncronos para garantir que a aplicação possa manipular tarefas de longa duração (como consultas ao banco) sem bloquear a execução de outras tarefas.

#  IAutorInterface
Essa interface define os contratos (assinaturas de métodos) que a classe AutorService deve seguir. Ela atua como um vínculo entre o Controller e o Service, garantindo que o Controller se conecte a um serviço que implemente as operações necessárias.

Métodos Definidos:

ListarAutores: Lista todos os autores.

BuscarAutorPorId: Busca um autor específico por Id.

BuscarAutorPorIdLivro: Busca o autor relacionado a um livro específico por Id.

CriarAutor: Cria um novo autor.

EditarAutor: Edita os dados de um autor existente.

ExcluirAutor: Remove um autor com base no Id.

# Resumo do Funcionamento:
O Controller se conecta à IAutorInterface para chamar métodos relacionados a autores.

A IAutorInterface garante que o Controller tenha acesso a um conjunto consistente de métodos.

A implementação real das operações ocorre no AutorService, onde a comunicação direta com o banco de dados via AppDbContext acontece.

As operações são padronizadas usando a classe ResponseModel<T>, o que garante respostas claras e consistentes da API, com informações sobre status e mensagens.
