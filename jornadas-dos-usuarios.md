# Team Up: Jornada do Usuário & Histórias (MVP)

## 📍 Jornada 1
**Persona:** Marina, a jogadora focada que quer subir de elo após o trabalho, mas está cansada da toxicidade da fila solo e não quer perder tempo com trolls.  
**Objetivo:** Encontrar um Duo compatível para jogar partidas ranqueadas de Valorant hoje à noite, confirmando se a pessoa tem boa reputação para garantir um jogo sem estresse no MVP.

### 1. Buscar jogadores por jogo, nível e disponibilidade
* **Descrição:** Aplicar filtros na plataforma para encontrar jogadores de Valorant, no mesmo elo (ex: Ouro/Platina), disponíveis no turno da noite, e ativar o filtro de gênero (ex: buscar apenas mulheres ou pessoas com perfil verificado).
* **Sentimento do usuário:** Quero achar alguém do meu nível rápido e que jogue no mesmo horário, sem dor de cabeça.
* **Touchpoint:** Tela: Busca e Filtros de Matchmaking (Jogos, Elo, Horário, Gênero).

### 2. Abrir o perfil do jogador (Match)
* **Descrição:** Selecionar um dos perfis sugeridos nos resultados para ver detalhes de estilo de gameplay (ex: se joga de Suporte ou Duelista), faixa etária e biografia.
* **Sentimento do usuário:** Preciso ver se o estilo de jogo dessa pessoa complementa o meu e se a vibe bate.
* **Touchpoint:** Tela: Perfil do Jogador.

### 3. Ver sistema de reputação e avaliações
* **Descrição:** Checar a nota (0 a 5 ⭐) e ler os feedbacks descritivos deixados por pessoas que já jogaram com ela anteriormente.
* **Sentimento do usuário:** Legal, ela tem 4.8 estrelas e dizem que tem uma comunicação ótima e não dá "rage". Sinto segurança para mandar o convite.
* **Touchpoint:** Seção: Reputação & Reviews (na página de Perfil do Jogador).

### 4. Dar o "Match" / Enviar convite de conexão
* **Descrição:** Clicar no botão para conectar com a pessoa e abrir o chat interno do Team Up para trocar uma ideia rápida antes de ir pro jogo.
* **Sentimento do usuário:** Deu match! Agora é só combinar quem vai jogar em qual posição e passar o nick do jogo.
* **Touchpoint:** Ação/Tela: Botão "Conectar" e Chat Interno.

### 5. Adicionar no jogo e iniciar a call
* **Descrição:** Copiar o Riot ID (ou nick de outro jogo) fornecido no chat e adicionar no cliente do jogo, além de entrar em um canal de voz (Discord ou chat de voz do próprio jogo) de forma segura.
* **Sentimento do usuário:** Pronto, time formado com segurança. Bora puxar a partida!
* **Touchpoint:** Ação: Copiar Nick/ID e integração externa (Abrir Jogo / Discord).

---

## 📚 Histórias de Usuários

### Acessar área do jogador e iniciar cadastro do Perfil Gamer

#### Passo de Jornada
* **Fase do Roadmap Estratégico:** Fase 1 – MVP de Conexão e Perfil Seguro (Onboarding e Matchmaking)
* **Jornada de Usuário:** Lucas, o jogador competitivo cansado de filas solo – Cadastrar e manter um perfil gamer preciso (jogos, elo, horários e estilo) para garantir matchs de qualidade e evitar toxicidade no MVP.
* **Passo:** Acessar área do jogador e iniciar a configuração do Perfil Gamer.

#### 📝 Geral
* **Produto:** Team Up
* **Título:** Acessar área do jogador e iniciar cadastro do Perfil Gamer
* **Narrativa:** 
  > **Como** Lucas, um jogador que busca times focados e sem toxicidade  
  > **Eu quero** acessar a área de Perfil (Home/Onboarding do Usuário) e iniciar a configuração das minhas preferências e contas  
  > **Para** começar rapidamente a ser pareado com outros jogadores compatíveis e poder jogar em um ambiente seguro.
* **Prioridade:** Alta (Essencial para habilitar o core business de matchmaking)
* **Tipo:** Feature
* **Coluna:** Análise
* **Subcoluna:** Buffer
* **Estimativa (pontos):** —
* **Tags:** `onboarding`, `perfil`, `matchmaking`, `mvp`

#### 🔍 Detalhes
**Descrição Detalhada:**  
Esta história cobre o primeiro contato do jogador com a área de gestão do seu perfil dentro do Team Up, garantindo um início rápido e guiado. Ao entrar na Área do Jogador, o usuário deve ver seu status de configuração (contas de jogos vinculadas, disponibilidade de horários, elo/ranque e estilo de gameplay) e um caminho óbvio para iniciar/continuar o cadastro. A experiência deve priorizar fluidez, reduzindo a fricção para que o jogador possa ir para a busca de duos o mais rápido possível. O sistema deve identificar se o usuário já tem um perfil ativo e, caso tenha, levar para o painel de gestão com ações de "continuar configuração" ou "atualizar status" (ex: mudar de 'disponível para jogar' para 'ausente'). Caso não tenha, deve iniciar um fluxo de onboarding com progresso visível e salvamento automático.

#### 🎨 Orientações de Tela
* **Título:** "Meu Perfil Gamer"
* **Subtítulo/boas-vindas:** "Configure suas preferências para encontrarmos o seu duo ou squad ideal."
* **Bloco de progresso (checklist):** "Jogos e Contas (Nicks)", "Nível e Elo", "Horários", "Estilo de Jogo" com status (Pendente/Em andamento/Concluído).
* **CTA primário:** "Criar Perfil" (se novo) ou "Completar Perfil" (se incompleto).
* **CTA secundário:** "Atualizar Status de Jogo" (sempre visível se o perfil estiver ativo, ex: "Buscando partida agora").
* **Seção "Próxima ação recomendada":** mostra o próximo passo mais importante (ex.: "Vincule seu Riot ID para encontrar jogadores de Valorant").
* **Link "Ver como os outros me veem":** (desabilitado até existir um perfil mínimo).
* **Mensagem de segurança/privacidade curta:** "Seus dados de jogo são usados apenas para pareamento. Você pode alterar seus filtros a qualquer momento."
* **Estado vazio (sem perfil):** ilustração gamificada + texto "Você ainda não configurou seu perfil para dar match."
* **Feedback de carregamento:** skeleton/loader para o checklist e os cards de status.

#### ⚙️ Regras de Negócio
1. Se o usuário não possuir um perfil configurado, exibir estado vazio e CTA "Criar Perfil", bloqueando o acesso à tela de Matchmaking.
2. Se o usuário possuir um perfil incompleto, exibir checklist com percentuais e CTA "Completar Perfil", levando diretamente à primeira etapa pendente.
3. O checklist deve considerar o "Perfil Mínimo" concluído apenas se: pelo menos 1 jogo estiver selecionado, o Nickname/ID correspondente for preenchido e ao menos 1 turno de disponibilidade (ex: Noite) estiver marcado.
4. O link "Ver como os outros me veem" só deve ser habilitado quando o Perfil Mínimo for atingido.
5. Exibir mensagens de erro amigáveis se falhar o carregamento do status do banco de dados com a opção "Tentar novamente".
6. Manter estado de progresso sincronizado com o backend (salvamento a cada etapa concluída no onboarding); não confiar apenas em cache local.

#### 🛠️ BDD & Implementação

**Critérios de Aceitação (BDD)**

> **Cenário 1: Acesso inicial sem Perfil cadastrado**  
> **Dado que** estou autenticado na plataforma e não possuo preferências de jogo configuradas  
> **Quando** eu acesso a Área do Jogador  
> **E** eu clico em "Criar Perfil"  
> **Então** o sistema deve abrir o fluxo de onboarding no primeiro passo (Seleção de Jogos).

> **Cenário 2: Acesso com cadastro incompleto**  
> **Dado que** estou autenticado e possuo um perfil com cadastro incompleto (ex: escolhi os jogos, mas não informei os horários)  
> **Quando** eu acesso a Área do Jogador  
> **E** eu clico em "Completar Perfil"  
> **Então** o sistema deve me levar automaticamente para a etapa pendente ("Disponibilidade/Horários").

> **Cenário 3: Acesso com falha de carregamento**  
> **Dado que** estou autenticado  
> **Quando** eu acesso a Área do Jogador  
> **E** ocorre uma falha de conexão com a API ao carregar o status do meu perfil  
> **Então** o sistema deve exibir um toast/mensagem de erro amigável e um botão "Tentar novamente", mantendo a interface base renderizada de forma segura.

**Orientações para Implementação:**
* Implementar salvamento e leitura do status por endpoint único (ex.: `/api/users/profile/status`) para reduzir o tempo de carregamento na tela inicial.
* Usar skeleton loading para os cards de jogos e checklist, evitando saltos de layout (CLS - Cumulative Layout Shift).
* Registrar eventos de analytics essenciais para o MVP: `view_profile_home`, `click_start_onboarding`, `click_continue_onboarding`.
* Definir "próxima ação recomendada" no backend com base na prioridade do funil de matchmaking (Prioridade: Vincular Conta > Informar Elo > Definir Horários > Bio/Preferência de Gênero).
* Garantir responsividade fluida no mobile, visto que muitos jogadores usam o celular para buscar parceiros enquanto o jogo está abrindo no PC/Console.
