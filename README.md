
# Digital Store API

API REST desenvolvida com **Node.js, Express, Prisma ORM e SQLite** para gerenciamento de produtos da Digital Store.

## Tecnologias utilizadas

- Node.js
- Express.js
- Prisma ORM 6
- SQLite
- Swagger (OpenAPI 3.0)
- CORS
- dotenv

## Funcionalidades

A API permite realizar operações CRUD de produtos:

| Método | Endpoint | Descrição |
|---|---|---|
| GET | `/api/products` | Listar todos os produtos |
| GET | `/api/products/:id` | Buscar produto por ID |
| POST | `/api/products` | Cadastrar um produto |
| PUT | `/api/products/:id` | Atualizar um produto |
| DELETE | `/api/products/:id` | Excluir um produto |

A API possui validação dos dados e tratamento de erros HTTP, incluindo 400 para dados inválidos e 404 para produtos não encontrados.

## Pré-requisitos

- Node.js instalado
- npm instalado

## Instalação

Clone o repositório:

```bash
git clone https://github.com/Milliena/digital-store-backend.git
```

Entre na pasta do projeto:

```bash
cd digital-store-backend
```

Instale as dependências:

```bash
npm install
```

## Configuração do banco de dados

Crie um arquivo `.env` na raiz do projeto:

```env
DATABASE_URL="file:./dev.db"
```

Execute as migrações:

```bash
npx prisma migrate deploy
```

Gere o Prisma Client:

```bash
npx prisma generate
```

## Executando o servidor

```bash
npm run dev
```

A API estará disponível em:

http://localhost:3000/api/products

## Documentação Swagger

Com o servidor em execução, acesse:

http://localhost:3000/api-docs/

## Exemplo de cadastro

Requisição: `POST /api/products`

Corpo JSON:

```json
{
  "name": "Tenis Nike",
  "price": 299.90,
  "category": "Calcados"
}
```

## Estrutura do projeto

```text
backend/
├── prisma/
│   ├── migrations/
│   └── schema.prisma
├── src/
│   ├── config/
│   │   └── swagger.js
│   ├── controllers/
│   │   └── productController.js
│   ├── middlewares/
│   ├── routes/
│   │   ├── index.js
│   │   └── productRoutes.js
│   ├── services/
│   │   └── productService.js
│   ├── app.js
│   └── main.js
├── .gitignore
├── package.json
└── prisma.config.ts
```

**Observação:** o arquivo `.env` e o banco de dados SQLite local não são enviados ao GitHub. O banco pode ser criado usando as migrações do Prisma.

## Integrantes do grupo

- Camile Araújo Alexandre
- Jamyle Pereira da Silva

Projeto desenvolvido em equipe por Mile e Jamyle em 2026.
