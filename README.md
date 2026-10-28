<h1 align="center">Matheus Jammal</h1>
<p align="center"><b>Desenvolvedor Full Stack · Construo software em torno de LLMs e automação</b></p>

<p align="center">
  <a href="https://www.linkedin.com/in/matheusjammal/" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:matheusagjammal@hotmail.com"><img src="https://img.shields.io/badge/Email-0078D4?style=for-the-badge&logo=microsoftoutlook&logoColor=white" alt="E-mail" /></a>
  <a href="https://www.matheusjammal.com" target="_blank"><img src="https://img.shields.io/badge/Portf%C3%B3lio-1A1AE5?style=for-the-badge&logoColor=white" alt="Portfólio" /></a>
</p>

<p align="center">🇧🇷 Português • <a href="README.en.md">🇺🇸 English</a></p>

---

## Sobre mim

Sou desenvolvedor full stack em Curitiba. Construo sistemas que substituem trabalho manual e repetitivo, e hoje boa parte deles tem um LLM no meio.

Desde março de 2025 sou desenvolvedor full stack na **L8 Group**, empresa de tecnologia e energia solar. Desenvolvo para a área de compliance, que recebe projetos de toda a empresa. Meu foco principal é automatizar a gestão e a manutenção das normas ISO 9001, 22301, 27001 e 27701: levanto requisitos, desenho, desenvolvo, implanto e mantenho os sistemas.

Antes da tecnologia, passei quatro anos na área comercial e financeira, com vendas técnicas e licitações públicas. Foi ali que vi quanto da operação dependia de planilhas e de trabalho manual repetitivo. Comecei a programar para resolver isso, e até hoje parto do problema de negócio antes de escolher a tecnologia.

Curso Gestão em Tecnologia da Informação no Instituto Federal do Paraná (IFPR), com previsão de conclusão em dezembro de 2028.

## Projetos em destaque

### ZeniteApp: automação de licitações públicas
Plataforma que automatiza a participação em licitações públicas, da busca de editais ao envio de lances.

- **IA de editais:** perguntas sobre o edital respondidas pelo Google Gemini com o texto completo no contexto. Escolhi **contexto direto em vez de RAG**: o edital cabe na janela e isso isola os dados de cada cliente por construção.
- **Resposta ancorada:** o prompt exige citar item e seção do edital e proíbe inventar, com temperatura 0,2.
- **Travas no servidor:** antes de cada chamada ao modelo, 6 verificações (escopo RBAC, vínculo, teto diário em R$, rate limit, cota mensal e limite de tokens), com o custo contabilizado na mesma transação.
- **Troca de provedor:** a integração com o modelo fica isolada em um único módulo; mudar de provedor significa mexer em um arquivo só.
- **Pipeline de dados:** um coletor em Python (httpx, asyncpg) consulta a API do PNCP a cada hora e grava em PostgreSQL, que hoje tem mais de 1,27 milhão de licitações.
- **Desempenho:** investiguei uma busca lenta com EXPLAIN ANALYZE e reescrevi a consulta para usar índices GIN, de 1,8 s para 140 ms (13× mais rápida).
- **Automação:** um app desktop em Electron + Playwright e um robô no servidor cadastram propostas e enviam mais de 100 lances por dia.
- **Qualidade:** 329 testes com Pytest, um Dockerfile por serviço e deploy automático a cada push na `main`.
- **Resultado:** o cadastro de uma proposta de 50 itens no portal de compras do governo, que era feito à mão item por item, passou de mais de 1 hora para menos de 5 minutos.

**Stack:** Python, FastAPI, PostgreSQL, Google Gemini API, React, TypeScript, Electron, Playwright, Docker

### L8 Notes AI: gestão de tarefas com IA
SPA que usa o Gemini para extrair tarefas e responsáveis de atas de reunião. A equipe de compliance inteira (6 pessoas) usa todos os dias. Tem OAuth2, RBAC hierárquico, criptografia server-side e um cron job diário.

**Stack:** React 19, TypeScript, Express.js, Firebase, Google Gemini API

### Portal L8 Energy: gestão do ciclo de vendas
Plataforma de gestão de vendas para uma empresa de energia solar. Tem controle de acesso por perfil, gestão de propostas, geração automática de contratos em PDF e análise de viabilidade técnica por geolocalização com a Google Solar API.

**Stack:** React, Firebase (Auth, Firestore, Functions), TailwindCSS, Google Solar API

## Como trabalho com IA

Desenvolvo guiado por especificação: escrevo escopo, regras e restrições antes de começar, e uso esse documento para dirigir a implementação com o Claude Code e para revisar o resultado. Nos produtos, trato o LLM como uma dependência externa: com contexto controlado, resposta que cita a fonte, custo medido e um único ponto de integração.

## Código público

- [matheusjammal.com](https://github.com/MatheusJammal/matheusjammal.com): meu portfólio, em HTML e CSS puros, sem framework nem build, publicado no GitHub Pages com domínio próprio.

## Tecnologias

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

- **Back-end e APIs:** Python, FastAPI, Node.js, Express, APIs REST, OAuth2
- **IA e automação:** Google Gemini API, Claude Code, Playwright, Electron, n8n, cron
- **Front-end:** React 19, TypeScript, JavaScript, TailwindCSS, Vite
- **Dados:** PostgreSQL, Firestore
- **Entrega e qualidade:** Docker, Git, Pytest, Firebase, Google Cloud, Azure DevOps
