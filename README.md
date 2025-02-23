# Projeto de API com Fastify, Postgres e Redis

Este projeto é uma API desenvolvida utilizando Node.js e o micro-framework Fastify. A API oferece funcionalidades para inscrição em eventos, convites por meio de usuários inscritos, contabilização de cliques e ranking de usuários. Além disso, implementa integração com o banco de dados PostgreSQL e Redis para gerenciar dados de usuários e ranking.

## Tecnologias Utilizadas

- **Node.js**: Ambiente de execução para JavaScript no servidor.
- **Fastify**: Micro-framework para construção de APIs rápidas e eficientes.
- **Swagger**: Documentação interativa da API.
- **CORS**: Configuração para permitir acessos de diferentes endereços Web.
- **PostgreSQL**: Banco de dados relacional utilizado para armazenar os dados principais da aplicação.
- **Redis**: Banco de dados em memória utilizado para gerenciar o ranking da aplicação.
- **tsup**: Ferramenta para realizar o build da aplicação para deploy.

## Funcionalidades

### 1. **Configuração Inicial**
A aplicação foi iniciada com o Node.js, configurando o ambiente básico e as bibliotecas essenciais para a construção de uma API eficiente.

- **Fastify** foi configurado como o micro-framework principal da aplicação.
- **Swagger** foi integrado para gerar a documentação interativa da API.
- A aplicação foi configurada para aceitar requisições de outros endereços Web por meio de **CORS**.

### 2. **Conexão com Banco de Dados**
A API foi configurada para se conectar ao banco de dados **PostgreSQL** para armazenar dados de inscrições, usuários e eventos.

Além disso, o **Redis** foi integrado para gerenciar o ranking de usuários, permitindo armazenar e recuperar dados em memória de forma eficiente.

### 3. **Rotas de Inscrição e Convite**
- **Rota de inscrição**: Usuários podem se inscrever para o evento.
- **Rota de convite**: Usuários podem convidar outros para se inscrever por meio de um link único gerado.

### 4. **Funcionalidade de Ranking**
- As rotas foram atualizadas para incluir a funcionalidade de ranking, permitindo a consulta da posição do usuário no ranking, a quantidade de inscritos por indicação e a visualização geral do ranking.
- A rota de inscrição foi adaptada para permitir que um usuário se inscreva com base em um convite de outro inscrito, atualizando o ranking automaticamente.

### 5. **Preparação para Deploy**
A aplicação foi configurada para deploy utilizando **tsup**, realizando o build necessário para a produção.

## Como Rodar a Aplicação

### Requisitos

- Node.js (v14 ou superior)
- PostgreSQL
- Redis

### Passos

1. Clone o repositório:

    ```bash
    git clone https://github.com/seu-usuario/seu-repositorio.git
    cd seu-repositorio
    ```

2. Instale as dependências:

    ```bash
    npm install
    ```

3. Configure as variáveis de ambiente para o PostgreSQL e Redis. Crie um arquivo `.env` com as seguintes variáveis:

    ```bash
    DATABASE_URL=postgres://usuario:senha@localhost:5432/banco
    REDIS_URL=redis://localhost:6379
    ```

4. Execute a aplicação em modo de desenvolvimento:

    ```bash
    npm run dev
    ```

5. Acesse a API no navegador ou com uma ferramenta como o Postman. A documentação interativa do Swagger estará disponível em:

    ```
    http://localhost:3000/documentation
    ```

## Deploy

Para realizar o deploy da aplicação, utilize o comando de build:

```bash
npm run build

```
Em seguida, siga o processo de deploy adequado para o ambiente desejado, utilizando a versão construída da aplicação.

Contribuição
## Contribuições são bem-vindas! Se você deseja contribuir com este projeto, siga os seguintes passos:

- 1- Fork o repositório.
- 2- Crie uma nova branch (git checkout -b minha-feature).
- 3- Faça suas alterações.
- 4- Commit e envie suas alterações para o seu fork.
- 5- Abra um pull request explicando suas alterações.
