# insper.api.docs

## Membros do Grupo:
- Marcelo Rabello Barranco
- Pedro Antonio Silva

## API de Documentação de Projetos

Este repositório serve para documentar os projetos de API e Microserviços.

Nosso objetivo é criar um "Duolingo da Culinária" para ensinar receitas de forma interativa e divertida.

## Partes do nosso projeto:

### [Docker-api](https://github.com/P-ASilva/insper.api.docker-api.git)
Este repositório contém a configuração Docker Compose que define e gerencia os contêineres Docker utilizados pelos diversos microserviços. Ele simplifica a orquestração e implantação dos serviços em ambientes de desenvolvimento e produção, garantindo consistência e facilidade de gerenciamento.

- **Principais Arquivos:**
  - `docker-compose.yaml`: Define a configuração dos contêineres, redes e volumes.
  - `.gitignore`: Lista de arquivos e diretórios ignorados pelo Git.
  - `README.md`: Documentação inicial do repositório.

### [Auth-resource](https://github.com/P-ASilva/insper.api.auth-resource.git)
Fornece endpoints RESTful para autenticação e autorização de usuários. Este microserviço lida com a criação e validação de tokens de autenticação, assegurando que apenas usuários autenticados possam acessar recursos protegidos.

- **Principais Funcionalidades:**
  - Login de usuários.
  - Validação de tokens JWT.
  - Registro de novos usuários.

### [Auth](https://github.com/P-ASilva/insper.api.auth.git)
Implementa a lógica central de autenticação e autorização, incluindo a geração e verificação de tokens JWT. Integra com o banco de dados para armazenar informações de usuários e permissões.

- **Principais Funcionalidades:**
  - Gerenciamento de sessões de usuários.
  - Controle de acesso baseado em permissões.

### [Account-resource](https://github.com/P-ASilva/insper.api.account-resource.git)
Gerencia as operações relacionadas às contas dos usuários, fornecendo endpoints para criação, atualização e exclusão de contas.

- **Principais Funcionalidades:**
  - Criação de novas contas de usuário.
  - Atualização de informações de perfil.
  - Exclusão de contas.

### [Account](https://github.com/P-ASilva/insper.api.account.git)
Contém a lógica de negócios para manipulação de contas de usuários. Conecta-se ao banco de dados para realizar operações CRUD (Create, Read, Update, Delete) nas contas.

- **Principais Funcionalidades:**
  - Persistência de dados de contas.
  - Validação de dados de entrada.

### [Ingredientes-resource](https://github.com/Maraba23/insper.api.ingredientes-resource.git)
Fornece endpoints para gerenciar ingredientes, permitindo que os usuários adicionem, atualizem e consultem ingredientes.

- **Principais Funcionalidades:**
  - Adição de novos ingredientes.
  - Atualização de detalhes de ingredientes.
  - Consulta de lista de ingredientes disponíveis.

### [Ingredientes](https://github.com/Maraba23/insper.api.ingredientes.git)
Implementa a lógica de negócios para o gerenciamento de ingredientes, incluindo validação e persistência de dados no banco de dados.

- **Principais Funcionalidades:**
  - Validação de dados de ingredientes.
  - Persistência e recuperação de informações de ingredientes.

### [Receitas-resource](https://github.com/P-ASilva/insper.api.receitas-resource.git)
Disponibiliza endpoints para a gestão de receitas culinárias, permitindo que os usuários criem, atualizem e visualizem receitas.

- **Principais Funcionalidades:**
  - Criação de novas receitas.
  - Atualização de receitas existentes.
  - Consulta de receitas detalhadas.

### [Receitas](https://github.com/P-ASilva/insper.api.receitas.git)
Contém a lógica de negócios e persistência de dados para receitas, assegurando que as receitas sejam armazenadas e recuperadas corretamente.

- **Principais Funcionalidades:**
  - Validação de receitas.
  - Persistência de receitas no banco de dados.

### [Gateway](https://github.com/Maraba23/insper.api.gateway.git)
Atua como um ponto central de entrada para todas as solicitações, roteando-as para os microserviços apropriados e gerenciando a comunicação entre eles.

- **Principais Funcionalidades:**
  - Roteamento de requisições.
  - Balanceamento de carga.
  - Autenticação e autorização centralizadas.

### [Discovery](https://github.com/Maraba23/insper.api.discovery.git)
Responsável pela descoberta de serviços, permitindo que os microserviços se registrem e descubram uns aos outros dinamicamente.

- **Principais Funcionalidades:**
  - Registro de serviços.
  - Descoberta de serviços.

### [Ops](https://github.com/P-ASilva/insper.api.ops.git)
Gerencia as operações e a infraestrutura da API, incluindo monitoramento, logging e automação de deploys.

- **Principais Funcionalidades:**
  - Monitoramento de performance.
  - Logging centralizado.
  - Scripts de automação para deploy.

### [Front-end](https://github.com/Maraba23/insper.api.frontend)
Interface de usuário para interagir com a API, permitindo que os usuários visualizem receitas, ingredientes e contas, além de criar e atualizar suas próprias receitas.

- **Principais Funcionalidades:**
  - Visualização de receitas.
  - Adição de ingredientes.
  - Criação de novas receitas.

## Documentação das rotas:
Nossa documentação se encontra em SpringDocs (Swagger)
