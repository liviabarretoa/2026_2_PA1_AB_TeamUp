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
- **Narrativa:** Como Marina, eu quero editar as informações do meu Perfil (jogos, elo, gênero e horários) para padronizar meu perfil e torná-lo encontrável para parceiros compatíveis.
- **Prioridade:** Alta | **Tipo:** Feature | **Tags:** cadastro, preferencias, matchmaking

**Detalhes**
- **Descrição Detalhada:** A tela deve orientar o usuário a preencher os jogos que joga, elo/nível, gênero (para filtros de segurança) e horários disponíveis. O sistema deve validar campos obrigatórios, permitir salvar rascunho e publicar.
- **Orientações de Tela:** Campos de "Nick do Jogo / Riot ID", "Jogos" (multi-seleção), "Elo/Ranque Atual" (dropdown dinâmico) e "Horários". Componente de "Pré-visualização rápida" do card.
- **Regras de Negócio:** Nick do jogo é obrigatório. Obrigatório selecionar pelo menos 1 jogo e Elo correspondente. Ao salvar, registrar evento analytics: perfil_salvo.

**BDD & Implementação**
- **Critérios de Aceitação (BDD):** Dado que estou na tela "Perfil Gamer" Quando preencho "Nick", seleciono ao menos 1 "Jogo" e "Elo", e toco em "Salvar" Então devo ver mensagem de sucesso e os dados devem permanecer ao reabrir a tela

---

### 3. Visualizar mural de parceiros e aplicar filtros táticos

**Passo de Jornada**
- **Fase do Roadmap Estratégico:** Fase 1 – MVP de Conexão Segura e Perfil Gamer
- **Jornada de Usuário:** Marina, a jogadora focada e sem tempo – Encontrar um parceiro visualizando perfis compatíveis.
- **Passo:** Visualizar mural de Player Cards e aplicar filtros básicos.

**Geral**
- **Produto:** Team Up
- **Narrativa:** Como Marina, eu quero visualizar uma lista/mural de perfis de jogadores e usar filtros de elo, gênero e horário para encontrar parceiros que atendam exatamente às minhas necessidades de segurança e compatibilidade.
- **Prioridade:** Alta | **Tipo:** Feature | **Tags:** matchmaking, filtros, player-cards

**Detalhes**
- **Descrição Detalhada:** O usuário terá acesso a um feed exibindo perfis de outros jogadores e poderá restringir os cards por Jogo, Elo, Turno de disponibilidade e Gênero.
- **Orientações de Tela:** Modal de Filtros com Checkboxes para Jogos, Range de Elo, Opções de Turno. Toggle switch de segurança: "Buscar apenas perfis verificados/gênero". Área Principal com Player Cards.
- **Regras de Negócio:** O mural carrega apenas perfis com o mesmo jogo selecionado. O toggle de gênero restringe o retorno da API apenas a contas validadas.

**BDD & Implementação**
- **Critérios de Aceitação (BDD):** Dado que estou na tela "Encontrar Parceiros" Quando abro o menu de filtros, seleciono "Platina" e "Noite", e toco em "Aplicar" Então o mural deve atualizar exibindo apenas perfis que correspondam a essas condições

---

### 4. Enviar solicitação de conexão e confirmar Match

**Passo de Jornada**
- **Fase do Roadmap Estratégico:** Fase 1 – MVP de Conexão Segura e Perfil Gamer
- **Jornada de Usuário:** Marina, a jogadora focada e sem tempo – Interagir com os perfis encontrados para formar sua dupla.
- **Passo:** Enviar solicitação de conexão e confirmar Match.

**Geral**
- **Produto:** Team Up
- **Narrativa:** Como Marina, eu quero poder enviar uma solicitação de conexão em um card de perfil para que, se o outro jogador aceitar, um Match seja formado e possamos interagir.
- **Prioridade:** Alta | **Tipo:** Feature | **Tags:** match, interacao, conexao

**Detalhes**
- **Descrição Detalhada:** O usuário envia uma solicitação de conexão. O usuário alvo recebe a notificação e, quando aceita, a plataforma dispara a validação de "Match".
- **Orientações de Tela:** Player Card com botões "Pular" e "Conectar". Aba "Minhas Solicitações" para convites recebidos. Modal "Deu Match!".
- **Regras de Negócio:** Um usuário não pode enviar solicitações repetidas se o convite já estiver pendente. Recusar remove o card silenciosamente.

**BDD & Implementação**
- **Critérios de Aceitação (BDD):** Dado que possuo solicitações pendentes na aba "Minhas Solicitações" Quando clico em "Aceitar" no card de um usuário Então o sistema deve exibir a tela de "Deu Match!" e iniciar uma conversa no Chat

---

### 5. Trocar mensagens e IDs no chat integrado

**Passo de Jornada**
- **Fase do Roadmap Estratégico:** Fase 1 – MVP de Conexão Segura e Perfil Gamer
- **Jornada de Usuário:** Marina, a jogadora focada – Conversar com sua dupla recém-formada antes de entrar no jogo.
- **Passo:** Trocar mensagens e IDs no chat integrado.

**Geral**
- **Produto:** Team Up
- **Narrativa:** Como Marina, eu quero acessar um chat de texto privado com meus Matches para trocar IDs do jogo, link do Discord e combinar táticas sem expor meus dados públicos na rede.
- **Prioridade:** Alta | **Tipo:** Feature | **Tags:** chat, mensageria, mvp

**Detalhes**
- **Descrição Detalhada:** Chat de texto integrado para comunicação assíncrona ou em tempo real (básica). Mantém a interação rastreável pela plataforma inicialmente.
- **Orientações de Tela:** Tela "Mensagens" (Inbox) listando chats ativos. Tela "Chat Privado" com histórico, balões de texto e botão "Opções" (Desfazer Match, Denunciar).
- **Regras de Negócio:** Mensagens limitadas a texto (bloqueio de scripts e mídia na Fase 1).

**BDD & Implementação**
- **Critérios de Aceitação (BDD):** Dado que estou dentro de um "Chat Privado" ativo Quando digito uma mensagem no input e clico em "Enviar" Então a mensagem deve aparecer imediatamente no histórico da conversa

---

### 6. Receber notificações push de novos Matches

**Passo de Jornada**
- **Fase do Roadmap:** Fase 1 – Descoberta & MVP
- **Passo:** Habilitar e receber alertas de conexões.

**Geral**
- **Narrativa:** Como Marina, eu quero receber uma notificação no meu celular quando alguém aceitar meu convite, para que eu possa iniciar o chat rapidamente sem perder o timing da partida.
- **Prioridade:** Média | **Tipo:** Feature | **Tags:** push, engajamento

**Detalhes & Implementação**
- **Regras de Negócio:** Notificações não devem conter dados pessoais sensíveis. O toque na notificação abre diretamente a sala de chat recém-criada.
- **BDD:** Dado que o app está em segundo plano Quando um usuário aceitar meu convite de Match Então devo receber uma notificação push informando o novo Match.

---

### 7. Denunciar perfil ou comportamento tóxico

**Passo de Jornada**
- **Fase do Roadmap:** Fase 2 – Segurança & Lobbies
- **Passo:** Enviar reporte de segurança.

**Geral**
- **Narrativa:** Como Marina, eu quero denunciar usuários com comportamento inadequado no chat ou perfis ofensivos, para manter o ambiente seguro e garantir que a plataforma tome providências.
- **Prioridade:** Crítica | **Tipo:** Feature | **Tags:** seguranca, report

**Detalhes & Implementação**
- **Regras de Negócio:** Denunciar via chat deve anexar automaticamente o log das últimas 15 mensagens. A denúncia desfaz o Match e bloqueia o usuário imediatamente para quem denunciou.
- **BDD:** Dado que estou no chat com um Match Quando clico em "Denunciar", seleciono o motivo e confirmo Então o Match é desfeito e o chat é removido do meu inbox.

---

### 8. Avaliar parceiro após a partida (Score Mútuo)

**Passo de Jornada**
- **Fase do Roadmap:** Fase 2 – Segurança & Lobbies
- **Passo:** Registrar feedback da experiência de jogo.

**Geral**
- **Narrativa:** Como Marina, eu quero avaliar meu parceiro com um sistema de estrelas ou tags de comportamento após jogarmos juntos, para ajudar o algoritmo a destacar bons jogadores.
- **Prioridade:** Alta | **Tipo:** Feature | **Tags:** avaliacao, reputacao

**Detalhes & Implementação**
- **Regras de Negócio:** O usuário só pode avaliar a mesma pessoa uma vez a cada 30 dias. Notas consistentemente muito baixas acionam análise da moderação.
- **BDD:** Dado que formei um Match há mais de 2 horas Quando acesso o aplicativo, recebo o pop-up de avaliação e envio minha nota Então o score interno do usuário avaliado é atualizado.

---

### 9. Visualizar Score Público nos Player Cards

**Passo de Jornada**
- **Fase do Roadmap:** Fase 2 – Segurança & Lobbies
- **Passo:** Analisar reputação no mural.

**Geral**
- **Narrativa:** Como Marina, eu quero ver um indicador visual do "Score de Confiança" nos perfis que aparecem para mim, para decidir rapidamente se envio ou aceito um convite.
- **Prioridade:** Alta | **Tipo:** Feature | **Tags:** score, feed

**Detalhes & Implementação**
- **Regras de Negócio:** Exigir um mínimo de 5 avaliações recebidas para o score se tornar público no card, evitando viés negativo em contas novas.
- **BDD:** Dado que estou visualizando o mural de parceiros Quando vejo um card de jogador Então um selo codificado por cor deve indicar o nível de confiabilidade daquele usuário.

---

### 10. Agendar sessão de jogo com um Match (Calendário)

**Passo de Jornada**
- **Fase do Roadmap:** Fase 2 – Segurança & Lobbies
- **Passo:** Propor e confirmar um horário futuro para jogar.

**Geral**
- **Narrativa:** Como Marina, eu quero enviar uma sugestão de data e horário (ex: "Sexta às 20h") no chat do meu Match, para garantir que teremos compatibilidade de agenda sem precisar ficar perguntando se a pessoa está online.
- **Prioridade:** Média | **Tipo:** Feature | **Tags:** agendamento, retencao, chat

**Detalhes & Implementação**
- **Regras de Negócio:** Limite de agendamentos pendentes simultâneos para evitar spam. Ao ser aceito, o sistema programa um lembrete (push notification) automático para ambos 15 minutos antes.
- **BDD:** Dado que estou em um Chat Privado Quando envio uma sugestão de horário pelo ícone de calendário Então o outro usuário recebe um card interativo com a opção de Aceitar ou Recusar.

---

### 11. Definir e visualizar Estilo de Jogo (Playstyle)

**Passo de Jornada**
- **Fase do Roadmap:** Fase 1 – MVP de Conexão Segura e Perfil Gamer
- **Passo:** Configurar e filtrar preferências de dinâmica e foco para as partidas.

**Geral**
- **Narrativa:** Como Marina, eu quero selecionar tags que definam o meu Estilo de Jogo (ex: "Foco no Elo", "Comunicação Ativa", "Sem Rage") para atrair parceiros que partilhem dos mesmos objetivos e filtrar jogadores com expectativas diferentes.
- **Prioridade:** Alta | **Tipo:** Feature | **Tags:** perfil, matchmaking, expectativas

**Detalhes & Implementação**
- **Regras de Negócio:** O usuário é obrigado a escolher entre 1 e 3 tags de Estilo de Jogo no perfil. Estas tags são destacadas visualmente no Player Card no mural de buscas.
- **BDD:** Dado que estou na tela de edição do Perfil Quando seleciono as tags "Tryhard" e "Comunicação Ativa" e salvo Então elas devem ser exibidas publicamente no meu Player Card.

---

### 12. Aplicar filtros táticos avançados (Rotas e Classes)

**Passo de Jornada**
- **Fase do Roadmap:** Fase 2 – Segurança & Lobbies
- **Passo:** Filtrar perfis por função de jogo.

**Geral**
- **Narrativa:** Como Marina, eu quero filtrar jogadores por suas funções específicas (ex: Controlador, Iniciador, Suporte), para montar uma composição de time balanceada.
- **Prioridade:** Alta | **Tipo:** Feature | **Tags:** filtros, match

**Detalhes & Implementação**
- **Regras de Negócio:** As listas de funções disponíveis no filtro mudam dinamicamente dependendo do jogo selecionado pelo usuário na busca.
- **BDD:** Dado que estou buscando parceiros Quando aplico o filtro "Controlador" Então o sistema retorna apenas jogadores que registraram essa função como principal.

---

### 13. Assinar o plano Premium (Gateway de Pagamento)

**Passo de Jornada**
- **Fase do Roadmap:** Fase 3 – Monetização Inicial
- **Passo:** Realizar o pagamento da assinatura.

**Geral**
- **Narrativa:** Como Marina, eu quero assinar o plano Premium via PIX ou cartão de crédito, para ter vantagens exclusivas, como ver quem me enviou convites antes mesmo de dar Match.
- **Prioridade:** Alta | **Tipo:** Feature | **Tags:** monetizacao, premium

**Detalhes & Implementação**
- **Regras de Negócio:** A liberação das funcionalidades Premium deve ocorrer automaticamente via webhooks do provedor de pagamento após a confirmação da transação.
- **BDD:** Dado que estou no fluxo de pagamento Quando a transação é aprovada Então minha conta recebe imediatamente a flag "Premium".

---

### 14. Equipar itens cosméticos no Perfil

**Passo de Jornada**
- **Fase do Roadmap:** Fase 3 – Monetização Inicial
- **Passo:** Personalizar a exibição do card.

**Geral**
- **Narrativa:** Como Marina, eu quero acessar uma loja de itens virtuais para equipar bordas animadas e banners temáticos no meu Player Card, para me destacar visualmente no mural de buscas.
- **Prioridade:** Baixa | **Tipo:** Feature | **Tags:** loja, cosmeticos

**Detalhes & Implementação**
- **Regras de Negócio:** Itens ficam vinculados ao ID do usuário. Apenas a moldura selecionada é renderizada publicamente sobre a foto de perfil.
- **BDD:** Dado que possuo uma borda cosmética na minha conta Quando clico em "Equipar" Então todos os usuários passarão a ver meu card com a nova borda.

---

### 15. Validar conta via API Oficial do Jogo (Ex: Riot ID)

**Passo de Jornada**
- **Fase do Roadmap:** Fase 4 – Integrações & Recorrência
- **Passo:** Sincronizar credenciais oficiais.

**Geral**
- **Narrativa:** Como Marina, eu quero vincular meu perfil do Team Up com minha conta oficial do jogo via autenticação Oauth2, para exibir um selo de "Elo Verificado" e passar mais confiança.
- **Prioridade:** Alta | **Tipo:** Feature | **Tags:** api, verificacao

**Detalhes & Implementação**
- **Regras de Negócio:** A plataforma não armazena credenciais (senhas) do jogo oficial, salvando apenas o token de autorização e o Elo retornado pela API da desenvolvedora.
- **BDD:** Dado que aprovo a integração na página oficial Quando retorno ao Team Up Então meu Elo é travado para o valor real e ganho o selo de validação.

---

### 16. Sincronizar Status de "Online" e "Em Partida"

**Passo de Jornada**
- **Fase do Roadmap:** Fase 4 – Integrações & Recorrência
- **Passo:** Visualizar status em tempo real.

**Geral**
- **Narrativa:** Como Marina, eu quero ver um indicador na minha lista de Matches mostrando se a pessoa está "No Menu", "Em Partida" ou "Offline", para não enviar convites em horas inoportunas.
- **Prioridade:** Média | **Tipo:** Feature | **Tags:** status, realtime

**Detalhes & Implementação**
- **Regras de Negócio:** Exige integração robusta via WebSockets ou polling com a API do jogo vinculada para obter a atividade do jogador em tempo real.
- **BDD:** Dado que abro minha lista de Matches Quando um usuário estiver jogando uma partida no momento Então o avatar dele exibirá o status vermelho "Em Partida".

---

### 17. Automação e integração com Discord API

**Passo de Jornada**
- **Fase do Roadmap:** Fase 4 – Integrações & Recorrência
- **Passo:** Criar sala de voz com um clique.

**Geral**
- **Narrativa:** Como Marina, eu quero clicar em um botão no chat que gera automaticamente um link temporário para um canal de voz no servidor oficial do Discord do app, pulando a etapa de adicionar amigos manualmente.
- **Prioridade:** Média | **Tipo:** Feature | **Tags:** discord, voz

**Detalhes & Implementação**
- **Regras de Negócio:** O backend utiliza um bot do Discord para gerar canais de voz efêmeros. O canal é automaticamente destruído quando todos os usuários saem.
- **BDD:** Dado que estou no chat com um Match Quando clico no ícone "Gerar Call de Voz" Então um link do Discord é enviado na conversa para nós dois.

---

### 18. Alternar para o Tema Escuro (Dark Mode)

**Passo de Jornada**
- **Fase do Roadmap:** Uso Contínuo
- **Passo:** Configurar UI/UX.

**Geral**
- **Narrativa:** Como Marina, eu quero poder alternar a interface do aplicativo para o Tema Escuro, para descansar meus olhos durante sessões prolongadas à noite.
- **Prioridade:** Alta | **Tipo:** Feature | **Tags:** ui-ux, acessibilidade

**Detalhes & Implementação**
- **Regras de Negócio:** A preferência é salva localmente no dispositivo. A inversão de cores não deve prejudicar a legibilidade dos Player Cards ou selos de ranque.
- **BDD:** Dado que acesso as configurações Quando seleciono "Tema Escuro" Então as cores da interface são invertidas instantaneamente sem recarregar o app.

---

### 19. Desfazer Match e remover conexão

**Passo de Jornada**
- **Fase do Roadmap:** Fase 1 – Descoberta & MVP
- **Passo:** Gerenciar lista de amigos.

**Geral**
- **Narrativa:** Como Marina, eu quero poder remover um Match antigo da minha lista, para manter meu inbox organizado apenas com as pessoas que ainda jogo ativamente.
- **Prioridade:** Média | **Tipo:** Feature | **Tags:** gestao, contatos

**Detalhes & Implementação**
- **Regras de Negócio:** A remoção é silenciosa (o outro usuário não recebe alerta). O histórico de chat é apagado da visualização de ambos.
- **BDD:** Dado que abro as opções de um contato existente Quando clico em "Desfazer Match" e confirmo Então a pessoa e a conversa somem da minha lista de mensagens.

---

### 20. Excluir conta e dados (LGPD)

**Passo de Jornada**
- **Fase do Roadmap:** Todos
- **Passo:** Encerrar jornada e garantir conformidade legal.

**Geral**
- **Narrativa:** Como Marina, eu quero ter uma opção clara e simples para deletar permanentemente minha conta e meus dados pessoais do Team Up, para garantir minha privacidade caso deixe de usar a plataforma.
- **Prioridade:** Alta | **Tipo:** Feature | **Tags:** privacidade, lgpd

**Detalhes & Implementação**
- **Regras de Negócio:** Implementar hard delete de dados sensíveis e credenciais, mantendo soft delete apenas de métricas anonimizadas de produto. Exige re-autenticação para concluir.
- **BDD:** Dado que estou na aba de Privacidade Quando solicito a exclusão da conta e insiro minha senha Então minha conta é inativada e agendada para remoção permanente no banco de dados.
