# Gerenciador de Repositórios - API REST

Este projeto implementa uma **API REST** para gerenciar repositórios, utilizando C# 12, Entity Framework Core com banco de dados em memória (InMemory) e Swagger para documentação. A API permite realizar operações como listar, cadastrar, atualizar e excluir repositórios, além de marcar repositórios como favoritos e listar repositórios favoritos.

# Funcionalidades

A API oferece os seguintes endpoints:

- `GET /repositorio` - Listar todos os repositórios.
- `GET /repositorio/{id}` - Obter um repositório específico pelo ID.
- `POST /repositorio` - Cadastrar um novo repositório.
- `PUT /repositorio/{id}` - Atualizar um repositório existente.
- `DELETE /repositorio/{id}` - Remover um repositório.
- `GET /meus-repositorios` - Listar os repositórios do candidato (você).
- `GET /buscar-repositorios` - Buscar repositórios por nome ou parte do nome.
- `POST /favoritar/{id}` - Marcar um repositório como favorito.
- `GET /favoritos` - Listar todos os repositórios favoritos.

# Tecnologias Utilizadas

- **C# 12**
- **ASP.NET Core** (API REST)
- **Entity Framework Core** (InMemory)
- **Swagger** (para documentação da API)
- **xUnit** (para testes unitários)
- **Serilog** (opcional, para logs)

# Requisitos

- **.NET 7.0 ou superior**
- **Visual Studio 2022 ou superior**

# Como Rodar o Projeto

# 1) Clonar o repositório

git clone https://github.com/seu-usuario/repositorio-api.git

# 2) Abrir o projeto no Visual Studio

Abra o Visual Studio 2022 ou superior e carregue o projeto.

# 3) Rodar a aplicação

Para rodar a aplicação, basta pressionar F5 no Visual Studio.

# 4) Acessar a documentação Swagger

Após rodar a aplicação, você pode acessar a documentação interativa da API utilizando o Swagger em:

https://localhost:7173/swagger/index.html

# 5) Estrutura do Projeto

O projeto está organizado nas seguintes pastas:

Controllers: Contém os controladores da API, responsáveis pelas rotas e lógica de requisições HTTP.

RepositorioController.cs: Controlador principal para gerenciar os repositórios.
Data: Contém o DbContext e configurações do banco de dados.

AppDbContext.cs: Contexto de banco de dados usando Entity Framework Core com InMemory Database.
Models: Contém as classes de modelo de dados.

Repositorio.cs: Modelo de dados para os repositórios.
Services: Contém os serviços que podem implementar lógica de negócios.

RepositorioService.cs: Serviço que contém a lógica de busca e manipulação de repositórios.
Tests: Contém os testes unitários para a API e os serviços.

RepositorioControllerTests.cs: Testes para o controlador de repositórios.
RepositorioServiceTests.cs: Testes para o serviço de repositórios.

# 6) Como Funciona

1. Criar um Repositório
   
Para cadastrar um novo repositório, envie uma requisição POST para /repositorio com o seguinte corpo:

{
  "nome": "Meu Repositorio",
  "descricao": "Descrição do repositório",
  "linguagem": "C#",
  "dono": "Candidato"
}

2. Atualizar um Repositório
   
Para atualizar um repositório, envie uma requisição PUT para /repositorio/{id} com o corpo de atualização desejado.

3. Marcar como Favorito
   
Para marcar um repositório como favorito, envie uma requisição POST para /favoritar/{id}.

4. Buscar Repositórios
   
Você pode buscar repositórios por nome enviando uma requisição GET para /buscar-repositorios?nome=parte-do-nome.

# Contribuições

Contribuições são bem-vindas! Se você tiver sugestões de melhorias ou correções de bugs, sinta-se à vontade para abrir uma issue ou enviar um pull request.
