# Toughts

Rede social simples para compartilhar pensamentos. Projeto em Node.js com arquitetura MVC.

## Funcionalidades
- Cadastro, login e logout (senhas com hash via bcrypt)
- Dashboard para criar, editar e remover seus pensamentos
- Página inicial pública com busca e ordenação

## Tecnologias
Node.js · Express 5 · Handlebars · Sequelize · MySQL · express-session

## Estrutura
```
controllers/   lógica das rotas (Auth e Toughts)
db/            conexão com o MySQL
helpers/       middleware de autenticação
models/        modelos Sequelize (User, Tought)
routes/        rotas de autenticação e pensamentos
views/         templates Handlebars
public/        arquivos estáticos (CSS, imagens)
```

## Como rodar
1. Inicie um MySQL local (ex.: XAMPP) e crie o banco:
   ```sql
   CREATE DATABASE toughts;
   ```
2. Ajuste usuário e senha em `db/conn.js` se necessário (padrão: `root`, sem senha)
3. Instale as dependências:
   ```bash
   npm install
   ```
4. Inicie o servidor:
   ```bash
   npm start
   ```
5. Acesse http://localhost:3000

As tabelas são criadas automaticamente na primeira execução.
