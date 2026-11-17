<p align="center">
  <img src="assets/hero.gif" alt="Um mascote 3D de capacete monta, cubo por cubo, o nome Ruan Pereira: back-end e automação" width="100%" />
</p>

Estudo Engenharia de Computação na Universidade Federal do Ceará e trabalho com back-end em **Java/Spring** e
**TypeScript/NestJS**, front-end em **React** e automação em **Python**. Gosto de transformar trabalho repetitivo
em sistema que funciona sozinho. Estou estudando Cloud, com foco em AWS.

[Automações](#automações) · [Projetos web](#projetos-web) · [Desenvolvimento mobile](#desenvolvimento-mobile) · [Contato](#contato)

<br>

<img src="assets/sec-automacoes.svg" alt="Automações" width="100%" />

### SAM: o robô que transforma intimação em tarefa

<p align="center">
  <img src="assets/sam-motion.gif" alt="Motion do SAM: login no sistema, captura das intimações, leitura pela IA e criação das tarefas" width="860" />
</p>

<p align="center"><sub>Fluxo do SAM em motion. Todos os dados mostrados são fictícios. <a href="assets/sam-motion.mp4">Ver em MP4</a>.</sub></p>

Num escritório de advocacia, toda intimação (aviso da Justiça) precisa virar uma tarefa com prazo no sistema de
gestão. São dezenas por dia, e na segunda-feira chegam juntas as do fim de semana. O trabalho é repetitivo, exige
atenção, e um erro de data pode custar um prazo perdido. O SAM faz isso do começo ao fim, sem ninguém digitar.

| Etapa | O que acontece |
|---|---|
| Login | Entra sozinho no sistema do escritório |
| Captura | Pega só as intimações do dia anterior (na segunda, de sexta a domingo) que ainda não têm tarefa |
| Análise com IA | Uma IA lê cada intimação, segue o manual da Controladoria e decide o tipo do ato, a tarefa e o prazo em dias |
| Datas por regra | O código, não a IA, calcula as datas: só dias úteis, prazo fatal e tarefa dois dias antes, considerando feriados |
| Travas de segurança | Antes de gravar, barra o que está incompleto, duplicado ou com data vencida e encaminha para a equipe |
| Lançamento | Preenche o formulário da tarefa campo a campo, adiciona, confere o quadro e grava |
| Conferência | Abre o sistema de novo e confere se cada tarefa realmente ficou lá |
| Relatório | Entrega à equipe o que foi lançado, o que não foi e os pontos de atenção |

**Decisões de projeto**

- A IA entende o texto; as datas são calculadas por regra. Sem chute em prazo.
- Prefere não lançar a lançar errado: o que o robô barra vai para uma pessoa, nunca some.
- Confere o próprio trabalho: depois de gravar, verifica no sistema se a tarefa existe.
- Credenciais e seletores ficam em configuração, nunca no código.

`Python` `Selenium` `Flask` `Agentes de IA` `HTML/JS`

> O código do SAM é privado: ele roda em um escritório real e lida com dados de clientes.
> Aqui está só a explicação e o motion. Se quiser conversar sobre como foi feito, é só me chamar.

### Vila dos Bots: onde cada robô tem a sua vila

O SAM não trabalha sozinho. O escritório tem cinco robôs, e cada um mora numa vila em pixel art dentro da
**Vila dos Bots**, o painel que mostra o que cada um está fazendo. A vila só assiste: cada passo real do robô
vira um evento, e o mascote anda pela cena, explica na caixa de fala o que está fazendo e comemora (ou reclama)
no fim. Ela não grava nem aprova nada, e os eventos levam só fases e contagens, nunca nome de cliente nem o
teor de um processo.

<p align="center"><sub>As telas abaixo estão em modo simulação, sem dados reais. <a href="https://ruanpereiradev.github.io/autobots/">Abrir a vila em simulação</a>.</sub></p>

<p align="center">
  <img src="assets/vila-card-01.svg" alt="Vila 01, Sam: fortaleza de pedra em pixel art com um dragão dormindo sobre o tesouro e quatro heróis" width="100%" />
</p>

<p align="center">
  <img src="assets/vila-card-02.svg" alt="Vila 02, Bumblebee: ponte vista de cima com carros, robôs duelando e o carro amarelo do Bumblebee" width="49%" />
  <img src="assets/vila-card-03.svg" alt="Vila 03, Albi: campo com casa em domo, lago, dragão verde no céu e o mascote rosa do Albi" width="49%" />
</p>

<p align="center">
  <img src="assets/vila-card-04.svg" alt="Vila 04, Jarvis: garagem com telas, carros, armaduras e um núcleo azul de IA flutuando" width="49%" />
  <img src="assets/vila-card-05.svg" alt="Vila 05, Orelha: parque de cães com a casinha do Orelha, mural de calendário, caixa de correio e o cachorro" width="49%" />
</p>

`Pixel art em Canvas` `HTML/JS` `Flask` `Eventos em JSONL`

**Outras automações**

- **[Atlas Orquestrador](https://github.com/RuanPereiradev/atlas-orquestrador)**: orquestrador de eventos em NestJS para sincronização de dados em tempo real, com webhooks do Supabase. `NestJS` `TypeScript` `Supabase`
- **[CRM Sync Service](https://github.com/RuanPereiradev/crm-sync-service)**: serviço de sincronização de dados de CRM. `NestJS` `TypeScript`
- **[pyexcel](https://github.com/RuanPereiradev/pyexcel)**: script que lê uma base em Excel e separa os registros em abas por bairro, mantendo a formatação. `Python`

<br>

<img src="assets/sec-web.svg" alt="Projetos web" width="100%" />

### AGΩN: gestão de academias ligada à catraca

Sistema web para o dono e a recepção da academia. Ele se comunica com a catraca: a cada passagem, decide se
libera ou bloqueia o aluno, conforme o plano. **Já é usado por grandes academias da região.**

<p align="center">
  <img src="assets/agon-card-00.svg" alt="Agon: painel inicial com atalhos, indicadores de alunos ativos e entradas de hoje, e lista de planos para renovar. Dados fictícios" width="100%" />
</p>

<p align="center">
  <img src="assets/agon-card-01.svg" alt="Agon, tela Frequência: entradas de hoje, pessoas na academia agora, horário de pico e gráfico de movimento por hora. Dados fictícios" width="49%" />
  <img src="assets/agon-card-02.svg" alt="Agon, tela Matrículas: lista de alunos com plano, vencimento, forma de pagamento e situação. Dados fictícios" width="49%" />
</p>

<p align="center">
  <img src="assets/agon-card-03.svg" alt="Agon, tela Planos: cartões dos planos mensal, trimestral, semestral e anual com preço, serviços e número de alunos. Dados fictícios" width="49%" />
  <img src="assets/agon-card-04.svg" alt="Agon, tela Relatórios: alunos ativos, novos alunos, cancelamentos e gráficos de entradas por mês e por dia da semana. Dados fictícios" width="49%" />
</p>

<p align="center"><sub>Telas com dados fictícios, gerados só para as imagens.</sub></p>

`Python` `Flask` `SQLite` `HTML/CSS/JS` `Catraca Topdata`

> O código do AGΩN é privado: ele roda em academias reais e lida com dados de alunos.

### Castel: hotel e restaurante num só sistema

Sistema de gestão para hotel e restaurante. No restaurante, o cliente escaneia o QR da mesa, vê o cardápio e
faz o pedido pelo celular. O garçom acompanha cada item, a cozinha recebe os pedidos por setor, e o caixa fecha a
comanda. O hotel usa o mesmo núcleo financeiro para lançar diárias na conta do hóspede.

<p align="center">
  <img src="assets/castel-card-01.svg" alt="Castel, tela do cliente: entrada da mesa pelo QR, com nome e cardápio. Dados fictícios" width="49%" />
  <img src="assets/castel-card-02.svg" alt="Castel, tela de login: acesso da equipe por usuário e senha. Dados fictícios" width="49%" />
</p>

<p align="center"><sub>Telas com dados fictícios. Salão, caixa, cozinha e administração entram em breve.</sub></p>

`Java 21` `Spring Boot 4` `React` `PostgreSQL` `Docker` `Flyway`

**Decisões de projeto**

- Monolito modular: cada módulo (restaurante, hotel, billing, finance) expõe só a própria API. A fronteira é
  validada por ArchUnit no CI.
- Dinheiro sempre em `Money` e nunca em `double`. Valor trafega como string decimal.
- Comanda aceita lançamento concorrente sem lock otimista. Lock pessimista só no fechamento.
- Estados de domínio são métodos de negócio (`confirm()`, `cancel()`), não `setStatus()`.

**Outros projetos web**

*Motion explicativo em produção.*

- **[CineSol](https://github.com/RuanPereiradev/cinesol-microsservice)**: plataforma de gestão de cinemas e venda de ingressos em arquitetura de microsserviços. `NestJS` `Kafka` `Prisma` `PostgreSQL` `Docker`
- **[Docket Auth API](https://github.com/RuanPereiradev/docket-backend)**: API de autenticação com MFA (TOTP). `Java 21` `Spring Boot` `PostgreSQL` `Redis`
- **[AgendaPro](https://github.com/RuanPereiradev/AgendaPro-FrontEnd)**: front-end de um sistema de agendamento profissional online. `Next.js` `React` `TypeScript` `Tailwind`
- **[LetterFy](https://github.com/RuanPereiradev/letterfy-frontend)**: plataforma para avaliar músicas e álbuns, com back-end em Java. `React` `Vite` `Tailwind`
- **[WmTur](https://github.com/RuanPereiradev/WmTur)**: landing page de vendas de passeios em Jericoacoara. `React` `Vite`

<br>

<img src="assets/sec-mobile.svg" alt="Desenvolvimento mobile" width="100%" />

*Motion explicativo em produção.*

- **Glicare**: aplicativo para pacientes com diabetes, médicos e nutricionistas, com autenticação, controle de glicemia, gerenciamento de usuário, feedbacks, configurações e notificações. Atuei no back-end, incluindo o login com Google e iCloud. `C#` `.NET` `Docker`
  - [Backend do login com Google e iCloud](https://github.com/RuanPereiradev/Glicare-Login-Google-Icloud)
  - [Back-Glicare](https://github.com/RuanPereiradev/Back-Glicare)

<br>

<img src="assets/sec-tecnologias.svg" alt="Tecnologias" width="100%" />

<p align="center">
  <img src="https://skillicons.dev/icons?i=py,java,spring,ts,nestjs,react,nextjs,cs,dotnet,docker,postgres,redis,linux,git,github,vscode&theme=dark" alt="Tecnologias" />
</p>

<br>

<img src="assets/sec-contato.svg" alt="Contato" width="100%" />

- E-mail: [ruanpereira@alu.ufc.br](mailto:ruanpereira@alu.ufc.br)
- LinkedIn: [ruan-pereira-do-nascimento](https://www.linkedin.com/in/ruan-pereira-do-nascimento-ab6a45228/)
- Instagram: [@ruanpereira__](https://instagram.com/ruanpereira__)
