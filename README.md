# Introdução

Monetrix é um sistema de gerenciamento de finanças pessoais que oferece aos usuários funcionalidades robustas para manter o controle financeiro. A plataforma permite:

Criar conta de usuário: Registro de novos usuários com autenticação segura.
Criar lançamentos: Inserção de transações financeiras, como despesas, receitas e transferências.
Criar contas bancárias: Gerenciamento de múltiplas contas bancárias e carteiras.
Listar lançamentos: Visualização das transações financeiras realizadas, categorizadas por data ou tipo.
Visualizar saldo: Acompanhamento de saldo consolidado das contas bancárias.
Emitir relatórios: Geração de relatórios detalhados com base em filtros personalizados, como período, tipo de transação, e conta.

# Estrutura do Projeto

O Monetrix será construído e implantado usando Docker, garantindo uma infraestrutura consistente e facilitando a escalabilidade. O sistema será composto por um front-end em Vue.js, que se comunicará com o back-end desenvolvido em Node.js via GraphQL.

O PrismaServer gerenciará a conexão e as consultas diretas ao banco de dados PostgreSQL, enquanto o PrismaClient lidará com as requisições GraphQL no back-end, interagindo com o PrismaServer para obter e manipular dados.

## Front end

O front-end fornecerá uma interface amigável e dinâmica para interação com os dados financeiros dos usuários.

### Tecnologias e Ferramentas

- Vue.js: Framework JavaScript para construção de interfaces de usuário.
- Vue Router: Gerenciamento de rotas para navegação entre diferentes páginas do sistema.
- Vuetify: Biblioteca de componentes UI baseada em Material Design para Vue.js.
- Vuelidate: Biblioteca de validação de formulários.
- Apollo Client: Cliente para consumir a API GraphQL.
- Chart.js: Biblioteca para criação de gráficos dinâmicos e interativos.

### Principais Funcionalidades

- Interface gráfica dinâmica para criação e visualização de lançamentos e contas.
- Gráficos intuitivos para exibição de dados financeiros, como fluxo de caixa e saldo.
- Navegação fluida e responsiva entre páginas do sistema.

## Back end

O back-end será responsável por gerenciar as transações e a lógica de negócios, utilizando GraphQL para fornecer e manipular os dados de maneira eficiente e flexível.

### Tecnologias e Ferramentas

- API GraphQL: Interface para comunicação entre o front-end e o banco de dados.
- Prisma IO: ORM (Object-Relational Mapping) para manipulação de dados.
- GraphQL Yoga: Framework leve para construir servidores GraphQL.
- Auth JWT: Autenticação via JSON Web Tokens, garantindo segurança nas sessões dos usuários.
- Bcrypt: Para hashing seguro de senhas.
- Moment.js: Biblioteca para manipulação e formatação de datas.

### Principais Funcionalidades

- Autenticação e autorização de usuários.
- Operações CRUD (Criar, Ler, Atualizar, Excluir) para lançamentos e contas bancárias.
- Geração de relatórios personalizados com base nos filtros do usuário.
  Processamento de dados financeiros e cálculos, como saldos e totais.

## Banco de Dados

A aplicação utilizará PostgreSQL como banco de dados relacional, garantindo segurança e alta performance para lidar com grandes volumes de dados financeiros.

### Ferramentas

- PostgreSQL: Banco de dados relacional robusto e escalável.
- PrismaServer: Responsável pela conexão direta e execução de consultas no PostgreSQL.
- PrismaClient: Conectado ao PrismaServer para lidar com as operações de dados via GraphQL.

## Outras Ferramentas

Para garantir a consistência e automação no processo de build e deploy, serão utilizadas as seguintes ferramentas:

- Docker: Para encapsulamento e gerenciamento de containers.
- Docker Compose: Para orquestração de containers, facilitando o desenvolvimento e a manutenção do ambiente de produção.
