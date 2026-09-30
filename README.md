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

* **Proposta de Valor:** Matchmaking pré-jogo baseado em sinergia de funções, comportamento verificado e integração de voz.
* **Segmento de Clientes:** Gamers competitivos de títulos em equipe (League of Legends, Valorant, CS2, Overwatch 2).
* **Canais:** Web App responsivo, integração nativa via bot de Discord e divulgação em comunidades competitivas.
* **Relacionamento:** Sistema comunitário de reputação (*Fair Play Karma*) com moderação ativa.
* **Fontes de Receita:** Modelo Freemium (gratuito para buscas básicas; plano Pro com estatísticas avançadas, filtros ilimitados e badges exclusivas).
* **Recursos-Chave:** Algoritmo proprietário de compatibilidade de duos, banco de dados e APIs oficiais de jogos.
* **Atividades-Chave:** Desenvolvimento contínuo, aprimoramento do algoritmo e moderação comunitária.
* **Parcerias-Chave:** Discord Developer Platform, Riot Games API, Steam Developer e ligas amadoras de eSports.
* **Estrutura de Custos:** Servidores em nuvem, banco de dados em tempo real e infraestrutura de rede.

---

## 💎 Value Proposition Canvas

### 1. Perfil do Cliente
* **Tarefas do Cliente:** Encontrar parceiros compatíveis no final do dia; coordenar comunicação por voz; subir de elo nas ranqueadas.
* **Dores:** Perder partidas por trolls ou desistências na fila solo; parceiros que não usam microfone; disputa pela mesma rota.
* **Ganhos:** Comunicação tática limpa; vitórias consistentes; entrosamento sem desgaste mental.

### 2. Mapa de Valor
* **Produtos e Serviços:** Plataforma web de matchmaking com mural de *Player Cards* e filtros em tempo real.
* **Aliviadores de Dores:** Verificação de reputação para afastar jogadores tóxicos; filtros estritos de função e elo.
* **Criadores de Ganho:** Conexão direta com sala de voz do Discord; sistema de avaliações mútuas pós-jogo.

---

## 🚀 Jornada do Usuário e Histórias (MVP)

A jornada principal do produto foi estruturada do onboarding até a avaliação final:

1. **Cadastro e Perfil:** Vinculação de ID do jogo, seleção de elo, horários habituais e funções principais.
2. **Exploração de Parceiros:** Aplicação de filtros táticos para visualizar o mural de *Player Cards*.
3. **Conexão e Partida:** Envio de solicitação, aceite mútuo e direcionamento automático para a sala de voz.
4. **Ciclo de Feedback:** Avaliação rápida do comportamento do parceiro após o término da sessão.

### Histórias de Usuário em BDD (Behavior-Driven Development)

#### US01: Filtragem por Função e Elo
> **Como** jogador competitivo  
> **Quero** filtrar perfis por elo compatível e função complementar  
> **Para que** eu não entre em partidas com choque de rotas ou disparidade de nível técnico.

```gherkin
Cenário: Filtro bem-sucedido de parceiro para Duo
  Dado que estou logado na plataforma TeamUp com o perfil "Elo Ouro - Função Suporte"
  Quando eu aplico o filtro de busca por elo "Ouro" e função "Atirador (ADC)"
  Então o sistema deve exibir apenas perfis com elo compatível que joguem de Atirador
  E cada card deve indicar o nível de reputação e preferência de comunicação por voz.
```

#### US02: Avaliação Mútua Pós-Partida
> **Como** usuário que concluiu uma sessão de jogos  
> **Quero** avaliar o comportamento e a comunicação do meu parceiro  
> **Para que** a comunidade mantenha um índice de confiabilidade saudável e transparente.

```gherkin
Cenário: Envio de avaliação positiva pós-jogo
  Dado que eu finalizei uma partida com o duo indicado pelo TeamUp
  Quando eu selecionar a opção "Recomendo" e marcar a tag "Boa Comunicação"
  Então o índice de reputação do jogador deve ser incrementado
  E essa informação deve ser refletida no perfil público dele.
```

---

## 🗺️ Roadmap Estratégico

| Fase | Foco Estratégico | Entregáveis Principais |
| :--- | :--- | :--- |
| **Fase 1 (Atual)** | **Descoberta & MVP** | CSD, Canvas, BDDs aprovados, telas de cadastro, mural de perfis e autenticação. |
| **Fase 2** | **Conexão & Automação** | Chat interno em tempo real, integração direta com bot de Discord e sistema de feedback pós-jogo. |
| **Fase 3** | **Expansão de Plataforma** | Validação automatizada de dados via Riot/Steam API e sistema de formação de equipes completas (5v5). |

---

## 👥 Equipe do Projeto

* **Lívia Barreto**
* **Rômulo Azevedo**
* **Rafaele Gomes**
* **Manu**
* *Projeto acadêmico desenvolvido na Universidade de Fortaleza (UNIFOR).*
