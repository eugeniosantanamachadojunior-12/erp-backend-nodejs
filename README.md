🚀 Sistema ERP Backend Corporativo — Node.js + Express + MySQL

Sistema ERP backend completo desenvolvido em Node.js, simulando ambiente corporativo real, com controle transacional de vendas, gestão automática de estoque, auditoria, relatórios gerenciais, dashboard executivo e autenticação JWT.

Projeto construído com arquitetura utilizada em sistemas empresariais como Totvs, Omie e SAP Business One.

🧠 Visão Geral

Este projeto implementa o núcleo de um ERP moderno, aplicando regras de negócio reais de sistemas comerciais:

Processamento seguro de vendas

Controle automático de estoque

Rastreabilidade de movimentações

Relatórios gerenciais

Dashboard executivo

Segurança com autenticação JWT

Desenvolvido com foco em arquitetura, integridade de dados e boas práticas de engenharia de software.

🏗️ Arquitetura

Arquitetura em camadas (MVC):

Node.js + Express
        ↓
Controllers (Regras de negócio)
        ↓
MySQL (Transacional ACID)


Estrutura de pastas:

src/
 ├─ config/
 ├─ controllers/
 ├─ routes/
 ├─ middlewares/

⚙️ Tecnologias

Node.js

Express.js

MySQL

mysql2 (Promise)

JWT (jsonwebtoken)

bcryptjs

Arquitetura MVC

Git/GitHub

📦 Módulos Implementados
Módulo	Descrição
Clientes	CRUD completo
Produtos	CRUD completo
Pedidos	Venda transacional
Itens do pedido	Relacionamento N:N
Estoque automático	Baixa e reversão
Auditoria de estoque	Movimentações
Relatórios	Vendas por período
Dashboard	KPIs e gráficos
Autenticação	JWT
Segurança	Middleware de proteção
🔄 Fluxo de Venda (Transacional)

Inicia transação MySQL

Cria pedido PENDENTE

Bloqueia produtos (FOR UPDATE)

Valida estoque

Insere itens

Baixa estoque

Atualiza total

Confirma pedido

Commit

Em caso de erro → Rollback automático

📊 Dashboard Executivo

Endpoints disponíveis:

GET /dashboard/resumo

GET /dashboard/vendas-diarias

GET /dashboard/top-produtos

Fornecem indicadores para tomada de decisão gerencial.

🔐 Segurança

Senhas criptografadas com bcrypt

Autenticação via JWT

Middleware de proteção de rotas

Fluxo de autenticação:

Registro → /auth/register

Login → /auth/login

Recebe token JWT

Envia token no header Authorization: Bearer TOKEN

🧪 Exemplo de Requisição

Criação de pedido:

POST /pedidos

{
  "cliente_id": 1,
  "itens": [
    { "produto_id": 2, "quantidade": 3 }
  ]
}

🗄️ Modelagem de Dados

Principais tabelas:

clientes

produtos

pedidos

itens_pedido

movimentacoes_estoque

usuarios

🚀 Como Executar
npm install
node server.js


Servidor disponível em:

http://localhost:3000

👨‍💻 Autor

Eugenio Santana Machado

Projeto desenvolvido como sistema ERP completo para portfólio profissional.

🎯 Objetivo do Projeto

Demonstrar domínio prático em:

Backend corporativo

Sistemas transacionais

Arquitetura de software

Segurança de APIs

Este projeto simula o núcleo de sistemas utilizados por empresas reais.
