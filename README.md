# Projeto Labook

### Tópicos
:small_blue_diamond: [Descrição do projeto](#descrição-do-projeto)

:small_blue_diamond: [Funcionalidades](#funcionalidades)

:small_blue_diamond: [Instruções](#instruções)

:small_blue_diamond: [Documentação](#documentação)

:small_blue_diamond: [Tecnologias Utilizadas](#tecnologias-utilizadas)

:small_blue_diamond: [Tarefas em aberto](#tarefas-em-aberto)


## Descrição do projeto

Uma jovem empreendedora teve uma ideia revolucionária que parece estar dando certo, mas está precisando de uma força para deixar o backend redondo.

O Labook é uma rede social com o objetivo de promover a conexão e interação entre seus mais diversos usuários. As pessoas poderão criar e curtir publicações.


## Funcionalidades

1. Cadastro de usuários
    - name, email e password devem ser do tipo string
    - name deve possuir ao menos 3 caracteres, enquanto password ao menos 6 caracteres
    - email deve ter um formato válido e único, não podendo repetir no banco de dados
    - Em caso de sucesso, retorna uma mensagem e um token de acesso que guarda o id e a role da pessoa (NORMAL ou ADMIN)
  
2. Login de usuários
    - email e password devem ser fornecidos e serem do tipo string
    - password deve possuir ao menos 6 caracteres
    - email deve ter um formato válido
    - O usuário com o e-mail fornecido deve existir no sistema
    - Em caso de sucesso, retorna uma mensagem  e um token de acesso
    
3. Criar post
    - Endpoint protegido: caso tentem acessá-lo sem token, deve ser retornada uma mensagem de erro
    - content deve possuir no mínimo 1 caractere
    
4. Deletar post
    - Endpoint protegido: caso tentem acessá-lo sem token, deve ser retornada uma mensagem de erro
    - ADMINS podem deletar qualquer post, equanto contas NORMAIS só podem deletar seus próprios posts
    - id do post a ser deletado deve existir no sistema
    
5. Dar like em post
    - Uma mesma pessoa não pode dar mais de um like em um post
    - id do post deve existir no sistema
    - se o post já estiver com um like do usuário, é retornado um erro

6. Remover like de um post
    - id do post deve existir no sistema
    - se o post não estiver com o like do usuário, é retornado um erro
    
7. Ver todos os posts
    - Endpoint protegido: caso tentem acessá-lo sem token, deve ser retornada uma mensagem de erro
    - dentre as informações dos posts, deve existir também o número de likes de cada um
    
## Instruções

### Instalando as dependências:
-   `npm install`:
    Instala todas as dependências listadas no `package.json`.

### Criando o arquivo .env:

Criar o arquivo `.env` e configurar com as informações de seu banco de dados.

```
DB_HOST = host
DB_USER = usuario
DB_PASS = senha
DB_NAME = nome-do-banco-de-dados
JWT_KEY = "minha-senha-segura"
JWT_EXPIRES_IN = "1h"
BCRYPT_COST = 12
```

### Executar o projeto:

-   `npm run dev:`
    Estabelece a conexão com o banco de dados e reinicia automaticamente o servidor `localhost` toda a vez que o projeto for alterado e salvo.

### Criando e populando as tabelas

Acessar o arquivo `tables.sql` e executar os comandos de criação das tabelas `Labook_Users`, `Labook_Posts` e `Labook_Likes`, respectivamente.

Popular as tabelas através das requisições do Postman ou do arquivo `requests.rest` da aplicação.

## Documentação
  - [Postman](https://documenter.getpostman.com/view/21556158/2s8ZDVZ3rK)
  
## Tecnologias utilizadas
  -   NodeJS
  -   TypeScript
  -   MySQL
  -   Knex
  -   Express
  -   Cors
  -   JWT
  -   UUID
  -   BcryptJS
  -   Markdown
  
## Tarefas em aberto
:memo: Cobertura de testes automatizados

:memo: Deploy do backend
  
## Autora
 [**Andressa Darzé**](https://github.com/andressadarze) - Desenvolvedora Web Full-Stack
 
 
 [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/andressadarze)



