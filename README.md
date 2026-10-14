<h1 align="center">Hi, I'm Matheus 👋</h1>
<p align="center"><b>Full Stack Developer • Automation • Data • AI</b></p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1000&color=2F81F7&center=true&vCenter=true&width=600&lines=Python+%7C+FastAPI+%7C+PostgreSQL;React+%7C+TypeScript+%7C+Node.js;Automation%2C+data+pipelines+and+AI" alt="Typing SVG" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/matheusjammal/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:matheusagjammal@hotmail.com"><img src="https://img.shields.io/badge/Email-0078D4?style=for-the-badge&logo=microsoftoutlook&logoColor=white" alt="Email" /></a>
</p>

<p align="center">🇺🇸 English • <a href="README.pt-BR.md">🇧🇷 Português</a></p>

---

## About Me

I'm a full stack developer from Curitiba, Brazil, focused on automation, data and AI. I build systems that replace manual, repetitive work.

Since March 2025 I've been the lead developer of the internal platforms at **L8 Group**, a technology and solar energy company. My work there covers sales, purchasing and business intelligence: I gather requirements with the business teams, then design, build, deploy and maintain the systems.

Before tech, I spent four years in sales and finance, working on technical sales and public procurement. That's where I saw how much of the operation ran on spreadsheets and repetitive manual work. I started programming to fix it, and I still start from the business problem before choosing the technology.

I'm currently studying IT Management at the Federal Institute of Paraná (IFPR).

## Tech Stack

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

**Data**<br>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/Firestore-FFCA28?style=flat-square&logo=firebase&logoColor=black" />

**Automation & AI**<br>
<img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white" />
<img src="https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white" />
<img src="https://img.shields.io/badge/Google_Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" />
<img src="https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=anthropic&logoColor=white" />

**DevOps & Tools**<br>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" />
<img src="https://img.shields.io/badge/Firebase-DD2C00?style=flat-square&logo=firebase&logoColor=white" />
<img src="https://img.shields.io/badge/Google_Cloud-4285F4?style=flat-square&logo=googlecloud&logoColor=white" />
<img src="https://img.shields.io/badge/Azure_DevOps-0078D7?style=flat-square&logo=azuredevops&logoColor=white" />

## Featured Projects

> The projects below run in production. Their source code is private, either because it's proprietary or because the project is being turned into a product. I'm happy to give a live demo in an interview.

### ZeniteApp: public procurement automation
A platform that automates participation in Brazilian public procurement, from finding tenders to submitting bids.

- **Data pipeline:** a Python collector (httpx, asyncpg) pulls data from the national procurement API (PNCP) every hour and stores it in PostgreSQL, which now holds over 1 million records.
- **Automation:** an Electron + Playwright desktop app and a server-side bot register proposals and submit over 100 bids a day.
- **Performance:** I traced a slow search with EXPLAIN ANALYZE and rewrote it to use GIN indexes, taking it from 1.8 s to 140 ms (13× faster).
- **AI:** Google Gemini analyzes tender documents, with server-side cost limits.
- **Quality:** 329 Pytest tests, one Dockerfile per service, and automatic deployment on every push to `main`.
- **Result:** a 50-item proposal now takes under 5 minutes to submit.

**Stack:** Python, FastAPI, PostgreSQL, React, TypeScript, Electron, Playwright, Docker

### L8 Energy Portal: sales cycle management
Sales management platform for a solar energy company. It covers role-based access control, proposal management, automated PDF contract generation, and site feasibility analysis by geolocation using the Google Solar API.

**Stack:** React, Firebase (Auth, Firestore, Functions), TailwindCSS, Google Solar API

### L8 Notes AI: AI-powered task management
A SPA that uses Gemini to extract tasks and owners from meeting minutes. The whole compliance team (6 people) uses it every day. Includes OAuth2, hierarchical RBAC, server-side encryption and a daily cron job.

**Stack:** React 19, TypeScript, Express.js, Firebase, Google Gemini API
