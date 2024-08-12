# DIO - Trilha .NET - API e Entity Framework
www.dio.me

## Desafio de projeto
Para este desafio, você precisará usar seus conhecimentos adquiridos no módulo de API e Entity Framework, da trilha .NET da DIO.

## Contexto
Você precisa construir um sistema gerenciador de tarefas, onde você poderá cadastrar uma lista de tarefas que permitirá organizar melhor a sua rotina.

Essa lista de tarefas precisa ter um CRUD, ou seja, deverá permitir a você obter os registros, criar, salvar e deletar esses registros.

A sua aplicação deverá ser do tipo Web API ou MVC, fique a vontade para implementar a solução que achar mais adequado.

A sua classe principal, a classe de tarefa, deve ser a seguinte:

![Diagrama da classe Tarefa](diagrama.png)

Não se esqueça de gerar a sua migration para atualização no banco de dados.

## Métodos esperados
É esperado que você crie o seus métodos conforme a seguir:


**Swagger**


![Métodos Swagger](swagger.png)


**Endpoints**


| Verbo  | Endpoint                | Parâmetro | Body          |
|--------|-------------------------|-----------|---------------|
| GET    | /Tarefa/{id}            | id        | N/A           |
| PUT    | /Tarefa/{id}            | id        | Schema Tarefa |
| DELETE | /Tarefa/{id}            | id        | N/A           |
| GET    | /Tarefa/ObterTodos      | N/A       | N/A           |
| GET    | /Tarefa/ObterPorTitulo  | titulo    | N/A           |
| GET    | /Tarefa/ObterPorData    | data      | N/A           |
| GET    | /Tarefa/ObterPorStatus  | status    | N/A           |
| POST   | /Tarefa                 | N/A       | Schema Tarefa |

Esse é o schema (model) de Tarefa, utilizado para passar para os métodos que exigirem

```json
{
  "id": 0,
  "titulo": "string",
  "descricao": "string",
  "data": "2022-06-08T01:31:07.056Z",
  "status": "Pendente"
}
```


## Solução
O código está pela metade, e você deverá dar continuidade obedecendo as regras descritas acima, para que no final, tenhamos um programa funcional. Procure pela palavra comentada "TODO" no código, em seguida, implemente conforme as regras acima.

## Sobre o Projeto (Meu Desafio entregue)
Neste projeto, construí uma aplicação Web API para gerenciar tarefas. A aplicação permite criar, ler, atualizar e excluir tarefas (CRUD). Utilizei o Entity Framework Core para interagir com o banco de dados e configurei a API para expor endpoints RESTful para a manipulação de tarefas.

## Funcionalidades
Criar Tarefa: Permite adicionar novas tarefas ao banco de dados.
Obter Tarefa por ID: Recupera uma tarefa específica usando seu ID.
Obter Todas as Tarefas: Lista todas as tarefas cadastradas.
Obter Tarefas por Título: Filtra tarefas com base no título fornecido.
Obter Tarefas por Data: Filtra tarefas com base na data fornecida.
Obter Tarefas por Status: Filtra tarefas com base no status fornecido.
Atualizar Tarefa: Atualiza uma tarefa existente usando seu ID.
Deletar Tarefa: Remove uma tarefa específica do banco de dados.
Estrutura do Projeto
O projeto é uma aplicação ASP.NET Core Web API que utiliza o Entity Framework Core para a persistência dos dados. A API está configurada com Swagger para facilitar a documentação e o teste dos endpoints.


