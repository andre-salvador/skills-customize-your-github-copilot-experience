# 📘 Atividade: Data Persistence with SQLite

## 🎯 Objetivo

Aprenda a persistir dados em um banco SQLite usando o módulo `sqlite3` da biblioteca padrão do Python. Você vai substituir o armazenamento temporário em memória da API de livros por um banco de dados que mantém os registros entre reinicializações.

## 📝 Tarefas

### 🛠️ Criar o banco de dados e a tabela

#### Descrição
Crie uma conexão com um banco SQLite local e prepare a tabela que armazenará os livros da API.

#### Requisitos
O programa concluído deve:

- Conectar a um arquivo de banco de dados SQLite usando o módulo `sqlite3`
- Criar uma tabela `books` se ela ainda não existir, com identificador, título, autor e ano de publicação
- Inserir um livro de exemplo e consultar os registros para confirmar que a tabela funciona


### 🛠️ Implementar operações no banco

#### Descrição
Substitua as operações em memória por consultas ao SQLite para criar, listar, buscar e remover livros.

#### Requisitos
O programa concluído deve:

- Implementar operações para criar, listar, buscar por identificador e remover livros
- Usar consultas parametrizadas para inserir ou localizar valores fornecidos pelo usuário
- Tratar o caso em que um livro não existe, sem encerrar a aplicação com erro inesperado
- Fechar ou gerenciar corretamente as conexões e confirmar as alterações no banco


### 🛠️ Integrar SQLite à API FastAPI

#### Descrição
Atualize a API de livros criada na atividade de FastAPI para usar o banco SQLite. Reinicie o servidor durante os testes para verificar que os dados continuam disponíveis.

#### Requisitos
O programa concluído deve:

- Usar o banco SQLite nas rotas de listar, criar, buscar e remover livros
- Preservar os códigos HTTP apropriados, incluindo `404 Not Found` para livros inexistentes
- Confirmar que um livro criado permanece disponível após reiniciar a aplicação
- Demonstrar os endpoints atualizados por meio de `/docs` ou de testes automatizados
