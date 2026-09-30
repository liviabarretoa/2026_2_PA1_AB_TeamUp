# 🎮 TeamUp — Plataforma de Matchmaking Competitivo

![Status](https://img.shields.io/badge/Status-Em_Desenvolvimento-blue?style=for-the-badge)
![Foco](https://img.shields.io/badge/Foco-eSports_%26_Ranked-orange?style=for-the-badge)
![Metodologia](https://img.shields.io/badge/Metodologia-BDD_%26_Discovery-green?style=for-the-badge)
![Curso](https://img.shields.io/badge/Engenharia_de_Software-UNIFOR-002B49?style=for-the-badge)

> Conectando jogadores (casuais ou competitivos) por sinergia comportamental, funções complementares e horários compatíveis. O fim da roleta-russa da fila solo (*Solo Queue*).

---

## 🎯 Visão do Produto e Escopo (É/Não É)

Definição clara das fronteiras e do propósito do sistema para manter o alinhamento da equipe de engenharia e evitar desvios de escopo (*scope creep*):

| Dimensão | Definição Estratégica |
| :--- | :--- |
| **É** | Uma plataforma inteligente de matchmaking pré-jogo focada em parear duos e squads com base em compatibilidade de rotas, estilo de comunicação e índice de fair play. |
| **NÃO É** | Uma rede social generalista de jogos, um cliente de jogo independente (*launcher*) ou um fórum desorganizado de postagens. |
| **FAZ** | Filtragem granular por função/elo, criação de cards de jogador, mediação de convites mútuos e envio automático de link para sala de voz do Discord. |
| **NÃO FAZ** | Não altera o matchmaking interno dos servidores do jogo, não garante vitória em partidas e não atua como coach tático automatizado. |

---

## 🧠 Matriz CSD & Mapa de Empatia

### Matriz CSD (Certezas, Suposições e Dúvidas)

| Categoria | Descrição | Status de Validação |
| :--- | :--- | :--- |
| **Certeza** | Jogadores solo sofrem com alta taxa de toxicidade, desistências (AFK) e falta de comunicação no pareamento automático padrão. | Validado com a comunidade gamer. |
| **Suposição** | Usuários competitivos priorizam sinergia de voz e maturidade comportamental antes mesmo da exata paridade numérica de elo. | Em teste de usabilidade. |
| **Dúvida** | Qual será a taxa real de engajamento no preenchimento do formulário mútuo de avaliação comportamental pós-jogo? | Métrica prioritária do MVP. |

### Mapa de Empatia do Jogador Competitivo

| Quadrante | O que o usuário vivencia |
| :--- | :--- |
| **O que ele pensa e sente?** | Sente-se desmotivado para jogar e para tentar criar uma relação de amizade com outros jogadores. |
| **O que ele ouve?** | Ouve críticas recorrentes sobre o mau funcionamento e a ineficiência do sistema de denúncias e banimentos dentro do jogo. |
| **O que ele vê?** | Considera a comunidade muito grande e, por isso, percebe que ela pode ser bastante tóxica. |
| **O que ele fala e faz?** | Evita ativamente interagir com jogadores que não são seus conhecidos. |
| **Dores do Usuário** | Afasta-se da comunidade e bloqueia a comunicação no jogo, mesmo quando ela é necessária para a partida, se sente estressado e ansioso. |
| **Ganhos Almejados** | Conseguir encontrar pessoas compatíveis e formar laços, se sentir seguro dentro da comunidade. |

---

## 💼 Jobs To Be Done (JTBD)

> **Declaração Central:**
> *"Quando estou prestes a iniciar minha sessão diária de partidas, eu quero encontrar um duo ou time alinhado à minha rota, maturidade e estilo de comunicação, para que eu possa me divertir jogando, sem me estressar com toxicidade."*

O TeamUp resolve as dores e necessidades da comunidade gamer, criando um ecossistema focado no respeito mútuo, ideal tanto para sessões de jogo casuais e descontraídas quanto para o cenário competitivo.

*   **Dimensão Funcional (O que o usuário precisa fazer):**
    *   Encontrar pessoas para jogar e adicionar horários disponíveis para jogar.
    *   Filtrar parceiros por estilo de jogo, nível de habilidade, gênero, etc.
    *   Acessar um lugar que tenha uma boa avaliação de conduta dos jogadores e autenticar a idade dos usuários.

*   **Dimensão Emocional (Como o usuário quer se sentir):**
    *   Sentir-se confiante, acolhido e com o controle da experiência de jogo.
    *   Sentir tranquilidade por ter informações confiáveis e atualizadas do jogador, além de controle sobre a reputação para garantir matches mais adequados.
    *   Sentir segurança e confiança ao jogar e interagir com outras pessoas que mantenham o respeito e a harmonia durante as partidas.

*   **Dimensão Social (Como o usuário quer ser visto):**
    *   Ser reconhecido na comunidade como um parceiro tático confiável e construir uma rede sólida de duos.
    *   Ser reconhecido como confiável pelo comportamento saudável e ser recomendado por ter cumprido as regras.
    *   Ser visto como alguém valorizado por dar visibilidade ao aplicativo para mais visitas.

---

## 🧩 Problem-Solution Fit Canvas

O **TeamUp** foi estruturado para resolver as principais frustrações dos jogadores de jogos online. Entendemos que a diversão pode ser arruinada tanto em partidas competitivas quanto nas casuais devido à dependência de filas aleatórias (*solo queue*) e ao comportamento hostil.

Abaixo detalhamos como conectamos os problemas vividos pela comunidade com as nossas soluções:

### O Problema vs. A Solução

*   **Fila Solo Caótica & Dependência do Aleatório:**
    *   *A Causa:* Os algoritmos oficiais de pareamento focam exclusivamente no tempo de fila e no nível técnico/elo bruto, ignorando totalmente o temperamento, a afinidade interpessoal e o objetivo de jogo.
    *   *A Solução do TeamUp:* Pareamento baseado no histórico de conduta e na reputação do usuário, a qual é avaliada ativamente por outros jogadores da comunidade.
    *   *Métrica de Sucesso:* Redução de 80% nos relatos de toxicidade nos grupos formados pela plataforma.

*   **Incompatibilidade no Jogo e Falta de Sincronia:**
    *   *A Causa:* É comum dois jogadores que usam a mesma posição caírem juntos e disputarem espaço. Além disso, a falta de sincronia de horários faz com que o jogador perca tempo procurando companhia no momento em que está livre.
    *   *A Solução do TeamUp:* Filtros estritos por função primária e secundária antes de iniciar a busca, além de filtros por horários, estilo de jogo e nível de habilidade.
    *   *Métrica de Sucesso:* 100% de compatibilidade nas funções (rotas) dos times criados.

*   **Comunicação Falha, Assédio e Anonimato:**
    *   *A Causa:* Falta de coordenação por voz antes do início das partidas. Pior do que isso, o anonimato nos jogos gera impunidade para comportamentos tóxicos, o que afeta especialmente as mulheres, que evitam se comunicar por medo de sofrer assédio e machismo.
    *   *A Solução do TeamUp:* Um sistema bilateral de reputação (0 a 5 estrelas) com recortes e filtros de segurança focados em gênero. Além disso, o aplicativo conta com integração nativa com a API do Discord para a criação direta de salas privativas de voz.
    *   *Métrica de Sucesso:* Menos de 2 minutos para conectar os jogadores em uma chamada de voz após o match.

---

## 📊 Business Model Canvas

O modelo de negócios do **TeamUp** foi estruturado para ser sustentável, escalável e centrado na experiência da comunidade (abrangendo desde os jogadores focados em diversão casual até os mais competitivos).

*   **Proposta de Valor:** Matchmaking pré-jogo baseado em sinergia de funções, comportamento verificado e integração de voz. Oferecemos um ambiente seguro e previsível (com filtros exclusivos, como o de gênero) que reduz drasticamente o assédio e a toxicidade.

*   **Segmentos de Clientes:** Gamers casuais e competitivos de títulos em equipe (como League of Legends, Valorant, CS2 ou Overwatch 2) que jogam sozinhos (*solo queue*) e sofrem com a aleatoriedade de parceiros.

*   **Canais:** Plataformas de acesso via Web App responsivo, integração nativa via bot de Discord e divulgação orgânica em comunidades. Expansão via aplicativos mobile (Android e iOS) e marketing de influência.

*   **Relacionamento com Clientes:** Baseado em um sistema comunitário de reputação com moderação ativa. Foco total no autosserviço (navegação por *cards*) e incentivo constante à cultura de respeito mútuo.

*   **Fontes de Receita:** Modelo Freemium, sendo gratuito para buscas básicas, com a opção de um plano Pro oferecendo estatísticas avançadas, filtros ilimitados e badges exclusivas. Complementado por anúncios segmentados não invasivos e microtransações cosméticas para o perfil.

*   **Recursos-Chave:** Algoritmo proprietário de compatibilidade de duos, banco de dados seguro e integração com APIs oficiais de jogos. Contamos também com uma equipe centralizada de Devs, UI/UX e Moderação.

*   **Atividades-Chave:** Desenvolvimento contínuo, aprimoramento constante do algoritmo de pareamento e moderação comunitária (incluindo proteção contra *review bombing* e contas falsas).

*   **Parcerias-Chave:** Integrações estratégicas com Discord Developer Platform, Riot Games API, Steam Developer e colaboração com ligas amadoras de eSports. Parcerias sociais com coletivos gamers e criadores de conteúdo (streamers) focados em ambientes saudáveis.

*   **Estrutura de Custos:** Manutenção de servidores em nuvem, banco de dados em tempo real e infraestrutura de rede. Custos adicionais com taxas de lojas de aplicativos (Apple/Google), marketing de aquisição e equipe de suporte.
---

## 💎 Value Proposition Canvas

### 👤 1. Perfil do Cliente

*   **Tarefas do Cliente:** Encontrar parceiros com uma *vibe* parecida, garantir uma comunicação clara por voz e jogar sem estresse com pessoas que curtem o mesmo ritmo.
*   **Dores:** Entrar em partidas com jogadores tóxicos, lidar com parceiros que desaparecem no meio do jogo (AFK), sentir-se isolado ou desconfortável e sofrer ansiedade antes de jogar com desconhecidos.
*   **Ganhos:** Jogar de forma relaxada, encontrar pessoas que priorizam o respeito, construir amizades que duram e subir de elo sem medo.

---

### 🗺️ 2. Mapa de Valor

*   **Produtos e Serviços:** Plataforma que conecta jogadores por compatibilidade, *Player Cards* com filtros customizáveis (elo, função, comunicação e valores compartilhados) e acesso a uma sala de voz direta.
*   **Aliviadores de Dores:** Sistema de reputação comunitária que identifica quem é respeitoso, filtros que protegem ativamente contra comportamentos tóxicos e moderação ativa da comunidade.
*   **Criadores de Ganho:** *Match* com pessoas que compartilham dos mesmos valores, sistema de avaliação mútua que celebra a boa conduta e um espaço seguro para conversar antes de iniciar a partida.
---

## 🚀 Jornada do Usuário e Histórias (MVP)

A jornada principal do produto foi estruturada do onboarding até a avaliação final:
1. **Cadastro e Perfil:** Vinculação de ID do jogo, seleção de elo, horários habituais e funções principais.
2. **Exploração de Parceiros:** Aplicação de filtros táticos para visualizar o mural de *Player Cards*.
3. **Conexão e Partida:** Envio de solicitação, aceite mútuo e direcionamento automático para a sala de voz.
4. **Ciclo de Feedback:** Avaliação rápida do comportamento do parceiro após o término da sessão.

---

### 🗺️ Jornada Prática
**Persona:** Marina, uma jogadora que quer curtir o jogo e evoluir no seu próprio ritmo após o trabalho, mas está cansada da toxicidade da fila solo e não quer perder tempo com interações desgastantes.
**Objetivo:** Encontrar um parceiro (Duo) compatível para jogar partidas de Valorant hoje à noite, confirmando a boa reputação da pessoa para garantir uma sessão sem estresse.

**1. Buscar jogadores por jogo, nível e disponibilidade**
*   **Descrição:** Aplicar filtros na plataforma para encontrar jogadores de Valorant no mesmo nível de habilidade, disponíveis no turno da noite, e ativar o filtro de gênero (ex: buscar apenas mulheres ou pessoas com perfil verificado).
*   **Sentimento:** "Quero achar alguém com a mesma vibe e no mesmo horário, sem dor de cabeça."

**2. Abrir o perfil do jogador (Match)**
*   **Descrição:** Selecionar um dos perfis sugeridos para ver detalhes de estilo de gameplay, faixa etária e biografia.
*   **Sentimento:** "Preciso ver se o estilo e os objetivos dessa pessoa batem com os meus."

**3. Ver sistema de reputação e avaliações**
*   **Descrição:** Checar a nota (0 a 5 estrelas) e ler os feedbacks descritivos deixados por parceiros anteriores.
*   **Sentimento:** "Como ela tem 4.8 estrelas e dizem que a comunicação é ótima e sem toxicidade, sinto segurança para mandar o convite."

**4. Dar o "Match" / Enviar convite de conexão**
*   **Descrição:** Clicar em conectar e abrir o chat interno do TeamUp para trocar uma ideia rápida antes do jogo.
*   **Sentimento:** "Deu match! Agora é só combinar as posições e passar o nick."

**5. Adicionar no jogo e iniciar a call**
*   **Descrição:** Copiar o Riot ID, adicionar no jogo e entrar em um canal de voz de forma segura.
*   **Sentimento:** "Pronto, dupla formada com segurança. Vamos jogar!"

---

### 📖 Histórias de Usuário em BDD (Behavior-Driven Development)

#### US01: Filtragem por Função e Nível
> **Como** jogador 
> **Quero** filtrar perfis por elo compatível, gênero ou função complementar  
> **Para que** eu não entre em partidas com choque de rotas ou disparidade de nível técnico.

#### US02: Acessar área do jogador e iniciar cadastro do Perfil Gamer
**Jornada de Usuário:** Lucas, um jogador cansado de filas solo aleatórias – Cadastrar e manter um perfil gamer preciso (jogos, nível, horários e estilo) para garantir matchs de qualidade e evitar companhias tóxicas.

> **Como** Lucas, um jogador que busca times parceiros e sem toxicidade  
> **Eu quero** acessar a área de Perfil e iniciar a configuração das minhas preferências  
> **Para** começar rapidamente a ser pareado com outros jogadores compatíveis e jogar em um ambiente seguro.

*   **Prioridade:** Alta (Essencial para habilitar o core business de matchmaking)
*   **Tags:** `onboarding`, `perfil`, `matchmaking`, `mvp`

**Orientações de Tela & Regras de Negócio (Resumo):**
*   **Checklist de Progresso:** "Jogos e Contas", "Nível", "Horários", "Estilo de Jogo".
*   **Chamadas para Ação (CTAs):** "Criar Perfil" ou "Completar Perfil".
*   **Regra Core:** O perfil mínimo exige 1 jogo selecionado, 1 Nickname/ID correspondente e 1 turno de disponibilidade. Sem isso, o acesso à tela de Matchmaking é bloqueado.

**Critérios de Aceitação (BDD):**
> **Cenário 1: Acesso inicial sem Perfil cadastrado**  
> **Dado que** estou autenticado na plataforma e não possuo preferências configuradas  
> **Quando** eu acesso a Área do Jogador e clico em "Criar Perfil"  
> **Então** o sistema deve abrir o fluxo de onboarding no primeiro passo (Seleção de Jogos).

> **Cenário 2: Acesso com cadastro incompleto**  
> **Dado que** possuo um perfil com cadastro incompleto (ex: escolhi os jogos, mas não informei os horários)  
> **Quando** eu acesso a Área do Jogador e clico em "Completar Perfil"  
> **Então** o sistema deve me levar automaticamente para a etapa pendente.

---

## 🗺️ Roadmap Estratégico

| Fase | Foco Estratégico | Entregáveis Principais |
| :--- | :--- | :--- |
| **Fase 1 (Atual)** | **Descoberta & MVP** | CSD, Canvas, BDDs aprovados, telas de cadastro, mural de perfis e autenticação. |
| **Fase 2** | **Conexão & Automação** | Chat interno em tempo real, integração direta com bot de Discord e sistema de feedback pós-jogo. |
| **Fase 3** | **Expansão de Plataforma** | Validação automatizada de dados via Riot/Steam API e sistema de formação de equipes completas (5v5). |

---

## 👥 Equipe do Projeto

* **Lívia Maria Barreto Albuquerque / 2526422**
* **Manuelly Rodrigues Pessoa / 2522733**
* **Maria Rafaele Gomes de Araújo / 2618240**
* **Rômulo Azevedo Montenegro Neto / 2526043**
* *Projeto acadêmico desenvolvido na Universidade de Fortaleza (UNIFOR).*
