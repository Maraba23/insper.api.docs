# insper.api.docs

## API de Documentação de Projetos

- Esse repoitorio serve para documentar os projetos de API e Microserviços.

Nosso objetivo é criar um "Duolingo da Culinaria" para ensinar receitas de forma interativa e divertida.

## Partes do nosso projeto:

- [Docker-api](https://github.com/P-ASilva/insper.api.docker-api.git)
- [Auth-resource](https://github.com/P-ASilva/insper.api.auth-resource.git)
- [Auth](https://github.com/P-ASilva/insper.api.auth.git)
- [Account-resource](https://github.com/P-ASilva/insper.api.account-resource.git)
- [Account](https://github.com/P-ASilva/insper.api.account.git)
- [Ingredientes-resource](https://github.com/Maraba23/insper.api.ingredientes-resource.git)
- [Ingredientes](https://github.com/Maraba23/insper.api.ingredientes.git)
- [Receitas-resource](https://github.com/P-ASilva/insper.api.receitas-resource.git)
- [Receitas](https://github.com/P-ASilva/insper.api.receitas.git)
- [Gateway](https://github.com/Maraba23/insper.api.gateway.git)
- [Discovery](https://github.com/Maraba23/insper.api.discovery.git)

---

# Ingrediente API

A API `Ingrediente` gerencia operações CRUD (Create, Read, Update, Delete) para ingredientes.

## Endpoints

### Criar Ingrediente

- **Método HTTP**: `POST`
- **Endpoint**: `/ingredientes`
- **Corpo da Requisição** (`RequestBody`): `IngredienteIn`
  - **Descrição**: Objeto contendo as informações do ingrediente a ser criado.
  - **Obrigatório**: Sim
- **Resposta** (`ResponseEntity<IngredienteOut>`): Retorna o ingrediente criado.

### Atualizar Ingrediente

- **Método HTTP**: `PUT`
- **Endpoint**: `/ingredientes/{id}`
- **Path Variable** (`@PathVariable`): `id`
  - **Descrição**: ID do ingrediente a ser atualizado.
  - **Obrigatório**: Sim
- **Corpo da Requisição** (`RequestBody`): `IngredienteIn`
  - **Descrição**: Objeto contendo as novas informações do ingrediente.
  - **Obrigatório**: Sim
- **Resposta** (`ResponseEntity<IngredienteOut>`): Retorna o ingrediente atualizado.

### Ler Ingrediente

- **Método HTTP**: `GET`
- **Endpoint**: `/ingredientes/{id}`
- **Path Variable** (`@PathVariable`): `id`
  - **Descrição**: ID do ingrediente a ser lido.
  - **Obrigatório**: Sim
- **Resposta** (`ResponseEntity<IngredienteOut>`): Retorna o ingrediente solicitado.

### Ler Todos os Ingredientes

- **Método HTTP**: `GET`
- **Endpoint**: `/ingredientes`
- **Resposta** (`ResponseEntity<IngredienteOut>`): Retorna todos os ingredientes.

### Deletar Ingrediente

- **Método HTTP**: `DELETE`
- **Endpoint**: `/ingredientes/{id}`
- **Path Variable** (`@PathVariable`): `id`
  - **Descrição**: ID do ingrediente a ser deletado.
  - **Obrigatório**: Sim
- **Resposta** (`ResponseEntity<IngredienteOut>`): Confirmação da remoção do ingrediente.

---

# Receitas API

A API `Receitas` permite a criação, atualização, leitura e listagem de receitas.

## Endpoints

### Criar Receita

- **Método HTTP**: `POST`
- **Endpoint**: `/receitas`
- **Corpo da Requisição** (`RequestBody`): `ReceitaIn`
  - **Descrição**: Objeto contendo as informações da receita a ser criada.
  - **Obrigatório**: Sim
- **Resposta** (`ResponseEntity<ReceitaOut>`): Retorna a receita criada com seu respectivo ID e demais informações.

### Listar Todas as Receitas

- **Método HTTP**: `GET`
- **Endpoint**: `/receitas`
- **Resposta** (`ResponseEntity<List<ReceitaOut>>`): Retorna uma lista de todas as receitas disponíveis, incluindo seus IDs e informações relevantes.

### Obter Receita por ID

- **Método HTTP**: `GET`
- **Endpoint**: `/receitas/{id}`
- **Path Variable** (`@PathVariable`): `id`
  - **Descrição**: ID da receita a ser obtida.
  - **Obrigatório**: Sim
- **Resposta** (`ResponseEntity<ReceitaOut>`): Retorna a receita solicitada, incluindo seu ID e todas as informações pertinentes.

### Atualizar Receita

- **Método HTTP**: `PUT`
- **Endpoint**: `/receitas/{id}`
- **Path Variable** (`@PathVariable`): `id`
  - **Descrição**: ID da receita a ser atualizada.
  - **Obrigatório**: Sim
- **Corpo da Requisição** (`RequestBody`): `ReceitaIn`
  - **Descrição**: Objeto contendo as novas informações da receita.
  - **Obrigatório**: Sim
- **Resposta** (`ResponseEntity<ReceitaOut>`): Retorna a receita atualizada com as novas informações fornecidas.

---

# Account API

A API `Account` facilita a criação, atualização, leitura e autenticação de contas de usuário.

## Endpoints

### Criar Conta

- **Método HTTP**: `POST`
- **Endpoint**: `/accounts`
- **Corpo da Requisição** (`RequestBody`): `AccountIn`
  - **Descrição**: Objeto contendo as informações da conta a ser criada.
  - **Obrigatório**: Sim
- **Resposta** (`ResponseEntity<AccountOut>`): Retorna a conta criada, incluindo detalhes como ID da conta e informações do usuário.

### Ler Conta

- **Método HTTP**: `GET`
- **Endpoint**: `/accounts`
- **Cabeçalhos da Requisição**:
  - `id-user`: ID do usuário cuja conta está sendo acessada.
    - **Obrigatório**: Sim
  - `role-user`: Papel do usuário (por exemplo, administrador, usuário regular).
    - **Obrigatório**: Sim
- **Resposta** (`ResponseEntity<AccountOut>`): Retorna detalhes da conta do usuário, baseando-se nos cabeçalhos de requisição fornecidos.

### Login

- **Método HTTP**: `POST`
- **Endpoint**: `/accounts/login`
- **Corpo da Requisição** (`RequestBody`): `LoginIn`
  - **Descrição**: Objeto contendo as credenciais do usuário para login.
  - **Obrigatório**: Sim
- **Resposta** (`ResponseEntity<AccountOut>`): Retorna detalhes da conta do usuário após a autenticação bem-sucedida.

### Atualizar Conta

- **Método HTTP**: `PUT`
- **Endpoint**: `/accounts/{id}`
- **Path Variable** (`@PathVariable`): `id`
  - **Descrição**: ID da conta a ser atualizada.
  - **Obrigatório**: Sim
- **Corpo da Requisição** (`RequestBody`): `AccountIn`
  - **Descrição**: Objeto contendo as novas informações da conta.
  - **Obrigatório**: Sim
- **Resposta** (`ResponseEntity<AccountOut>`): Retorna a conta atualizada, incluindo as novas informações fornecidas.
