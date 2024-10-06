# AppDbContext:

# Propósito:
Serve como o intermediário entre o código da aplicação e o banco de dados. Essa classe gerencia as operações de banco de dados, como consultas e alterações nas tabelas.

# Construtor:
Recebe um objeto DbContextOptions<AppDbContext> chamado options, que contém as opções de configuração do banco de dados, como a string de conexão. Ele é passado para o construtor da classe base DbContext.

# Propriedades:
DbSet<AutorModel> Autores: Representa a tabela de autores no banco de dados. Baseada no modelo AutorModel, ela permite realizar operações CRUD (criar, ler, atualizar, deletar) na tabela Autores.

DbSet<LivroModel> Livros: Representa a tabela de livros no banco de dados. Baseada no modelo LivroModel, ela permite realizar operações CRUD na tabela Livros.

# Conclusão
Essa classe define como as tabelas Autores e Livros serão mapeadas para os modelos AutorModel e LivroModel, além de gerenciar a conexão e comunicação com o banco de dados.
