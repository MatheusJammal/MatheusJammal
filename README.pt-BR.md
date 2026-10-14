<h1 align="center">Olá, eu sou o Matheus 👋</h1>
<p align="center"><b>Desenvolvedor Full Stack • Automação • Dados • IA</b></p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1000&color=2F81F7&center=true&vCenter=true&width=600&lines=Python+%7C+FastAPI+%7C+PostgreSQL;React+%7C+TypeScript+%7C+Node.js;Automa%C3%A7%C3%A3o%2C+pipelines+de+dados+e+IA" alt="Typing SVG" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/matheusjammal/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:matheusagjammal@hotmail.com"><img src="https://img.shields.io/badge/Email-0078D4?style=for-the-badge&logo=microsoftoutlook&logoColor=white" alt="Email" /></a>
</p>

<p align="center"><a href="README.md">🇺🇸 English</a> • 🇧🇷 Português</p>

---

## Sobre mim

Sou desenvolvedor full stack em Curitiba, com foco em automação, dados e IA. Construo sistemas que substituem trabalho manual e repetitivo.

Desde março de 2025 sou o desenvolvedor principal das plataformas internas da **L8 Group**, empresa de tecnologia e energia solar. Lá cuido das áreas de vendas, compras e inteligência de negócios: levanto requisitos com as áreas, desenho, desenvolvo, implanto e mantenho os sistemas.

Antes da tecnologia, passei quatro anos na área comercial e financeira, com vendas técnicas e licitações públicas. Foi ali que vi quanto da operação dependia de planilhas e de trabalho manual repetitivo. Comecei a programar para resolver isso, e até hoje parto do problema de negócio antes de escolher a tecnologia.

Curso Gestão em Tecnologia da Informação no Instituto Federal do Paraná (IFPR).

## Tecnologias

**Backend & APIs**<br>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
<img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" />
<img src="https://img.shields.io/badge/REST_API-FF6C37?style=flat-square&logo=postman&logoColor=white" />
<img src="https://img.shields.io/badge/OAuth2-EB5424?style=flat-square&logo=auth0&logoColor=white" />

**Frontend & Desktop**<br>
<img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/TailwindCSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
<img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" />
<img src="https://img.shields.io/badge/Electron-47848F?style=flat-square&logo=electron&logoColor=white" />

**Dados**<br>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/Firestore-FFCA28?style=flat-square&logo=firebase&logoColor=black" />

**Automação e IA**<br>
<img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white" />
<img src="https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white" />
<img src="https://img.shields.io/badge/Google_Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" />
<img src="https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=anthropic&logoColor=white" />

**DevOps e Ferramentas**<br>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" />
<img src="https://img.shields.io/badge/Firebase-DD2C00?style=flat-square&logo=firebase&logoColor=white" />
<img src="https://img.shields.io/badge/Google_Cloud-4285F4?style=flat-square&logo=googlecloud&logoColor=white" />
<img src="https://img.shields.io/badge/Azure_DevOps-0078D7?style=flat-square&logo=azuredevops&logoColor=white" />

## Projetos em destaque

> Os projetos abaixo estão em produção. O código é privado, seja por ser propriedade da empresa, seja porque o projeto está virando produto. Posso fazer uma demonstração ao vivo em entrevista.

### ZeniteApp: automação de licitações públicas
Plataforma que automatiza a participação em licitações públicas, da busca de editais ao envio de lances.

- **Pipeline de dados:** um coletor em Python (httpx, asyncpg) consulta a API do PNCP a cada hora e grava em PostgreSQL, que hoje tem mais de 1 milhão de registros.
- **Automação:** um app desktop em Electron + Playwright e um robô no servidor cadastram propostas e enviam mais de 100 lances por dia.
- **Desempenho:** investiguei uma busca lenta com EXPLAIN ANALYZE e reescrevi a consulta para usar índices GIN, de 1,8 s para 140 ms (13× mais rápida).
- **IA:** o Google Gemini analisa os editais, com travas de custo no servidor.
- **Qualidade:** 329 testes com Pytest, um Dockerfile por serviço e deploy automático a cada push na `main`.
- **Resultado:** uma proposta com dezenas de itens passou a ser cadastrada em menos de 5 minutos.

**Stack:** Python, FastAPI, PostgreSQL, React, TypeScript, Electron, Playwright, Docker

### Portal L8 Energy: gestão do ciclo de vendas
Plataforma de gestão de vendas para uma empresa de energia solar. Tem controle de acesso por perfil, gestão de propostas, geração automática de contratos em PDF e análise de viabilidade técnica por geolocalização com a Google Solar API.

**Stack:** React, Firebase (Auth, Firestore, Functions), TailwindCSS, Google Solar API

### L8 Notes AI: gestão de tarefas com IA
SPA que usa o Gemini para extrair tarefas e responsáveis de atas de reunião. A equipe de compliance inteira (6 pessoas) usa todos os dias. Tem OAuth2, RBAC hierárquico, criptografia server-side e um cron job diário.

**Stack:** React 19, TypeScript, Express.js, Firebase, Google Gemini API
