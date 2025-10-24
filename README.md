# 🧀 DevRats – A Academia dos Devs / The Developer Gym

> “Treine seu código. Ganhe XP. Evolua como um verdadeiro DevRat!”  
> *(Train your code. Earn XP. Evolve like a true DevRat!)*

---

## 🧠 Visão Geral

O **DevRats** é uma plataforma que transforma sua rotina de programação em uma experiência gamificada.  
Conecte sua conta do **GitHub**, acompanhe seus commits e evolua como um verdadeiro rato de laboratório do código 🐀💻  

Cada atividade de desenvolvimento gera **XP**, **níveis**, **streaks** e **badges**.  
Você pode competir com amigos, entrar em “parties” e exibir seu progresso com um **badge dinâmico** no seu README do GitHub.

---

## ⚙️ Tech Stack

| Camada | Tecnologia | Função |
|--------|-------------|--------|
| **Frontend** | Next.js 14 (App Router) | Interface e rotas |
| **UI** | TailwindCSS + Framer Motion + i18next | Estilo, animações e tradução |
| **Backend** | Next API Routes + Node fetch | Lógica e integração com GitHub |
| **Banco de Dados** | MongoDB (Atlas) | Usuários, stats e badges |
| **Autenticação** | NextAuth.js (GitHub Provider) | Login OAuth seguro |
| **Realtime** | Socket.io | Party Mode (competição em tempo real) |
| **Charts** | Recharts | Visualização de XP e commits |
| **Badge** | SVG dinâmico via API | Exibição no README do GitHub |
| **Hospedagem** | Vercel | Deploy rápido e gratuito |

---

## 🏗️ Estrutura de Pastas

devrats/
│
├── src/
│ ├── app/
│ │ ├── layout.tsx
│ │ ├── page.tsx
│ │ ├── dashboard/
│ │ │ ├── page.tsx
│ │ │ ├── badges/page.tsx
│ │ │ ├── leaderboard/page.tsx
│ │ │ ├── party/page.tsx
│ │ │ └── settings/page.tsx
│ │ └── api/
│ │ ├── auth/[...nextauth]/route.ts
│ │ ├── user/route.ts
│ │ ├── stats/route.ts
│ │ ├── badge/[username]/route.ts
│ │ ├── leaderboard/route.ts
│ │ ├── party/route.ts
│ │ ├── webhook/github/route.ts
│ │ └── translate/route.ts
│ │
│ ├── components/
│ │ ├── Navbar.tsx
│ │ ├── XPProgressBar.tsx
│ │ ├── BadgeCard.tsx
│ │ ├── CommitChart.tsx
│ │ ├── PartyLeaderboard.tsx
│ │ ├── LanguageToggle.tsx
│ │ ├── ThemeToggle.tsx
│ │ └── NotificationToast.tsx
│ │
│ ├── lib/
│ │ ├── mongodb.ts
│ │ ├── github.ts
│ │ ├── badges.ts
│ │ ├── streak.ts
│ │ ├── party.ts
│ │ ├── i18n.ts
│ │ └── auth-options.ts
│ │
│ ├── models/
│ │ ├── User.ts
│ │ ├── Commit.ts
│ │ ├── Badge.ts
│ │ └── Party.ts
│ │
│ └── styles/
│ └── globals.css
│
├── public/
│ ├── icons/
│ ├── flags/
│ └── badges/
│
├── tailwind.config.js
├── next.config.js
├── package.json
└── .env.local


---

## 🌍 Dualidade Linguística (PT/EN)

O app detecta automaticamente o idioma do navegador e permite trocar entre **🇧🇷 Português** e **🇺🇸 Inglês**.

Ferramenta: **react-i18next**

Exemplo de tradução:

**Português**
```json
{
  "welcome": "Bem-vindo ao DevRats!",
  "xp_today": "Você ganhou {{xp}} XP hoje!",
  "level_up": "Você subiu de nível!"
}


{
  "welcome": "Welcome to DevRats!",
  "xp_today": "You earned {{xp}} XP today!",
  "level_up": "You leveled up!"
}

<html>
<body>
<!--StartFragment--><h2 data-start="3342" data-end="3359">💪 Gamificação</h2>
<div class="_tableContainer_1rjym_1"><div tabindex="-1" class="group _tableWrapper_1rjym_13 flex w-fit flex-col-reverse">
Mecânica | Descrição
-- | --
🧀 XP | Ganho com commits, PRs e issues
🔥 Streak | Dias consecutivos com commits
🏋️ Níveis | Evolua a cada quantidade de XP
🏅 Badges | Conquistas especiais (“Code Streak”, “Open Source Beast”)
💬 Party Mode | Competições em tempo real com amigos
🧩 Missões diárias | “3 commits hoje”, “abra um PR” etc
📈 Leaderboard | Ranking global e por país
🕹️ Notificações | Toasts animados de progresso e conquistas

</div></div><!--EndFragment-->
</body>
</html>

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
  createdAt: Date
}

{
  userId: ObjectId,
  date: Date,
  count: number
}

{
  name: { pt: string, en: string },
  description: { pt: string, en: string },
  requirement: string,
  icon: string,
  xpRequired: number,
  type: "streak" | "xp" | "special"
}

{
  code: string,
  members: [ObjectId],
  startDate: Date,
  endDate: Date,
  stats: [{ userId: ObjectId, commits: number }],
  winner: ObjectId | null
}

<html>
<body>
<!--StartFragment--><h2 data-start="4588" data-end="4614">🔗 Endpoints Principais</h2>
<div class="_tableContainer_1rjym_1"><div tabindex="-1" class="group _tableWrapper_1rjym_13 flex w-fit flex-col-reverse">
Rota | Descrição
-- | --
/api/auth/[...nextauth] | Login via GitHub OAuth
/api/stats | Atualiza XP, streak e badges via GitHub API
/api/badge/[username] | Gera badge SVG dinâmico
/api/party | Criação e controle de Partys (com Socket.io)
/api/leaderboard | Retorna ranking global
/api/webhook/github | Recebe push events do GitHub
/api/translate | Traduções dinâmicas (PT/EN)

</div></div><!--EndFragment-->
</body>
</html>


<html>
<body>
<!--StartFragment--><h2 data-start="5057" data-end="5069">🪄 Extras</h2>
<ul data-start="5071" data-end="5375">
<li data-start="5071" data-end="5132">
<p data-start="5073" data-end="5132">🎨 <strong data-start="5076" data-end="5088">Rat Mode</strong> — animações temáticas quando ganha badges</p>
</li>
<li data-start="5133" data-end="5179">
<p data-start="5135" data-end="5179">🌚 <strong data-start="5138" data-end="5160">Dark / Light Theme</strong> com persistência</p>
</li>
<li data-start="5180" data-end="5218">
<p data-start="5182" data-end="5218">📊 <strong data-start="5185" data-end="5201">Commit Chart</strong> com <code data-start="5206" data-end="5216">recharts</code></p>
</li>
<li data-start="5219" data-end="5269">
<p data-start="5221" data-end="5269">🔔 <strong data-start="5224" data-end="5249">Notificações animadas</strong> via Framer Motion</p>
</li>
<li data-start="5270" data-end="5326">
<p data-start="5272" data-end="5326">🧭 <strong data-start="5275" data-end="5293">Party mini-map</strong> mostrando progresso dos amigos</p>
</li>
<li data-start="5327" data-end="5375">
<p data-start="5329" data-end="5375">🧩 <strong data-start="5332" data-end="5350">Missões do Dia</strong> com recompensas extras</p>
</li>
</ul>
<hr data-start="5377" data-end="5380">
<h2 data-start="5382" data-end="5428">🗓️ Cronograma de Desenvolvimento (11 dias)</h2>
<div class="_tableContainer_1rjym_1"><div tabindex="-1" class="group _tableWrapper_1rjym_13 flex w-fit flex-col-reverse">
Dia | Tarefa
-- | --
1–2 | Setup + Auth GitHub
3 | Banco MongoDB + Models
4–5 | Dashboard + XP + streak
6 | Sistema de Badges
7 | Leaderboard + Party mode
8 | Badge dinâmico SVG
9 | i18n + Tema
10 | Polimento + Animações
11 | Deploy + README + apresentação 💥

</div></div>
<hr data-start="5741" data-end="5744">
<h2 data-start="5746" data-end="5758">🚀 Deploy</h2>
<p data-start="5760" data-end="5874">Hospedado em <a data-start="5773" data-end="5801" rel="noopener" target="_new" class="decorated-link cursor-pointer">Vercel<span aria-hidden="true" class="ms-0.5 inline-block align-middle leading-none"><svg width="20" height="20" viewBox="0 0 20 20" fill="currentColor" xmlns="http://www.w3.org/2000/svg" data-rtl-flip="" class="block h-[0.75em] w-[0.75em] stroke-current stroke-[0.75]"><path d="M14.3349 13.3301V6.60645L5.47065 15.4707C5.21095 15.7304 4.78895 15.7304 4.52925 15.4707C4.26955 15.211 4.26955 14.789 4.52925 14.5293L13.3935 5.66504H6.66011C6.29284 5.66504 5.99507 5.36727 5.99507 5C5.99507 4.63273 6.29284 4.33496 6.66011 4.33496H14.9999L15.1337 4.34863C15.4369 4.41057 15.665 4.67857 15.665 5V13.3301C15.6649 13.6973 15.3672 13.9951 14.9999 13.9951C14.6327 13.9951 14.335 13.6973 14.3349 13.3301Z"></path></svg></span></a><br data-start="5801" data-end="5804">
Banco de dados no <a data-start="5822" data-end="5874" rel="noopener" target="_new" class="decorated-link" href="https://www.mongodb.com/cloud/atlas">MongoDB Atlas<span aria-hidden="true" class="ms-0.5 inline-block align-middle leading-none"><svg width="20" height="20" viewBox="0 0 20 20" fill="currentColor" xmlns="http://www.w3.org/2000/svg" data-rtl-flip="" class="block h-[0.75em] w-[0.75em] stroke-current stroke-[0.75]"><path d="M14.3349 13.3301V6.60645L5.47065 15.4707C5.21095 15.7304 4.78895 15.7304 4.52925 15.4707C4.26955 15.211 4.26955 14.789 4.52925 14.5293L13.3935 5.66504H6.66011C6.29284 5.66504 5.99507 5.36727 5.99507 5C5.99507 4.63273 6.29284 4.33496 6.66011 4.33496H14.9999L15.1337 4.34863C15.4369 4.41057 15.665 4.67857 15.665 5V13.3301C15.6649 13.6973 15.3672 13.9951 14.9999 13.9951C14.6327 13.9951 14.335 13.6973 14.3349 13.3301Z"></path></svg></span></a></p>
<!--EndFragment-->
</body>
</html>🪄 Extras

🎨 Rat Mode — animações temáticas quando ganha badges

🌚 Dark / Light Theme com persistência

📊 Commit Chart com recharts

🔔 Notificações animadas via Framer Motion

🧭 Party mini-map mostrando progresso dos amigos

🧩 Missões do Dia com recompensas extras

🗓️ Cronograma de Desenvolvimento (11 dias)
Dia	Tarefa
1–2	Setup + Auth GitHub
3	Banco MongoDB + Models
4–5	Dashboard + XP + streak
6	Sistema de Badges
7	Leaderboard + Party mode
8	Badge dinâmico SVG
9	i18n + Tema
10	Polimento + Animações
11	Deploy + README + apresentação 💥
🚀 Deploy

Hospedado em Vercel

Banco de dados no [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
