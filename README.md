# 🧀 DevRats – A Academia dos Devs / The Developer Gym

 > "Treine seu código. Ganhe XP. Evolua como um verdadeiro DevRat!" 
 > *(Train your code. Earn XP. Evolve like a true DevRat!)* 
 
 <div align="center"> 
 
 ![DevRats Logo](https://via.placeholder.com/200x200?text=🐀+DevRats) 
 
 [![Next.js](https://img.shields.io/badge/Next.js-14-black?logo=next.js)](https://nextjs.org/) [![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248?logo=mongodb)](https://www.mongodb.com/) [![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?logo=typescript)](https://www.typescriptlang.org/) [![Vercel](https://img.shields.io/badge/Deployed-Vercel-black?logo=vercel)](https://vercel.com) 
 
 [🇧🇷 Português](#português) | [🇺🇸 English](#english) 
 
 </div> 
 
 --- 
 ## 🧠 Visão Geral
 
  O **DevRats** transforma sua rotina de programação em uma experiência gamificada envolvente. 
  
  Conecte sua conta do **GitHub**, sincronize automaticamente seus commits e evolua como um verdadeiro rato de laboratório do código 🐀💻 
  
  Cada linha de código vira **XP**, cada commit mantém sua **streak**, e cada conquista desbloqueia novos **badges**. Você pode competir com amigos em tempo real através do **Party Mode** e exibir todo seu progresso com um **badge dinâmico SVG** no seu perfil do GitHub. 
  
  ### ✨ Features Principais 
  
  - 🎮 **Gamificação Completa**: Sistema de XP, níveis e conquistas 
  
  - 🔥 **Streak System**: Mantenha seus commits diários e não quebre a sequência 
  
  - 🏅 **Sistema de Badges**: Desbloqueie conquistas especiais 
  
  - 👥 **Party Mode**: Competições em tempo real com amigos 
  
  - 📊 **Analytics**: Visualize seu progresso com gráficos interativos 
  - 🌍 **Bilíngue**: Interface completa em PT-BR e EN-US 
  - 🎨 **Temas**: Dark e Light mode com persistência 
  - 🧬 **Badge Dinâmico**: SVG gerado em tempo real para seu README 
  --- 
  ## ⚙️ Tech Stack
   ### Frontend 
   - **Next.js 14** (App Router) - Framework React com SSR 
   - **TypeScript** - Type safety e melhor DX 
   - **TailwindCSS** - Utility-first CSS framework 
   - **Framer Motion** - Animações fluidas e interativas 
   - **react-i18next** - Sistema de internacionalização 
   - **Recharts** - Visualização de dados e gráficos 
   
   ### Backend 
   - **Next.js API Routes** - Endpoints serverless 
   - **NextAuth.js** - Autenticação OAuth com GitHub 
   - **Socket.io** - Comunicação em tempo real para Party 
   Mode 
   - **Node.js fetch** - Integração com GitHub API 
   
   ### Database & Storage 
   - **MongoDB Atlas** - Banco de dados NoSQL na nuvem 
   - **Mongoose** - ODM para MongoDB 
   
   ### DevOps & Deploy 
   - **Vercel** - Hospedagem e CI/CD automático 
   - **GitHub Webhooks** - Sincronização automática de commits 
   - **Environment Variables** - Configuração segura 
   --- 
   
## 🏗️ Estrutura do Projeto

devrats/
│
├── src/
│   ├── app/                          # Next.js App Router
│   │   ├── layout.tsx               # Layout principal
│   │   ├── page.tsx                 # Landing page
│   │   │
│   │   ├── dashboard/               # Dashboard do usuário
│   │   │   ├── page.tsx            # Overview
│   │   │   ├── badges/page.tsx     # Conquistas
│   │   │   ├── leaderboard/page.tsx # Rankings
│   │   │   ├── party/page.tsx      # Party Mode
│   │   │   └── settings/page.tsx   # Configurações
│   │   │
│   │   └── api/                     # API Routes
│   │       ├── auth/[...nextauth]/route.ts
│   │       ├── user/route.ts
│   │       ├── stats/route.ts
│   │       ├── badge/[username]/route.ts
│   │       ├── leaderboard/route.ts
│   │       ├── party/route.ts
│   │       ├── webhook/github/route.ts
│   │       └── translate/route.ts
│   │
│   ├── components/                   # Componentes React
│   │   ├── Navbar.tsx
│   │   ├── XPProgressBar.tsx
│   │   ├── BadgeCard.tsx
│   │   ├── CommitChart.tsx
│   │   ├── PartyLeaderboard.tsx
│   │   ├── LanguageToggle.tsx
│   │   ├── ThemeToggle.tsx
│   │   └── NotificationToast.tsx
│   │
│   ├── lib/                          # Utilitários e helpers
│   │   ├── mongodb.ts               # Conexão MongoDB
│   │   ├── github.ts                # GitHub API integration
│   │   ├── badges.ts                # Lógica de badges
│   │   ├── streak.ts                # Cálculo de streaks
│   │   ├── party.ts                 # Party Mode logic
│   │   ├── i18n.ts                  # Configuração i18n
│   │   └── auth-options.ts          # NextAuth config
│   │
│   ├── models/                       # Mongoose Models
│   │   ├── User.ts
│   │   ├── Commit.ts
│   │   ├── Badge.ts
│   │   └── Party.ts
│   │
│   └── styles/
│       └── globals.css              # Estilos globais
│
├── public/                           # Assets estáticos
│   ├── icons/                       # Ícones do app
│   ├── flags/                       # Bandeiras PT/EN
│   └── badges/                      # Imagens de badges
│
├── tailwind.config.js
├── next.config.js
├── package.json
└── .env.local             # Variáveis de ambiente
--- 

## 💪 Sistema de Gamificação 

| Mecânica | Descrição | 
|----------|-----------| 
| 🧀 **XP** | Ganho através de commits, PRs e issues resolvidos |
 | 🔥 **Streak** | Dias consecutivos programando (não quebre a sequência!) |
| 🏋️ **Níveis** | Evolua a cada threshold de XP alcançado 
| 
| 🏅 **Badges** | Conquistas especiais ("Code Streak Master", "Open Source Beast") | 
| 💬 **Party Mode** | Competições em tempo real com amigos (1v1 ou grupos) | 
| 🧩 **Missões Diárias** | Desafios: "3 commits hoje", "abra um PR", etc | 
| 📈 **Leaderboard** | Rankings global, por país e entre amigos | 
| 🕹️ **Notificações** | Toasts animados de progresso e conquistas | 
### 🎯 Como Funciona o XP
 - **Commit**: 10 XP base 
 - **Pull Request**: 50 XP 
 - **Issue Resolvido**: 30 XP 
 - **Code Review**: 20 XP 
 - **Bônus de Streak**: +5 XP por dia consecutivo 
 - **Bônus de Party**: +10 XP quando em competição 
 --- 
 ## 🗄️ Modelos de Dados ### User Schema

typescript
{
  githubId: string,
  username: string,
  avatar: string,
  xp: number,
  level: number,
  streak: number,
  lastCommitDate: Date,
  badges: [ObjectId],
  language: "pt" | "en",
  theme: "dark" | "light",
  createdAt: Date,
  updatedAt: Date
}

### Commit Schema

typescript
{
  userId: ObjectId,
  date: Date,
  count: number,
  xpEarned: number,
  repositories: [string]
}

### Badge Schema

typescript
{
  name: { 
    pt: string, 
    en: string 
  },
  description: { 
    pt: string, 
    en: string 
  },
  requirement: string,
  icon: string,
  xpRequired: number,
  type: "streak" | "xp" | "special" | "party"
}
### Party Schema

typescript
{
  code: string,
  members: [ObjectId],
  startDate: Date,
  endDate: Date,
  duration: number, // em minutos
  stats: [{ 
    userId: ObjectId, 
    commits: number,
    xpEarned: number 
  }],
  winner: ObjectId | null,
  isActive: boolean
}
--- 
## 🔗 API Endpoints
| Rota | Método | Descrição | 
|------|--------|-----------| 
| /api/auth/[...nextauth] | ALL | Autenticação OAuth com GitHub | 
| /api/stats | GET/POST | Atualiza XP, streak e badges via GitHub API | 
| /api/badge/[username] | GET | Gera badge SVG dinâmico | 
| /api/party | POST/GET | Criação e controle de Partys | 
| /api/party/join | POST | Entrar em uma Party existente | 
| /api/leaderboard | GET | Retorna rankings (global, país, amigos) | 
| /api/webhook/github | POST | Recebe push events do GitHub | 
| /api/translate | GET | Traduções dinâmicas PT/EN | 
| /api/user/[username] | GET | Dados públicos do usuário | 
--- 
## 🌍 Sistema de Internacionalização 

O app detecta automaticamente o idioma do navegador e permite alternar entre **🇧🇷 Português** e **🇺🇸 Inglês**. 
### Tecnologia: react-i18next 

**Exemplo - Português (pt.json)**
json
{
  "welcome": "Bem-vindo ao DevRats!",
  "xp_today": "Você ganhou {{xp}} XP hoje!",
  "level_up": "Você subiu de nível!",
  "streak_warning": "Cuidado! Sua streak está em risco!"
}

**Exemplo - English (en.json)**
json
{
  "welcome": "Welcome to DevRats!",
  "xp_today": "You earned {{xp}} XP today!",
  "level_up": "You leveled up!",
  "streak_warning": "Watch out! Your streak is at risk!"
}
--- 
## 🪄 Features Extras 
- 🎨 **Rat Mode** - Animações temáticas quando ganha badges especiais 
- 🌚 **Dark / Light Theme** - Alternância com persistência no localStorage 
- 📊 **Commit Chart** - Visualização de commits com recharts 
- 🔔 **Notificações Animadas** - Toasts com Framer Motion 
- 🧭 **Party Mini-map** - Veja o progresso dos amigos em tempo real 
- 🧩 **Missões do Dia** - Desafios diários com recompensas extras - 🎭 **Perfil Público** - Página de perfil compartilhável 
- 📱 **Responsivo** - Design adaptado para mobile, tablet e desktop 
--- 

## 🚀 Como Rodar Localmente 

### Pré-requisitos 
- Node.js 18+ 
- npm ou yarn 
- Conta GitHub (para OAuth) 
- Conta MongoDB Atlas 
### 1. Clone o repositório
bash
git clone https://github.com/seu-usuario/devrats.git
cd devrats
### 2. Instale as dependências

bash
npm install
# ou
yarn install

### 3. Configure as variáveis de ambiente 

Crie um arquivo .env.local na raiz do projeto:

env
# MongoDB
MONGODB_URI=mongodb+srv://seu-usuario:senha@cluster.mongodb.net/devrats

# NextAuth
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=seu-secret-muito-seguro

# GitHub OAuth
GITHUB_ID=seu-github-oauth-id
GITHUB_SECRET=seu-github-oauth-secret

# GitHub API
GITHUB_TOKEN=seu-github-personal-access-token

# Socket.io (opcional para development)
SOCKET_SERVER_URL=http://localhost:3001


### 4. Rode o projeto

bash
npm run dev
# ou
yarn dev

Acesse: http://localhost:3000 

--- 
## 📅 Cronograma de Desenvolvimento (11 dias) 

| Dia | Tarefa | Status | 
|-----|--------|--------| 
| **1-2** | Setup inicial + Autenticação GitHub OAuth | ⏳ 
| 
| **3** | MongoDB setup + Models (User, Commit, Badge) 
| ⏳ | 
| **4-5** | Dashboard + Sistema de XP + Streak | ⏳ | 
| **6** | Sistema de Badges + Conquistas | ⏳ | 
| **7** | Leaderboard + Party Mode (Socket.io) | ⏳ | 
| **8** | Badge dinâmico SVG + Webhooks GitHub | ⏳ | 
| **9** | i18n (PT/EN) + Sistema de Temas | ⏳ | 
| **10** | Polimento + Animações + UX | ⏳ | 
 **11** | Deploy Vercel + README + Apresentação 💥 | 
 ⏳ | 
 
 --- 
 
 ## 🎯 Deploy 
 
 ### Hospedagem 
 - **Frontend + Backend**: [Vercel](https://vercel.com) 
 - **Database**: [MongoDB Atlas]
 (https://www.mongodb.com/cloud/atlas) 
 - **CDN**: Vercel Edge Network 
 
 ### Deploy Automático 
 O projeto está configurado para deploy automático a cada push na branch main: 
 1. Conecte seu repositório ao Vercel 
 2. Configure as variáveis de ambiente 
 3. Deploy! 🚀 
 --- 
 ## 📜 Licença 
 Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes. 
 --- 
 ## 👥 Contribuindo Contribuições são bem-vindas! Sinta-se livre para:
1. Fazer um Fork do projeto 
2. Criar uma branch para sua feature (git checkout -b feature/MinhaFeature) 
3. Commit suas mudanças (git commit -m 'Add: Minha nova feature') 4. Push para a branch (git push origin feature/MinhaFeature) 
5. Abrir um Pull Request 
--- 
## 💬 Contato & Suporte 
- 🐛 **Issues**: [GitHub Issues](https://github.com/seu-usuario/devrats/issues) 
- 💡 **Discussões**: [GitHub Discussions](https://github.com/seu-usuario/devrats/discussions) 
- 📧 **Email**: contato@devrats.com 
--- <div align="center"> 
**Feito com 🧀 e muito ☕ por DevRats Team** 

⭐ Não esqueça de dar uma star no projeto! 

</div> this is actually our readme, so before i do the npx am i need to go for typescript ? bro its in english lets speak in english okay ?

This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
