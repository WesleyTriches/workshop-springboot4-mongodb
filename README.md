# Workshop Spring Boot 4 - CRUD com MongoDB

Projeto desenvolvido no curso:

**Java COMPLETO - Programação Orientada a Objetos + Projetos**  
Instrutor: **Nélio Alves**

Este projeto implementa uma **API REST** com operações **CRUD**, utilizando **Spring Boot**, **Spring Data MongoDB** e **MongoDB** como banco de dados NoSQL.  
O objetivo é praticar conceitos de orientação a objetos, estruturação de projetos backend e desenvolvimento de APIs RESTful.

## Tecnologias utilizadas
- Java  
- Spring Boot  
- Spring Data MongoDB  
- MongoDB  
- Maven  

## Funcionalidades

O projeto oferece os seguintes endpoints RESTful:

| Método | Endpoint        | Descrição                    |
|------|-----------------|------------------------------|
| GET  | `/users`        | Lista todos os usuários      |
| GET  | `/users/{id}`   | Busca um usuário por ID      |
| POST | `/users`        | Cria um novo usuário         |
| PUT  | `/users/{id}`   | Atualiza um usuário existente|
| DELETE | `/users/{id}` | Remove um usuário            |

## Tratamento de exceções

O projeto utiliza um **handler global de exceções** para retornar respostas padronizadas em casos de erro, como:

- **ResourceNotFoundException** → retorna HTTP 404 quando o recurso não é encontrado  
- **DatabaseException** → retorna HTTP 400 para erros de integridade ou operações inválidas  

### Exemplo de resposta JSON de erro

```json
{
  "timestamp": "2026-01-22T22:07:50Z",
  "status": 404,
  "error": "Resource not found",
  "message": "Resource not found. Id 8",
  "path": "/users/8"
}
