
TeamUp 🎮 — Matchmaking Tático para Gamers Competitivos

Matchmaking inteligente pré-partida para jogadores competitivos encontrarem duos e squads alinhados por elo, comunicação em tempo real, função tática e rotina de jogo.

🎯 Sobre o Projeto

Nos jogos competitivos por equipe (como Valorant, League of Legends e Counter-Strike), a maioria dos jogadores encara a chamada "fila solo" (Solo Queue). Essa experiência é frequentemente marcada por:

Comunicação inexistente ou ineficaz (jogadores sem microfone ou sem uso de chamadas táticas);

Toxicidade precoce e abandono de partidas, destruindo a pontuação competitiva (PDL/MMR);

Conflito de funções no time, onde múltiplos jogadores disputam a mesma rota ou função chave.

O TeamUp foi concebido na disciplina de Engenharia de Software para solucionar essa dor na raiz: uma camada de inteligência e afinidade pré-jogo que monta a equipe ideal antes de os jogadores iniciarem a fila oficial do servidor.

## Documentação do Projeto
Abaixo estão os documentos estratégicos e de pesquisa que fundamentam o desenvolvimento do Team Up:

* 📄 **[Visão do Produto e Escopo (É/Não É)](https://github.com/liviabarretoa/2026_2_PA1_AB_TeamUp/blob/main/matriz-de-alinhamento-%C3%A9-n%C3%A3o%20%C3%A9-faz-n%C3%A3o%20faz.md)**
* 📄 **[Matriz CSD & Mapa de Empatia](https://github.com/liviabarretoa/2026_2_PA1_AB_TeamUp/blob/main/matriz-csd.md)**
* 📄 **[Jobs To Be Done (JTBD)](https://github.com/liviabarretoa/2026_2_PA1_AB_TeamUp/blob/main/jobs-to-be-done(JTBD).md)**
* 📄 **[Problem-Solution Fit Canvas](https://github.com/liviabarretoa/2026_2_PA1_AB_TeamUp/blob/main/problem-solution-fit-canvas.md)**
* 📄 **[Business Model Canvas](https://github.com/liviabarretoa/2026_2_PA1_AB_TeamUp/blob/main/business-model-canvas.md)**
* 📄 **[Value Proposition Canvas](https://github.com/liviabarretoa/2026_2_PA1_AB_TeamUp/blob/main/the-value-proposition-canvas.md)**
* 📄 **[Jornada do Usuário e Histórias (MVP)](https://github.com/liviabarretoa/2026_2_PA1_AB_TeamUp/blob/main/jornadas-dos-usuarios.md)**
* 📄 **[Roadmap Estratégico](https://github.com/liviabarretoa/2026_2_PA1_AB_TeamUp/blob/main/roadmap-estrat%C3%A9gico.md)**

Visão do Produto e Escopo (É/Não É)Para manter o escopo técnico do MVP focado e viável, aplicamos a matriz de delimitação de fronteiras (É / Não É / Faz / Não Faz):O que o TeamUp ÉO que o TeamUp NÃO É• Uma plataforma utilitária de afinidade tática e pareamento pré-jogo.• Um filtro de confiabilidade comportamental e de perfil esportivo.• Não é uma rede social aberta com feed de fotos ou timeline genérica.• Não é um servidor de comunidade caótico de Discord aberto.O que o TeamUp FAZO que o TeamUp NÃO FAZ• Valida patentes e histórico competitivo via APIs públicas oficiais.• Filtra duos por funções complementares, uso ativo de microfone e turnos disponíveis.• Gera links instantâneos para salas de voz no Discord e lobbies.• Não substitui os servidores dos jogos (Riot Games, Valve, etc.).• Não altera algoritmos internos de balanceamento das desenvolvedoras.• Não atua durante a partida em tempo real no MVP.Matriz CSD & Mapa de Empatia"Entrar na fila solo sem duo é jogar uma moeda para cima: você tem 50% de chance de perder antes dos 10 minutos por desistência ou toxicidade."— Depoimento de jogador competitivo em pesquisa exploratória (Elo Platina/Diamante).1. Matriz CSD (Certezas, Suposições e Dúvidas)TipoDescriçãoComo Validamos / StatusCertezaToxicidade e ausência de comunicação são os maiores fatores de abandono do modo competitivo.Confirmado via pesquisa empírica com a comunidade gamer.CertezaJogadores em duo sincronizados por voz apresentam taxa de vitória superior à fila solo.Validado por dados históricos de telemetria e eSports.SuposiçãoJogadores aceitam parear com parceiros de elo ligeiramente diferente se houver garantia de boa comunicação e postura esportiva.Hipótese prioritária a ser aferida no piloto do MVP.SuposiçãoO tempo máximo tolerado pelo jogador para encontrar um match tático é de 3 minutos.A ser medido por métricas de retenção no fluxo de busca.DúvidaHaverá adesão voluntária e recorrente aos formulários rápidos de avaliação mútua pós-jogo?Teste A/B com avaliação em 1 clique vs. feedback opcional.DúvidaA exigência de login prévio com Discord/Riot aumentará a taxa de abandono no cadastro?Monitoramento do funil de conversão no onboarding.2. Mapa de Empatia do Gamer CompetitivoQuadranteO que o Jogador Vivencia no Cenário AtualO que ele VÊ?Jogadores desconectando no meio da partida (AFK), discussões no chat de texto, amigos pessoais jogando em turnos incompatíveis.O que ele OUVE?"Subir de elo na fila solo é impossível", streamers reclamando da comunidade, ausência de chamadas táticas em jogadas críticas.O que ele PENSA e SENTE?Frustração ao perder pontos por culpa de terceiros, receio de abrir o jogo sozinho após um dia cansativo, desejo de competir a sério.O que ele FALA e FAZ?Tenta buscar duos em grupos caóticos de Discord, desiste da partida após sequências de partidas tóxicas, busca evoluir sua mecânica.Dores (Pains)Queda injusta de ranking (PDL/MMR), desgaste psicológico, perda de tempo com partidas desequilibradas.Ganhos (Gains)Subida consistente de elo, segurança psicológica para jogar, sinergia de jogadas e amizades confiáveis para squads fixos.Jobs To Be Done (JTBD)Declaração Central (Core Job Statement)"Quando eu vou disputar partidas ranqueadas competitivas,eu quero encontrar um parceiro com funções táticas complementares e boa comunicação,para que eu possa subir de elo de forma consistente e sem o desgaste psicológico da fila solo."As Três Dimensões do Job:Dimensão Funcional: Encontrar em menos de 3 minutos um jogador do mesmo patamar de habilidade que queira jogar na posição complementar à minha (ex.: suporte para meu atirador, iniciador para meu duelista).Dimensão Emocional: Jogar com segurança psicológica, sabendo que o parceiro não dará rage nem abandonará a partida no primeiro erro.Dimensão Social: Ter parceiros fixos de confiança para montar squads, trocar experiências e participar de torneios comunitários e universitários.Problem-Solution Fit CanvasProblema EmpíricoImpacto na ExperiênciaSolução de Engenharia no TeamUpFila Solo TóxicaAnsiedade, perda injusta de PDL e desmotivação geral.Índice de Reputação Comunitária: pareamento baseado em histórico comportamental mútuo.Conflito de Rotas/FunçõesDois jogadores querendo atuar na mesma função desestabilizam a formação tática.Filtro Estrito de Funções: pareamento automático entre função primária e secundária compatíveis.Falta de MicrofonePerda de chamadas decisivas em frações de segundo.Checagem de Voz Pré-Lobby: exigência opcional de canal de voz Discord ativo para a sessão.Desencontro de RotinaAmigos pessoais nunca estão online no mesmo horário.Janelas de Agenda: cruzamento de horários disponíveis recorrentes (ex.: terças e quintas à noite).Business Model CanvasSegmento de Clientes: Gamers competitivos de patentes intermediárias e altas (Ouro, Platina, Diamante, Imortal) com frequência de 3+ sessões semanais.Proposta de Valor: Matchmaking confiável baseado em sinergia tática e comportamental pré-jogo.Canais de Distribuição: Bot nativo em servidores gamers parceiros de Discord (/teamup), comunidades universitárias de eSports e compartilhamento entre duos.Parcerias Chave: APIs públicas da Riot Games e Valve (validação de contas) e API do Discord (automação de canais de voz temporários).Fontes de Receita:Camada Gratuita (Freemium): Pareamento individual, filtros básicos de elo e histórico recente.TeamUp Pro (Assinatura): Análise preditiva de sinergia entre duplas, estatísticas detalhadas de vitórias conjuntas e criação ilimitada de times 5x5.Estrutura de Custos: Hospedagem de infraestrutura em nuvem, banco de dados Redis de alta velocidade e consumo de cotas de APIs.Value Proposition Canvas     ┌─────────────────────────────────────┐         ┌─────────────────────────────────────┐
     │       MAPA DE VALOR (TeamUp)        │         │         PERFIL DO JOGADOR           │
     ├─────────────────────────────────────┤         ├─────────────────────────────────────┤
     │  Aliviadores de Dor:                │   ===>  │  Dores:                             │
     │  • Filtros anti-toxicidade e elo    │         │  • Trolls e abandonos prematuros    │
     │  • Confirmação prévia de voz/mic    │         │  • Perda injusta de pontos de liga  │
     │                                     │         │                                     │
     │  Criadores de Ganho:                │   ===>  │  Ganhos Desejados:                  │
     │  • Sinergia de jogo e entrosamento  │         │  • Subida consistente de ranking    │
     │  • Winrate consistente em duplas    │         │  • Partidas prazerosas e focadas    │
     └─────────────────────────────────────┘         └─────────────────────────────────────┘
Jornada do Usuário e Histórias (MVP)[ 1. Onboarding ] ──▶ [ 2. Filtros ] ──▶ [ 3. Match ] ──▶ [ 4. Feedback ]
 Conexão de conta       Definição de       Entrada no lobby       Avaliação rápida
  Riot / Discord         função e voz       sem burocracia         em 1 clique
Histórias de Usuário com Critérios BDD (Gherkin)🔹 US01 — Autenticação e Importação de Perfil GamerComo jogador competitivo,quero autenticar minha conta de jogo (Riot ID / Steam),para que minha patente e histórico sejam validados de forma transparente e sem fraudes.Cenário: Autenticação bem-sucedida de jogador
  Dado que o usuário está na tela de login
  Quando ele seleciona a opção "Conectar com Riot Games" e autoriza o acesso
  Então o sistema deve importar automaticamente seu Riot ID, Rank atual e taxa de vitória recente
  E exibir essas informações no seu Player Card público.
🔹 US02 — Busca por Afinidade TáticaComo usuário pronto para jogar,quero filtrar parceiros por função desejada e exigência de microfone,para que eu encontre alguém adequado à estratégia que pretendo adotar.Cenário: Filtragem com microfone obrigatório
  Dado que o jogador é Suporte e busca um Atirador (ADC)
  Quando ele marca o filtro "Exigir microfone ativo no Discord"
  Então a listagem de duos disponíveis deve ocultar qualquer perfil sem confirmação de voz ativa.
🔹 US03 — Geração Imediata de Sala / LobbyComo jogador pareado com um duo,quero receber um link direto para entrar no canal de voz e lobby,para que não percamos tempo trocando tags de amizade manualmente.Cenário: Aceite mútuo de pareamento
  Dado que dois jogadores se deram match mútuo
  Quando ambos clicam em "Aceitar Duo"
  Então o TeamUp deve criar temporariamente uma sala privada no Discord
  E disponibilizar o botão de "Entrar no Lobby do Jogo".
🔹 US04 — Avaliação de Conduta Pós-PartidaComo usuário que concluiu uma partida com um parceiro do TeamUp,quero enviar uma avaliação rápida de conduta,para que o ecossistema mantenha uma comunidade livre de jogadores desrespeitosos.Cenário: Feedback rápido em um clique
  Dado que a partida entre a dupla foi finalizada
  Quando o sistema solicita a avaliação rápida
  Então o usuário pode selecionar selos como "Comunicação Clara", "Pontual" ou "Tóxico"
  E a pontuação de reputação do parceiro é recalculada no banco de dados.
Roadmap Estratégico[ Fase 1: MVP Atual ] ────────▶ [ Fase 2: Expansão ] ────────▶ [ Fase 3: Escala ]
• Autenticação e perfil         • Algoritmo de sinergia         • Leitura via telemetria
• Filtro manual (elo/rota)       • Bot oficial de Discord        • Formação de times 5x5
• Geração de sala de voz         • Selos de reputação            • Campeonatos amadores
• Feedback pós-jogo básico       • Métricas de winrate em duo    • Assinatura Pro
🛠️ Tecnologias & Arquitetura PrevistaFrontend: React.js / Vite com Tailwind CSS (design dark mode tático).Backend: Node.js (Express / Fastify) para arquitetura de microserviços orientada a eventos.Banco de Dados: PostgreSQL (dados relacionais de usuários e partidas) + Redis (fila de matchmaking em tempo real).Integrações:Riot Games API / Tracker API: consulta de patentes e histórico competitivo.Discord Developer Portal: OAuth2 e automação de canais de voz temporários.💻 Como Executar o Projeto LocalmentePré-requisitosNode.js versão 18 ou superior instalado;Gerenciador de pacotes npm ou yarn;Git configurado.Passo a Passo# 1. Clone o repositório
git clone https://github.com/liviabarretoa/2026_2_PA1_AB_TeamUp.git

# 2. Acesse a pasta do projeto
cd 2026_2_PA1_AB_TeamUp

# 3. Instale as dependências
npm install

# 4. Configure as variáveis de ambiente
cp .env.example .env

# 5. Inicie o servidor de desenvolvimento
npm run dev
Abra http://localhost:5173 no seu navegador para acessar a aplicação localmente.👥 Equipe & ContribuiçãoEste projeto é desenvolvido como parte da disciplina de Engenharia de Software (Projeto Aplicado 1 - 2026.2).Lívia Barreto — Engenharia de Software & Descoberta de Produto — GitHubContribuições e sugestões são bem-vindas via Pull Requests ou abertura de Issues.

