# API de Produtos

CRUD de produtos com Node.js, Express e Mongoose.

## Estrutura

```text
src/
├── controllers/
│   └── productController.js
├── models/
│   └── Product.js
├── routes/
│   └── productRoutes.js
└── server.js
```

## Executar

```bash
npm install
cp .env.example .env
npm run dev
```

Copie `.env.example` para `.env` e configure `MONGODB_URI` com a string de conexão do MongoDB Atlas. Em produção, configure `PORT` e `MONGODB_URI` nas variáveis de ambiente do serviço.

## Rotas

| Método | Rota | Ação |
|---|---|---|
| GET | /produtos | Lista produtos |
| GET | /produtos/:id | Busca um produto |
| POST | /produtos | Cria um produto |
| PUT | /produtos/:id | Atualiza um produto |
| DELETE | /produtos/:id | Exclui um produto |

| GET | /produtos/buscar?termo=teclado | Busca por nome ou ID |

## Exemplo de JSON

```json
{
  "nome": "Teclado mecânico",
  "categoria": "Periféricos",
  "preco": 249.90,
  "estoque": 12
}
```
