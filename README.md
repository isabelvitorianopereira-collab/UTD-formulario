# 📋 Gerenciamento de Clientes — CRUD

Projeto final do curso de **Desenvolvimento de Interfaces Web com JavaScript** da **UTD**.

Aplicação web completa para gerenciamento de clientes, com operações de **criar, visualizar, editar e excluir** registros (CRUD), utilizando React no frontend e Node.js com Sequelize no backend.

---

## 🚀 Funcionalidades

- ➕ Cadastro de novos clientes
- 👁️ Listagem e visualização de clientes
- ✏️ Edição de dados de um cliente
- 🗑️ Exclusão de clientes

---

## 🛠️ Tecnologias Utilizadas

### Frontend
- [React](https://react.dev/) — biblioteca para construção da interface
- JavaScript (ES6+)
- Vite (porta padrão: `5173`)

### Backend
- [Node.js](https://nodejs.org/)
- [Express](https://expressjs.com/) — framework para a API REST
- [Sequelize](https://sequelize.org/) — ORM para comunicação com o banco de dados
- [MySQL2](https://www.npmjs.com/package/mysql2) — driver do banco de dados
- [CORS](https://www.npmjs.com/package/cors) — controle de acesso entre origens

---

## 📁 Estrutura do Projeto

```
backend/
└── app/
    ├── config/
    │   ├── db.config.js      # Configuração da conexão com o banco (Sequelize)
    │   └── env.js            # Variáveis de ambiente (host, usuário, senha, banco)
    ├── models/
    │   └── cliente.model.js  # Model da tabela de clientes
    ├── routes/
    │   └── route.js          # Definição das rotas da API
    ├── servicos/
    │   └── servico.js        # Lógica das operações CRUD
    ├── package.json
    └── server.js             # Ponto de entrada do servidor
```

---

## ⚙️ Como Executar o Projeto

### Pré-requisitos

- Node.js instalado
- MySQL em execução
- Um banco de dados criado (conforme configurado em `env.js`)

### Backend

```bash
# Acesse a pasta do backend
cd backend/app

# Instale as dependências
npm install

# Inicie o servidor
npm start
```

O servidor irá rodar em: `http://localhost:8080`

> ⚠️ Ao iniciar, o Sequelize recria a tabela automaticamente (`force: true`) e insere alguns clientes de exemplo.

### Frontend

```bash
# Acesse a pasta do frontend
cd frontend

# Instale as dependências
npm install

# Inicie a aplicação
npm run dev
```

A aplicação estará disponível em: `http://localhost:5173`

---

## 🔌 Endpoints da API

| Método | Rota                  | Descrição                    |
|--------|-----------------------|------------------------------|
| POST   | `/api/cliente`        | Cria um novo cliente         |
| GET    | `/api/clientes`       | Lista todos os clientes      |
| GET    | `/api/cliente/:id`    | Busca um cliente pelo ID     |
| PUT    | `/api/cliente`        | Atualiza um cliente          |
| DELETE | `/api/cliente/:id`    | Remove um cliente pelo ID    |

---

## 🗄️ Model do Cliente

| Campo  | Tipo    | Descrição          |
|--------|---------|--------------------|
| id     | INTEGER | Chave primária (auto increment) |
| nome   | STRING  | Nome do cliente    |
| idade  | INTEGER | Idade do cliente   |
| email  | STRING  | E-mail do cliente  |

---

## 📄 Licença

Este projeto foi desenvolvido para fins acadêmicos — **UTD, Curso de Desenvolvimento de Interfaces Web com JavaScript**.
