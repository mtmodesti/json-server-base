# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.


### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"
Os usuários cadastrados na API tem autorização para inserir novos jogos ou novos filmes nas rotas que serão mostradas
a seguir

### Rotas

GET - /movies
Essa rota lista todos os filmes cadastros. Não é neessário nenhuma autorização

POST - /movies 
Você pode cadastrar um novo filme na API. É recomendado usar os seguintes campos:

"name": "Nome do filme",
"year": ano do filme,
"userId": id do usuário que fara o post

GET - /games  
Essa rota lista todos os games cadastros. Não é neessário nenhuma autorização

POST - /games
Você pode cadastrar um novo filme na API. É recomendado usar os seguintes campos:
"name" : "Nome do Jogo",
"type" : "Estilo do jogo. Por exemplo: RPG",
"userId" : id do usuário que fará o post

