# Aplicação Node.js utilizando Nginx, Docker e MySQL.

## Descrição

Esse é um projeto de demonstração que consiste em um backend em Node.js com persistência de dados em um banco de dados MySQL, utilizando um proxy reverso com Nginx. Todo o ambiente é orquestrado usando Docker e Docker Compose para facilitar o desenvolvimento e a implantação. 

## Configuração

### Pré-requisitos

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Passos para Configuração

1. Clone o repositório:
    ```sh
    git clone https://github.com/BrenoFlaubert/node-api-with-nginx.git
    cd node
    ```

2. Crie um arquivo `.env` na raiz do projeto baseado no `.env.example`:
    ```sh
    cp .env.example .env
    ```

3. Preencha as variáveis de ambiente no arquivo `.env` com os valores apropriados:
    ```dotenv
    MYSQL_ROOT_PASSWORD=rootpassword
    MYSQL_DATABASE=mydatabase
    MYSQL_USER=root
    MYSQL_PASSWORD=rootpassword
    MYSQL_HOST=hostname
    ```

4. Instale as dependências do backend:
    ```sh
    cd node
    npm install
    cd ..
    ```

5. Inicie os serviços Docker:
    ```sh
    docker-compose up -d --build
    ```

## Licença

Este projeto está licenciado sob a MIT License. Consulte o arquivo [LICENSE](LICENSE) para obter mais detalhes.
