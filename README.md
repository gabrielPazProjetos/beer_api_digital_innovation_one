--- Beer API - Digital Innovation One (forkado)
API REST para gerenciamento de estoques de cerveja, desenvolvida com Spring Boot.  
Este projeto foi utilizado em um projeto da DIO para demonstrar testes unitários com JUnit e Mockito, além da prática de TDD e modificado por mim de acordo com a
proposta do desafio .

--- Funcionalidades
-- A API permite:
- Criar uma cerveja (POST /api/v1/beers)
- Listar todas as cervejas (GET /api/v1/beers)
- Buscar cerveja por nome (GET /api/v1/beers/{name})
- Deletar cerveja por ID (DELETE /api/v1/beers/{id})
- Incrementar estoque (PATCH /api/v1/beers/{id}/increment)
- Decrementar estoque (PATCH /api/v1/beers/{id}/decrement) 

--- Tecnologias utilizadas
- Java 14+
- Spring Boot
- Maven 3.6.3+
- JUnit 5
- Mockito
- Hamcrest
- Swagger (documentação da API)
- Postman (coleção de requisições)

--- Pré-requisitos
- Java 14 ou superior
- Maven 3.6.3 ou superior
- Git instalado
- IDE (IntelliJ IDEA Community Edition ou outra)

--- Como executar
-- Rodar a aplicação:
- bash
mvn spring-boot:run
Rodar os testes:

- bash
mvn clean test
Acesse a API em:

--- Testes Unitários
-- Os testes unitários foram desenvolvidos com JUnit 5 e Mockito, cobrindo os seguintes cenários:
- Criação de cerveja
- Busca por nome
- Listagem
- Exclusão
- Incremento de estoque
- Decremento de estoque 
- Decremento normal
- Decremento até zerar estoque
- Decremento abaixo de zero (lança exceção)
- Decremento com ID inválido (lança exceção)

--- Documentação Swagger
-- A API está documentada com Swagger. Endpoints disponíveis:
- POST /api/v1/beers
- GET /api/v1/beers/{name}
- GET /api/v1/beers
- DELETE /api/v1/beers/{id}
- PATCH /api/v1/beers/{id}/increment
- PATCH /api/v1/beers/{id}/decrement �

--- Postman Collection
-- O projeto inclui uma coleção Postman (postman/Beer API.postman_collection.json) com requisições prontas para testar a API:
- List Beers
- Create Beer
- Get Beer by Name
- Delete Beer by ID
- Increment Beer Stock 
- Decrement Beer Stock 

--- Alterações realizadas
-- Durante o desenvolvimento foram adicionadas as seguintes melhorias:
- BeerService
- Implementado método decrement(Long id, int quantityToDecrement).
- BeerController
- Criado endpoint REST PATCH /api/v1/beers/{id}/decrement.
- BeerControllerDocs
- Documentação Swagger atualizada para incluir increment e decrement.
Postman Collection

Adicionada requisição para PATCH /api/v1/beers/{id}/decrement.
