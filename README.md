# n8n com Docker

Este projeto executa o [n8n](https://n8n.io/) usando Docker e Docker Compose. Ele utiliza um banco de dados PostgreSQL para persistência de dados.

## Serviços

- **n8n**: A aplicação principal do n8n.
- **postgres**: O banco de dados PostgreSQL.

## Configuração

1.  Crie um arquivo `.env` copiando o arquivo `.env.example`:
    ```bash
    cp .env.example .env
    ```
2.  Edite o arquivo `.env` e preencha as variáveis de ambiente necessárias:

    - `POSTGRES_DB`: O nome do banco de dados PostgreSQL.
    - `POSTGRES_USER`: O nome de usuário para o banco de dados PostgreSQL.
    - `POSTGRES_PASSWORD`: A senha para o banco de dados PostgreSQL.
    - `N8N_BASIC_AUTH_USER`: O nome de usuário para a autenticação básica do n8n.
    - `N8N_BASIC_AUTH_PASSWORD`: A senha para a autenticação básica do n8n.

## Como executar

1.  Certifique-se de que você tem o Docker e o Docker Compose instalados.
2.  Execute o seguinte comando para iniciar os serviços em segundo plano:
    ```bash
    docker-compose up -d
    ```

## Acessando o n8n

Quando os serviços estiverem em execução, você pode acessar o n8n em [http://localhost:5678](http://localhost:5678). Você será solicitado a fornecer as credenciais de autenticação básica que você configurou no arquivo `.env`.
