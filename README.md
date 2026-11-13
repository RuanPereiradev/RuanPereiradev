<h1 align="center">Olá, eu sou o Ruan Pereira 👋</h1>

<p align="center">
  Desenvolvedor back-end e automação · Engenharia de Computação na UFC<br>
  Transformo trabalho repetitivo em sistema que funciona sozinho.
</p>

<p align="center">
  <a href="#-projeto-em-destaque"><img src="https://img.shields.io/badge/⭐_Projeto_em_destaque-SAM-2F6BFF?style=for-the-badge" /></a>
  <a href="#-meus-projetos"><img src="https://img.shields.io/badge/🚀_Meus_projetos-ver-111827?style=for-the-badge" /></a>
  <a href="#-conecte-se-comigo"><img src="https://img.shields.io/badge/📫_Contato-falar_comigo-16A34A?style=for-the-badge" /></a>
</p>

---

## 👨‍💻 Sobre mim

- 🔭 Estudando Engenharia de Computação na **Universidade Federal do Ceará**
- ⚙️ Trabalho com **Java/Spring**, **TypeScript/NestJS**, **React** e **Python** (automação e IA)
- 🌱 Estudando **Cloud: AWS**
- 📫 Contato: [ruanpereira@alu.ufc.br](mailto:ruanpereira@alu.ufc.br)

---

## ⭐ Projeto em destaque

<h3 align="center">🤖 SAM — o robô que transforma intimação em tarefa</h3>

<p align="center">
  <img src="assets/sam-motion.gif" alt="Motion explicativo do SAM: login no sistema, captura das intimações, leitura pela IA e criação das tarefas" width="860" />
</p>

<p align="center"><sub>Motion explicativo do fluxo do SAM · todos os dados mostrados são fictícios · <a href="assets/sam-motion.mp4">ver em vídeo (MP4)</a></sub></p>

### O problema

Num escritório de advocacia, toda intimação (aviso da Justiça) precisa virar uma **tarefa com prazo** no sistema
de gestão. São dezenas por dia, e na segunda-feira chegam juntas as do fim de semana. Esse trabalho é repetitivo,
exige atenção e um erro de data pode custar um prazo perdido.

### O que o SAM faz

O SAM é um robô que faz esse trabalho do começo ao fim, sem ninguém digitar:

| # | Etapa | O que acontece |
|---|-------|----------------|
| 1 | 🔐 **Login** | Entra sozinho no sistema do escritório |
| 2 | 📥 **Captura** | Pega só as intimações do dia anterior (na segunda, de sexta a domingo) que **ainda não têm tarefa** |
| 3 | 🧠 **Análise com IA** | Uma IA lê cada intimação, segue o manual da Controladoria e decide **o tipo do ato, a tarefa e o prazo em dias** |
| 4 | 📅 **Datas por regra** | O **código**, não a IA, calcula as datas: só dias úteis, prazo fatal e tarefa 2 dias antes (D-2), com feriados |
| 5 | 🛡️ **Travas de segurança** | Antes de gravar, barra o que está incompleto, duplicado ou com data já vencida e manda para a equipe |
| 6 | ✍️ **Lançamento** | Preenche o formulário da tarefa campo a campo, adiciona, confere o quadro e grava |
| 7 | ✅ **Conferência** | Abre o sistema de novo e confere se cada tarefa realmente ficou lá |
| 8 | 📋 **Relatório** | Entrega à equipe um relatório com o que foi lançado, o que não foi e os pontos de atenção |

### Decisões que importam

- **A IA entende o texto; as datas são calculadas por regra.** Sem chute em prazo.
- **Prefere não lançar a lançar errado.** O que o robô barra vai para uma pessoa, nunca some.
- **Confere o próprio trabalho.** Depois de gravar, verifica no sistema se a tarefa existe.
- **Segredos fora do código.** Credenciais e seletores ficam em configuração, nunca no repositório.

### Tecnologias

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white" />
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" />
  <img src="https://img.shields.io/badge/Agentes_de_IA-LLM-7C3AED?style=for-the-badge" />
  <img src="https://img.shields.io/badge/HTML%2FJS-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
</p>

> 🔒 **Código-fonte privado.** O SAM roda em um escritório real e lida com dados de clientes,
> por isso o repositório não é aberto. Aqui está só a explicação e o motion do fluxo.
> Se quiser conversar sobre como ele foi feito, é só me chamar.

---

## 🚀 Meus projetos

<table>
  <tr>
    <td width="50%" valign="top">
      <h4>🏨 Castel</h4>
      <p>Sistema de gestão hoteleira e de restaurante. Monolito modular com domínio rico.</p>
      <p><img src="https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white" /> <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white" /> <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" /> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" /></p>
      <a href="https://github.com/RuanPereiradev/sistema-castelo">Ver repositório →</a>
    </td>
    <td width="50%" valign="top">
      <h4>🍿 CineSol</h4>
      <p>Plataforma de gestão de cinemas e venda de ingressos em arquitetura de microsserviços.</p>
      <p><img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white" /> <img src="https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" /> <img src="https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white" /> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" /></p>
      <a href="https://github.com/RuanPereiradev/cinesol-microsservice">Ver repositório →</a>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h4>🔑 Docket Auth API</h4>
      <p>API de autenticação com MFA (TOTP), construída com Spring Boot, PostgreSQL e Redis.</p>
      <p><img src="https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white" /> <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white" /> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" /></p>
      <a href="https://github.com/RuanPereiradev/docket-backend">Ver repositório →</a>
    </td>
    <td width="50%" valign="top">
      <h4>🔄 Atlas Orquestrador</h4>
      <p>Orquestrador de eventos em NestJS para sincronização de dados em tempo real.</p>
      <p><img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white" /> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" /> <img src="https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white" /></p>
      <a href="https://github.com/RuanPereiradev/atlas-orquestrador">Ver repositório →</a>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h4>📅 AgendaPro</h4>
      <p>Front-end de um sistema de agendamento profissional online.</p>
      <p><img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" /> <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" /> <img src="https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" /></p>
      <a href="https://github.com/RuanPereiradev/AgendaPro-FrontEnd">Ver repositório →</a>
    </td>
    <td width="50%" valign="top">
      <h4>🏝️ WmTur</h4>
      <p>Landing page de vendas de passeios em Jericoacoara, feita em React.</p>
      <p><img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" /> <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" /></p>
      <a href="https://github.com/RuanPereiradev/WmTur">Ver repositório →</a>
    </td>
  </tr>
</table>

<p align="center">
  <a href="https://github.com/RuanPereiradev?tab=repositories">
    <img src="https://img.shields.io/badge/Ver_todos_os_repositórios-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
</p>

---

## 🛠️ Tecnologias e Ferramentas

<p align="center">
  <img src="https://skillicons.dev/icons?i=py,java,spring,ts,nestjs,react,nextjs,cs,dotnet,docker,postgres,redis,linux,git,github,vscode&theme=dark" />
</p>

---

## 📱 Conecte-se comigo

<p align="center">
  <a href="https://www.linkedin.com/in/ruan-pereira-do-nascimento-ab6a45228/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="mailto:ruanpereira@alu.ufc.br">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
  <a href="https://instagram.com/ruanpereira__" target="_blank">
    <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" />
  </a>
</p>

---

## 📊 GitHub

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=RuanPereiradev&layout=compact&theme=radical&hide_border=true" height="180" />
  <img src="https://streak-stats.demolab.com?user=RuanPereiradev&theme=radical&hide_border=true" height="180" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=RuanPereiradev&theme=github-dark&hide_border=true" />
</p>
