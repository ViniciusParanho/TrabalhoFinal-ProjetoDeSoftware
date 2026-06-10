# 🔧 Sistema de Gestão de Oficina Mecânica (SGOM) 👨‍💻

> Sistema web para gerenciamento completo de oficinas mecânicas, cobrindo agendamentos, ordens de serviço, controle de clientes, veículos e pagamentos.

---

## 🚧 Status do Projeto

![Versão](https://img.shields.io/badge/Versão-v1.0.0-blue)
![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow)
![Licença](https://img.shields.io/badge/Licença-MIT-green)
![React](https://img.shields.io/badge/React-18.x-007ec6?logo=react&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-20.x-007ec6?logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-007ec6?logo=postgresql&logoColor=white)

---

## 📚 Índice

- [Links Úteis](#-links-úteis)
- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades Principais](#-funcionalidades-principais)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Arquitetura](#-arquitetura)
- [Instalação e Execução](#-instalação-e-execução)
- [Estrutura de Pastas](#-estrutura-de-pastas)
- [Documentações utilizadas](#-documentações-utilizadas)
- [Autores](#-autores)
- [Agradecimentos](#-agradecimentos)
- [Licença](#-licença)

---

## 🔗 Links Úteis

- 📁 **Repositório:** [github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware)
- 🗂️ **Diagramas PlantUML:** [/Diagramas](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas)
- 🌐 **PlantUML Online:** [plantuml.com](https://plantuml.com)

---

## 📝 Sobre o Projeto

O **Sistema de Gestão de Oficina Mecânica (SGOM)** foi desenvolvido como projeto acadêmico da disciplina **Projeto de Software** do curso de Engenharia de Software da PUC Minas.

O sistema resolve um problema real e recorrente em pequenas e médias oficinas mecânicas: a dependência de processos manuais (papel, planilhas, WhatsApp) para controlar agendamentos, ordens de serviço e pagamentos, o que gera perda de informações, retrabalho e baixa qualidade no atendimento ao cliente.

O SGOM oferece uma plataforma web centralizada que permite:
- **Clientes** agendarem serviços e acompanharem o status de seus veículos.
- **Atendentes** gerenciarem o fluxo completo de atendimento, do cadastro ao pagamento.
- **Mecânicos** consultarem e atualizarem as ordens de serviço sob sua responsabilidade.
- **Gerentes** acessarem relatórios e administrarem a operação da oficina.

O projeto é fictício, com dados simulados, e tem como objetivo demonstrar boas práticas de arquitetura, modelagem e documentação de software.

---

## ✨ Funcionalidades Principais

- 📅 **Agendamento Online:** Clientes solicitam e confirmam agendamentos com geração de protocolo.
- 🔧 **Gestão de Ordens de Serviço:** Abertura, acompanhamento e encerramento de OS com cálculo automático de valor.
- 👤 **Cadastro de Clientes e Veículos:** Registro completo com CPF, placa e histórico de atendimentos.
- 💳 **Registro de Pagamentos:** Suporte a múltiplas formas de pagamento com emissão de recibo.
- 📊 **Relatórios Gerenciais:** Visão geral de OS por período, receita e desempenho por mecânico.
- 🔐 **Controle de Acesso por Perfil:** Quatro perfis distintos (Cliente, Atendente, Mecânico, Gerente) com permissões específicas.
- 🗂️ **Catálogo de Serviços:** Gerenciamento de serviços com preço e tempo previsto.

---

## 🛠 Tecnologias Utilizadas

### 💻 Front-end

- **Biblioteca:** React 18
- **Linguagem:** JavaScript ES6+
- **Estilização:** Tailwind CSS
- **Gerenciamento de Estado:** Context API
- **Build Tool:** Vite

### 🖥️ Back-end

- **Runtime:** Node.js 20 (LTS)
- **Framework:** Express 4.x
- **Banco de Dados:** PostgreSQL 16
- **ORM:** Prisma
- **Autenticação:** JWT

### ⚙️ Infraestrutura & DevOps

- **Containerização:** Docker e Docker Compose
- **Versionamento:** Git + GitHub

---

## 🏗 Arquitetura

O sistema adota uma **arquitetura em três camadas**:

1. **Apresentação:** Aplicação web em React, acessada via navegador pelos quatro perfis de usuário.
2. **Lógica de Negócio:** API REST em Node.js/Express, responsável pelas regras de domínio (agendamento, OS, pagamento).
3. **Dados:** Banco de dados relacional PostgreSQL com 8 tabelas interligadas.

A comunicação entre camadas ocorre via HTTP/JSON (front → API) e SQL/TCP (API → banco).

### Diagramas

| Diagrama | Arquivo |
|---|---|
| Casos de Uso | [casos_de_uso.puml](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas/casos_de_uso.puml) |
| Classes | [classes.puml](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas/classes.puml) |
| Sequência — Agendamento | [sequencia_agendamento.puml](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas/sequencia_agendamento.puml) |
| Sequência — Ordem de Serviço | [sequencia_os.puml](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas/sequencia_os.puml) |
| Sequência — Pagamento | [sequencia_pagamento.puml](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas/sequencia_pagamento.puml) |
| Comunicação — Agendamento | [comunicacao_agendamento.puml](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas/comunicacao_agendamento.puml) |
| Comunicação — Ordem de Serviço | [comunicacao_os.puml](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas/comunicacao_os.puml) |
| Comunicação — Pagamento | [comunicacao_pagamento.puml](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas/comunicacao_pagamento.puml) |
| Estados — Ordem de Serviço | [estados_os.puml](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas/estados_os.puml) |
| Estados — Agendamento | [estados_agendamento.puml](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas/estados_agendamento.puml) |
| Componentes | [componentes.puml](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas/componentes.puml) |
| Implantação | [implantacao.puml](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas/implantacao.puml) |
| Modelo de Dados | [modelo_dados.puml](https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware/tree/main/Diagramas/modelo_dados.puml) |

---

## 🔧 Instalação e Execução

### Pré-requisitos

- **Node.js:** v20.x ou superior
- **npm:** v9.x ou superior
- **Docker** (recomendado para o banco de dados)
- **Git**

### 🔑 Variáveis de Ambiente

Crie um arquivo **`.env`** na raiz da pasta `/backend`:

| Variável | Descrição | Exemplo |
|---|---|---|
| `PORT` | Porta do servidor | `3000` |
| `DATABASE_URL` | URL de conexão PostgreSQL | `postgresql://postgres:senha@localhost:5432/sgom` |
| `JWT_SECRET` | Chave secreta para tokens JWT | `chave_super_segura` |

Crie um arquivo **`.env`** na raiz da pasta `/frontend`:

| Variável | Descrição | Exemplo |
|---|---|---|
| `VITE_API_URL` | URL base da API | `http://localhost:3000/api` |

### 📦 Instalação de Dependências

1. **Clone o repositório:**

```bash
git clone https://github.com/ViniciusParanho/TrabalhoFinal-ProjetoDeSoftware.git
cd TrabalhoFinal-ProjetoDeSoftware
```

2. **Instale as dependências do front-end:**

```bash
cd frontend
npm install
cd ..
```

3. **Instale as dependências do back-end:**

```bash
cd backend
npm install
cd ..
```

### 💾 Inicialização do Banco de Dados

Suba o PostgreSQL via Docker:

```bash
docker run --name sgom_db \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_PASSWORD=senha123 \
  -e POSTGRES_DB=sgom \
  -p 5432:5432 \
  -d postgres:16
```

Execute as migrações com Prisma:

```bash
cd backend
npx prisma migrate dev
```

### ⚡ Como Executar a Aplicação

**Terminal 1 — Back-end:**

```bash
cd backend
npm run dev
```

🚀 API disponível em `http://localhost:3000`

**Terminal 2 — Front-end:**

```bash
cd frontend
npm run dev
```

🎨 Aplicação disponível em `http://localhost:5173`

### 🐳 Execução com Docker Compose

```bash
docker-compose up --build -d
```

Para encerrar:

```bash
docker-compose down
```

---

## 📂 Estrutura de Pastas

```
TrabalhoFinal-ProjetoDeSoftware/
├── README.md
├── docker-compose.yml
├── .gitignore
│
├── /Diagramas                        # Códigos PlantUML
│   ├── casos_de_uso.puml
│   ├── classes.puml
│   ├── sequencia_agendamento.puml
│   ├── sequencia_os.puml
│   ├── sequencia_pagamento.puml
│   ├── comunicacao_agendamento.puml
│   ├── comunicacao_os.puml
│   ├── comunicacao_pagamento.puml
│   ├── estados_os.puml
│   ├── estados_agendamento.puml
│   ├── componentes.puml
│   ├── implantacao.puml
│   └── modelo_dados.puml
│
├── /docs                             # Documentação do projeto
│   └── Documentacao_Projeto_SGOM.pdf
│
├── /frontend                         # Aplicação React
│   ├── .env
│   ├── package.json
│   ├── vite.config.js
│   └── /src
│       ├── /components
│       ├── /pages
│       │   ├── Agendamento.jsx
│       │   ├── OrdemServico.jsx
│       │   ├── Pagamento.jsx
│       │   └── Relatorios.jsx
│       ├── /services
│       └── /context
│
└── /backend                          # API REST Node.js
    ├── .env
    ├── package.json
    ├── /src
    │   ├── /controllers
    │   │   ├── AgendamentoController.js
    │   │   ├── OrdemServicoController.js
    │   │   ├── PagamentoController.js
    │   │   └── RelatorioController.js
    │   ├── /services
    │   │   ├── ClienteService.js
    │   │   └── VeiculoService.js
    │   ├── /routes
    │   └── /middleware
    └── /prisma
        └── schema.prisma
```

---

## 🔗 Documentações utilizadas

- 📖 **React:** [Documentação Oficial do React](https://react.dev/reference/react)
- 📖 **Vite:** [Guia de Configuração do Vite](https://vitejs.dev/config/)
- 📖 **Express:** [Documentação do Express.js](https://expressjs.com/)
- 📖 **Prisma:** [Documentação do Prisma ORM](https://www.prisma.io/docs)
- 📖 **PostgreSQL:** [Documentação do PostgreSQL](https://www.postgresql.org/docs/)
- 📖 **PlantUML:** [Documentação do PlantUML](https://plantuml.com/)
- 📖 **Docker:** [Documentação do Docker](https://docs.docker.com/)

---

## 👥 Autores

| 👤 Nome | GitHub |
|---|---|
| Vinícius Paranho Ribeiro | [@ViniciusParanho](https://github.com/ViniciusParanho) |

---

## 🙏 Agradecimentos

- [**Engenharia de Software PUC Minas**](https://www.instagram.com/engsoftwarepucminas/) — Pelo apoio institucional e estrutura acadêmica.
- [**Prof. Dr. João Paulo Aramuni**](https://github.com/joaopauloaramuni) — Pelos ensinamentos sobre Arquitetura de Software, Padrões de Projeto e Projeto de Software.

---

## 📄 Licença

Este projeto é distribuído sob a **Licença MIT**.
