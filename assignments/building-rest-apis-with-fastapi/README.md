# 📘 Atividade: Building REST APIs with FastAPI

## 🎯 Objetivo

Aprenda a criar uma API REST com FastAPI, organizar endpoints HTTP e validar dados de entrada usando modelos Pydantic. Ao final, você terá uma API simples para gerenciar livros e poderá testá-la pela documentação interativa do FastAPI.

## 📝 Tarefas

### 🛠️ Criar o primeiro endpoint

#### Descrição
Configure uma aplicação FastAPI e crie uma rota simples para confirmar que a API está funcionando.

#### Requisitos
O programa concluído deve:

- Criar uma aplicação FastAPI executável com Uvicorn
- Implementar `GET /` retornando uma mensagem JSON de boas-vindas
- Implementar `GET /health` retornando um indicador de que a API está ativa


### 🛠️ Implementar operações para livros

#### Descrição
Amplie a aplicação para gerenciar livros. Use uma lista em memória como armazenamento; não é necessário configurar um banco de dados.

#### Requisitos
O programa concluído deve:

- Criar um modelo Pydantic para representar um livro com título, autor e ano de publicação
- Implementar `GET /books` para listar os livros e `GET /books/{book_id}` para buscar um livro pelo identificador
- Implementar `POST /books` para adicionar um livro e retornar o livro criado
- Implementar `DELETE /books/{book_id}` para remover um livro existente
- Retornar o status HTTP `404 Not Found` quando o identificador solicitado não existir


### 🛠️ Validar e testar a API

#### Descrição
Melhore a validação das entradas e verifique os endpoints usando a documentação interativa gerada pelo FastAPI ou testes automatizados.

#### Requisitos
O programa concluído deve:

- Rejeitar dados inválidos, como título ou autor vazio e ano de publicação fora de uma faixa plausível
- Retornar `201 Created` ao criar um livro e `204 No Content` ao removê-lo com sucesso
- Testar os fluxos de listar, criar, buscar, remover e tratar um identificador inexistente
- Confirmar que os endpoints e seus modelos aparecem corretamente em `/docs`
