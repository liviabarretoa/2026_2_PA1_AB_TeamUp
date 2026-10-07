# Team Up: Jornada do Usuário & Histórias (MVP)

## Proto-persona
<div align="center">
<img width="800" alt="Carlos" src="https://github.com/user-attachments/assets/0cbf2053-1dc7-494c-89d3-65c392c5d884" />
</div>

## Jornada 1
**Persona:** Marina, a jogadora focada que quer subir de elo após o trabalho, mas está cansada da toxicidade da fila solo e não quer perder tempo com trolls.  
**Objetivo:** Encontrar um Duo compatível para jogar partidas ranqueadas de Valorant hoje à noite, confirmando se a pessoa tem boa reputação para garantir um jogo sem estresse no MVP.

### 1. Buscar jogadores por jogo, nível e disponibilidade
* **Descrição:** Aplicar filtros na plataforma para encontrar jogadores de Valorant, no mesmo elo (ex: Ouro/Platina), disponíveis no turno da noite, e ativar o filtro de gênero (ex: buscar apenas mulheres ou pessoas com perfil verificado).
* **Sentimento do usuário:** Quero achar alguém do meu nível rápido e que jogue no mesmo horário, sem dor de cabeça.
* **Touchpoint:** Tela: Busca e Filtros de Matchmaking (Jogos, Elo, Horário, Gênero).

### 2. Abrir o perfil do jogador (Match)
* **Descrição:** Selecionar um dos perfis sugeridos nos resultados para ver detalhes de estilo de gameplay (ex: se joga de Suporte ou Duelista), faixa etária e biografia.
* **Sentimento do usuário:** Preciso ver se o estilo de jogo dessa pessoa complementa o meu.
* **Touchpoint:** Tela: Perfil do Jogador.

### 3. Ver sistema de reputação e avaliações
* **Descrição:** Checar a nota (0 a 5 estrelas) e ler os feedbacks descritivos deixados por pessoas que já jogaram com ela anteriormente.
* **Sentimento do usuário:** Como ela tem 4.8 estrelas e dizem que tem uma comunicação ótima e não é tóxica, sinto segurança para mandar o convite.
* **Touchpoint:** Seção: Reputação & Reviews (na página de Perfil do Jogador).

### 4. Dar o "Match" / Enviar convite de conexão
* **Descrição:** Clicar no botão para conectar com a pessoa e abrir o chat interno do Team Up para trocar uma ideia rápida antes de ir pro jogo.
* **Sentimento do usuário:** Deu match! Agora é só combinar quem vai jogar em qual posição e passar o nick do jogo.
* **Touchpoint:** Ação/Tela: Botão "Conectar" e Chat Interno.

### 5. Adicionar no jogo e iniciar a call
* **Descrição:** Copiar o Riot ID (ou nick de outro jogo) fornecido no chat e adicionar no cliente do jogo, além de entrar em um canal de voz (Discord ou chat de voz do próprio jogo) de forma segura.
* **Sentimento do usuário:** Pronto, time formado com segurança. Vamos iniciar a partida.
* **Touchpoint:** Ação: Copiar Nick/ID e integração externa (Abrir Jogo / Discord).

## Histórias de Usuários

### 1. Acessar área do jogador e iniciar cadastro do Perfil

**Passo de Jornada**
- **Fase do Roadmap Estratégico:** Fase 1 – MVP de Conexão Segura e Perfil Gamer (Descoberta Básica)
- **Jornada de Usuário:** Marina, a jogadora focada e sem tempo – Cadastrar e manter um perfil gamer confiável (jogos, elo, horários e gênero) para garantir matches de qualidade e evitar toxicidade no MVP.
- **Passo:** Acessar área do jogador e iniciar cadastro do Perfil

**Geral**
- **Produto:** Team Up
- **Narrativa:** Como Marina, a jogadora focada e sem tempo, eu quero acessar a Área do Jogador (Home/Onboarding do Perfil) e iniciar o cadastro do meu Perfil Gamer para começar rapidamente a configurar minhas preferências e ser encontrada por parceiros ideais compatíveis.
- **Prioridade:** Alta | **Tipo:** Feature | **Tags:** onboarding, perfil, mvp

**Detalhes**
- **Descrição Detalhada:** Cobre o primeiro contato do jogador com a área de gestão do Perfil Gamer. O usuário deve ver seu status de configuração e um caminho óbvio para iniciar/continuar o cadastro. O sistema deve identificar se o usuário já tem um perfil cadastrado e levar para o painel de gestão com ações de “continuar configuração” ou “atualizar status”.
- **Orientações de Tela:** Título "Área do Jogador". Bloco de progresso (checklist): "Jogos e Nicks", "Nível e Elo", "Horários", "Preferências" com status. CTA primário: "Iniciar cadastro" ou "Continuar configuração". Link "Ver perfil público" desabilitado até existir perfil mínimo.
- **Regras de Negócio:** Se não possuir Perfil, exibir estado vazio. Se possuir cadastro incompleto, exibir checklist. O checklist considera "Perfil concluído" se ao menos 1 jogo, 1 elo e 1 horário estiverem preenchidos.

**BDD & Implementação**
- **Critérios de Aceitação (BDD):** Dado que estou autenticado e não possuo um Perfil cadastrado Quando eu acesso a Área do Jogador e clico em "Iniciar cadastro" Então o sistema deve abrir o fluxo de cadastro de Perfil no primeiro passo

---

### 2. Cadastrar/atualizar dados básicos do Perfil Gamer

**Passo de Jornada**
- **Fase do Roadmap Estratégico:** Fase 1 – MVP de Conexão Segura e Perfil Gamer
- **Jornada de Usuário:** Marina, a jogadora focada e sem tempo – Cadastrar e manter um perfil gamer confiável.
- **Passo:** Cadastrar/atualizar dados básicos do Perfil Gamer

**Geral**
- **Produto:** Team Up
- **Narrativa:** Como Marina, eu
