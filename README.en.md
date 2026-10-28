<h1 align="center">Matheus Jammal</h1>
<p align="center"><b>Full Stack Developer · I build software around LLMs and automation</b></p>

<p align="center">
  <a href="https://www.linkedin.com/in/matheusjammal/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:matheusagjammal@hotmail.com"><img src="https://img.shields.io/badge/Email-0078D4?style=for-the-badge&logo=microsoftoutlook&logoColor=white" alt="Email" /></a>
  <a href="https://www.matheusjammal.com"><img src="https://img.shields.io/badge/Portfolio-1A1AE5?style=for-the-badge&logoColor=white" alt="Portfolio" /></a>
</p>

<p align="center"><a href="README.md">🇧🇷 Português</a> • 🇺🇸 English</p>

---

## About Me

I'm a full stack developer from Curitiba, Brazil. I build systems that replace manual, repetitive work, and these days many of them have an LLM in the loop.

Since March 2025 I've been a full stack developer at **L8 Group**, a technology and solar energy company. I build for the compliance team, which takes on projects from across the company. My main focus is automating the management and upkeep of the ISO 9001, 22301, 27001 and 27701 standards: I gather requirements, then design, build, deploy and maintain the systems.

Before tech, I spent four years in sales and finance, working on technical sales and public procurement. That's where I saw how much of the operation ran on spreadsheets and repetitive manual work. I started programming to fix it, and I still start from the business problem before choosing the technology.

I'm studying IT Management at the Federal Institute of Paraná (IFPR), expected to graduate in December 2028.

## Featured Projects

### ZeniteApp: public procurement automation
A platform that automates participation in Brazilian public procurement, from finding tenders to submitting bids.

- **Tender AI:** questions about a tender are answered by Google Gemini with the full document in context. I chose **direct context over RAG**: the document fits in the window, and this keeps each client's data isolated by design.
- **Grounded answers:** the prompt requires citing the item and section of the tender and forbids making things up, at temperature 0.2.
- **Server-side guardrails:** before every model call, 6 checks run (RBAC scope, client link, daily spend cap in BRL, rate limit, monthly quota and token limit), and the cost is recorded in the same transaction.
- **Swappable provider:** the model integration lives in a single module, so changing providers means touching one file.
- **Data pipeline:** a Python collector (httpx, asyncpg) pulls data from the national procurement API (PNCP) every hour and stores it in PostgreSQL, which now holds over 1.27 million tenders.
- **Performance:** I traced a slow search with EXPLAIN ANALYZE and rewrote it to use GIN indexes, taking it from 1.8 s to 140 ms (13× faster).
- **Automation:** an Electron + Playwright desktop app and a server-side bot register proposals and submit over 100 bids a day.
- **Quality:** 329 Pytest tests, one Dockerfile per service, and automatic deployment on every push to `main`.
- **Result:** entering a 50-item proposal on the government procurement portal, which used to be done by hand item by item, went from over an hour to under 5 minutes.

**Stack:** Python, FastAPI, PostgreSQL, Google Gemini API, React, TypeScript, Electron, Playwright, Docker

### L8 Notes AI: AI-powered task management
A SPA that uses Gemini to extract tasks and owners from meeting minutes. The whole compliance team (6 people) uses it every day. Includes OAuth2, hierarchical RBAC, server-side encryption and a daily cron job.

**Stack:** React 19, TypeScript, Express.js, Firebase, Google Gemini API

### L8 Energy Portal: sales cycle management
Sales management platform for a solar energy company. It covers role-based access control, proposal management, automated PDF contract generation, and site feasibility analysis by geolocation using the Google Solar API.

**Stack:** React, Firebase (Auth, Firestore, Functions), TailwindCSS, Google Solar API

## How I Work with AI

I work spec-first: before I start, I write down the scope, rules and constraints, and I use that document to drive the implementation with Claude Code and to review the result. In products, I treat the LLM as an external dependency: controlled context, answers that cite their source, measured cost and a single integration point.

## Public Code

- [matheusjammal.com](https://github.com/MatheusJammal/matheusjammal.com): my portfolio, built with plain HTML and CSS (no framework, no build step) and served on GitHub Pages with a custom domain.

## Tech Stack

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Google_Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Google Gemini" />
  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white" alt="Playwright" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
</p>

- **Backend & APIs:** Python, FastAPI, Node.js, Express, REST APIs, OAuth2
- **AI & automation:** Google Gemini API, Claude Code, Playwright, Electron, n8n, cron
- **Frontend:** React 19, TypeScript, JavaScript, TailwindCSS, Vite
- **Data:** PostgreSQL, Firestore
- **Delivery & quality:** Docker, Git, Pytest, Firebase, Google Cloud, Azure DevOps
