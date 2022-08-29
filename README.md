# Desafio Técnico


## Descrição
Fazer uma aplicação to do list.

No nosso time, utilizamos principalmente React, Typescript, styled components… mas você é livre para fazer o desafio com a tecnologia que preferir. 

## Protótipo
O protótipo da aplicação está disponível em: 
https://www.figma.com/community/file/1146087484157280937

Basta fazer uma cópia do arquivo e você terá acesso a todas as informações. 
Para baixar os assets, ícones… você precisa selecionar o frame e exportar do Figma (em anexo dessa mensagem, há um print mostrando como exportar)

Você também é livre para fazer melhorias e implementações de features na aplicação/no design.

## O aplicativo deve ter:

1.1 - Formulário de adicionar to do (Modal)

1.1.1 - O to do deve possuir um título e uma descrição

1.2 - Lista de to dos com opção de deletar

1.3 - Nome do usuário "logado" para identificar de quem é a conta

## Como rodar a API

Para rodar a api, você precisa criar um cluster no MongoDB. Instruções aqui: https://docs.google.com/document/d/1tUOKVA8jwhZJ8LKGwjfbVdW6nOC65Yl1iAS1J2YdjTs/edit?usp=sharing

Depois de clonar o repositório, entre no diretório e instale as dependências com o comando `yarn`

Caso não tenha o yarn, é possível instalar com o comando
`npm i -g yarn`

Agora é só rodar a aplicação com `yarn start` (rodará na porta 3000)

## Rotas

```json
API URL http://localhost:3000

List Todos
GET /todos
Response:
[
    {
        "_id": string,
        "title": string,
        "description": string,
        "createdAt": string,
        "updatedAt": string,
        "__v": number
    }
]

Create Todo
POST /todos
Request body:
{
    "title": string,
    "description": string
}

Response:
{
    "_id": string,
    "title": string,
    "description": string,
    "createdAt": string,
    "updatedAt": string,
    "__v": number
}

Detail Todo
GET /todos/:id
Response:
{
    "_id": string,
    "title": string,
    "description": string,
    "createdAt": string,
    "updatedAt": string,
    "__v": number
}

Update Todo
PATCH /todos/:id
Request body:
{
    "title": string,
    "description": string
}

{
    "_id": string,
    "title": string,
    "description": string,
    "createdAt": string,
    "updatedAt": string,
    "__v": number
}

Delete Todo
DELETE /todos/:id
Response
{ "message": “Deleted successfully” }



Objeto de erro sempre vai seguir:

{ "message": string }
```