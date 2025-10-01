# Desafio Técnico - Desenvolvedor(a) Front- End (Vue.js)

Bem-vindo(a)!
Neste desafio queremos avaliar sua habilidade para projetar e resolver problemas com Vue.js. Foque em clareza, organização e funcionamento correto das regras de negócio abaixo. Assim como um sistema responsível e que seja acessível a todas as telas.

---

### 📌 Contexto

Você deverá desenvolver uma aplicação em Vue 3 que simula o gerenciamento de produtos.

O sistema possui dois tipos de usuários:

- Admin

- Tenant

O login é feito pelo mesmo endpoint, e a resposta da API retorna o tipo de usuário (admin ou tenant).
Com base nisso, a aplicação deve configurar automaticamente o prefixo das requisições:

- Admin → GET /admin/products

- Tenant → GET /tenant/products

Após o login, ambos os usuários serão redirecionados para a rota /produtos.

---

### 🔑 Funcionalidades

O usuário deve poder:

- Listar produtos (GET)
- Criar produtos (POST)
- Editar produtos (PUT)
- Excluir produtos (DELETE)

Mas só o usuário ADMIN pode:
- Editar status do produto

### ↘️ Fluxo do sistema

1. Tela de Cadastro
2. Tela de Login
3. Tela de Produtos contendo:

   - Uma tabela listando os produtos

   - Botão "Novo Produto"

   - Botão "Editar" em cada linha da tabela

   - Botão "Excluir" em cada linha da tabela

   - Botão toggle em cada linha da tabela que ativa ou desativa o status do produto (vísivel apenas para o ADMIN)

   - Todas as operações de CRUD devem atualizar a tabela em tempo real

---

### 📦 API Fake

Utilize o json-server para simular o back-end.
Estrutura de exemplo (db.json)

```json
{
  "admin": {
    "products": [
      {
        "id": 1,
        "name": "Notebook",
        "price": 3500,
        "image": "",
        "description": "",
        "status": "activated"
      },
      {
        "id": 2,
        "name": "Monitor",
        "price": 1500,
        "image": "",
        "description": "",
        "status": "disabled"
      }
    ]
  },
  "tenant": {
    "products": [
      {
        "id": 1,
        "name": "Mouse",
        "price": 150,
        "image": "",
        "description": "",
        "status": "activated"
      },
      {
        "id": 2,
        "name": "Teclado",
        "price": 250,
        "image": "",
        "description": "",
        "status": "disabled"
      }
    ]
  },
  "login": [
    {
      "id": 1,
      "email": "admin@test.com",
      "password": "123",
      "role": "admin",
      "token": "token-admin"
    },
    {
      "id": 2,
      "email": "tenant@test.com",
      "password": "123",
      "role": "tenant",
      "token": "token-tenant"
    }
  ]
}
```

---

### 🛠️ Requisitos técnicos obrigatórios

- Vue 3 + Vite

- Vue Router para navegação

- TanStack Query para requisições assíncronas

- Axios para comunicação com a API

- PrimeVue para UI (DataTable, Dialog, InputText, Button, Toast)

- JSON server

---

### ⚡ Avisos:

- Estruture bem as camadas de autenticação, store e hooks de requisições para que a troca entre admin e tenant seja simples e escalável.
- Não esqueça da responsividade
- O layout das telas fica a seu critério.
