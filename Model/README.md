# AutorModel
Propósito: Representa o modelo de dados para o autor no banco de dados.

Propriedades:

Id: Identificador único do autor.

Nome: Nome do autor.

Sobrenome: Sobrenome do autor.

Livros: Uma coleção de objetos LivroModel representando os livros associados a esse autor. Esta propriedade é ignorada durante a serialização JSON, pois o atributo [JsonIgnore] está aplicado, evitando a serialização cíclica e reduzindo a carga de dados.

# LivroModel
Propósito: Representa o modelo de dados para o livro no banco de dados.

Propriedades:

Id: Identificador único do livro.

Titulo: Título do livro.

Autor: Referência ao objeto AutorModel associado ao livro. Isso define o relacionamento de muitos-para-um entre LivroModel e AutorModel.

# ResponseModel<T>
Propósito: Uma classe genérica que serve como um padrão para as respostas de API.

Propriedades:

Dados: Um dado do tipo genérico T, que pode representar qualquer tipo, como autor ou livro. O uso de T? indica que este dado pode ser nulo.

Mensagem: Uma mensagem de resposta que fornece informações adicionais sobre o sucesso ou erro da operação.

Status: Um booleano que indica o status da operação (sucesso ou falha).
