# API de Gerenciamento de Produtos

## Objetivo

Esta API tem como objetivo gerenciar produtos de uma loja ou sistema, permitindo a criação, listagem, atualização e remoção de produtos de forma fácil e segura.

## Funcionalidades

- **Criar produto**: Adiciona um novo produto ao sistema.
- **Listar produtos**: Exibe todos os produtos cadastrados.
- **Buscar produto por ID**: Retorna os detalhes de um produto específico.
- **Atualizar produto**: Altera as informações de um produto existente.
- **Deletar produto**: Remove um produto do sistema.

## Tecnologias Utilizadas

- **Linguagem:** Node.js (JavaScript)
- **Framework:** Express.js
- **Banco de Dados:** MongoDB (Mongoose)
- **Outros:** dotenv, nodemon (em desenvolvimento)

## Instalação

1. **Clone o repositório:**
   ```sh
   git clone https://github.com/seu-usuario/seu-repo.git
   cd seu-repo
   ```

2. **Instale as dependências:**
   ```sh
   npm install
   ```

3. **Configure as variáveis de ambiente:**
   - Crie um arquivo `.env` na raiz do projeto baseado no `.env.example` e ajuste as configurações (exemplo de conteúdo):
     ```
     MONGODB_URI=mongodb://localhost:27017/seubanco
     PORT=3000
     ```

4. **Inicie o servidor:**
   ```sh
   npm run dev
   ```
   O servidor estará rodando em `http://localhost:3000`.

## Endpoints e Exemplos de Uso

### 1. Criar Produto

- **Endpoint:** `POST /produtos`
- **Exemplo de requisição:**
  ```json
  {
    "nome": "Camiseta",
    "preco": 49.90,
    "descricao": "Camiseta de algodão",
    "estoque": 100
  }
  ```
- **Exemplo de resposta:**
  ```json
  {
    "id": "60d9f1a7b60e2b001c8d1234",
    "nome": "Camiseta",
    "preco": 49.9,
    "descricao": "Camiseta de algodão",
    "estoque": 100
  }
  ```

### 2. Listar Produtos

- **Endpoint:** `GET /produtos`
- **Exemplo de resposta:**
  ```json
  [
    {
      "id": "60d9f1a7b60e2b001c8d1234",
      "nome": "Camiseta",
      "preco": 49.9,
      "descricao": "Camiseta de algodão",
      "estoque": 100
    },
    {
      "id": "60d9f1a7b60e2b001c8d1235",
      "nome": "Calça Jeans",
      "preco": 89.9,
      "descricao": "Calça jeans azul",
      "estoque": 50
    }
  ]
  ```

### 3. Buscar Produto por ID

- **Endpoint:** `GET /produtos/{id}`
- **Exemplo de resposta:**
  ```json
  {
    "id": "60d9f1a7b60e2b001c8d1234",
    "nome": "Camiseta",
    "preco": 49.9,
    "descricao": "Camiseta de algodão",
    "estoque": 100
  }
  ```

### 4. Atualizar Produto

- **Endpoint:** `PUT /produtos/{id}`
- **Exemplo de requisição:**
  ```json
  {
    "nome": "Camiseta Premium",
    "preco": 59.90,
    "descricao": "Camiseta de algodão premium",
    "estoque": 90
  }
  ```
- **Exemplo de resposta:**
  ```json
  {
    "id": "60d9f1a7b60e2b001c8d1234",
    "nome": "Camiseta Premium",
    "preco": 59.9,
    "descricao": "Camiseta de algodão premium",
    "estoque": 90
  }
  ```

### 5. Deletar Produto

- **Endpoint:** `DELETE /produtos/{id}`
- **Exemplo de resposta:**
  ```json
  {
    "mensagem": "Produto removido com sucesso."
  }
  ```

## Contribuição

Contribuições são bem-vindas! Abra uma issue ou envie um pull request.

## Licença

Este projeto está sob a licença MIT.