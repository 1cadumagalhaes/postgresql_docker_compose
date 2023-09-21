# Instância PostgreSQL com pgAdmin usando Docker Compose

Este repositório contém um exemplo de como configurar uma instância PostgreSQL com pgAdmin usando Docker Compose.

## Pré-requisitos

- Docker
- Docker Compose

## Executando a aplicação

1. Clone este repositório:

```
git clone https://github.com/1cadumagalhaes/postgresql_docker_compose.git
```

2. Navegue até o repositório clonado:

```
cd postgresql-pgadmin-docker-compose
```

3. Execute o seguinte comando para iniciar a instância PostgreSQL e o pgAdmin:

```
docker-compose up
```

4. Acesse o pgAdmin abrindo um navegador da web e navegando até `http://localhost:16543`. Faça login com o e-mail e a senha especificados no arquivo `docker-compose.yml`.

## Personalizando a aplicação

Você pode personalizar a aplicação alterando as variáveis de ambiente no arquivo `docker-compose.yml`. As seguintes variáveis de ambiente estão disponíveis:

- `POSTGRES_USER`: O nome de usuário para a instância PostgreSQL. O padrão é `postgres`.
- `POSTGRES_PASSWORD`: A senha para a instância PostgreSQL. O padrão é `postgres`.
- `PGADMIN_DEFAULT_EMAIL`: O endereço de e-mail para o usuário pgAdmin. O padrão é `teste@teste.com`.
- `PGADMIN_DEFAULT_PASSWORD`: A senha para o usuário pgAdmin. O padrão é `teste`.

## Acessando o banco de dados PostgreSQL

1. Faça login no pgAdmin abrindo um navegador da web e navegando até `http://localhost:16543`.

2. Clique no item `Servers` na barra lateral esquerda.
3. Esta janela deve abrir pedindo a senha do banco de dados:
![Password popup](./pg_admin_password.png)
4. Insira a senha especificada na variável de ambiente POSTGRES_PASSWORD no arquivo `docker-compose.yml` e clique em `OK`.