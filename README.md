# 🎮 TeamUp — Plataforma de Matchmaking Competitivo

![Status](https://img.shields.io/badge/Status-Em_Desenvolvimento-blue?style=for-the-badge)
![Foco](https://img.shields.io/badge/Foco-eSports_%26_Ranked-orange?style=for-the-badge)
![Metodologia](https://img.shields.io/badge/Metodologia-BDD_%26_Discovery-green?style=for-the-badge)
![Curso](https://img.shields.io/badge/Engenharia_de_Software-UNIFOR-002B49?style=for-the-badge)

> Conectando jogadores competitivos por sinergia comportamental, funções complementares e horários compatíveis. O fim da roleta-russa da fila solo (*Solo Queue*).

---

## 📌 Documentação do Projeto

Abaixo estão os documentos estratégicos e de pesquisa que fundamentam o desenvolvimento do Team Up:

* 📄 [Visão do Produto e Escopo (É/Não É)](#visão-do-produto-e-escopo-énão-é)
* 📄 [Matriz CSD & Mapa de Empatia](#matriz-csd--mapa-de-empatia)
* 📄 [Jobs To Be Done (JTBD)](#jobs-to-be-done-jtbd)
* 📄 [Problem-Solution Fit Canvas](#problem-solution-fit-canvas)
* 📄 [Business Model Canvas](#business-model-canvas)
* 📄 [Value Proposition Canvas](#value-proposition-canvas)
* 📄 [Jornada do Usuário e Histórias (MVP)](#jornada-do-usuário-e-histórias-mvp)
* 📄 [Roadmap Estratégico](#roadmap-estratégico)

---

## 🎯 Visão do Produto e Escopo (É/Não É)

Definição clara das fronteiras e do propósito do sistema para manter o alinhamento da equipe de engenharia e evitar desvios de escopo (*scope creep*).

| Dimensão | Definição Estratégica |
| :--- | :--- |
| **É** | Uma plataforma inteligente de matchmaking pré-jogo voltada a conectar jogadores por compatibilidade comportamental, comunicação e rotas. |
| **NÃO É** | Uma rede social generalista de jogos, um cliente de jogo independente ou uma plataforma de chat genérica. |
| **FAZ** | Pareamento inteligente de duos/squads, filtros por função primária/secundária, histórico de reputação pós-partida e integração de comunicação via Discord API. |
| **NÃO FAZ** | Não altera o cliente interno do jogo, não faz matchmaking in-game oficial, não garante vitória em partidas e não atua como coach tático automatizado. |

---

## 🧠 Matriz CSD & Mapa de Empatia

### Matriz CSD (Certezas, Suposições e Dúvidas)

| Categoria | Descrição | Status de Validação |
| :--- | :--- | :--- |
| **Certeza** | Jogadores solo enfrentam alta frustração com toxicidade, ociosidade (AFK) e falta de comunicação na fila solo padrão. | Validado via pesquisa com comunidade gamer. |
| **Suposição** | Jogadores competitivos priorizam sinergia de voz e postura madura antes mesmo da paridade de elo exata. | Em teste de usabilidade. |
| **Dúvida** | Qual a taxa real de adesão ao formulário mútuo de avaliação comportamental e reputação pós-partida? | Métrica chave monitorada no MVP. |

### Mapa de Empatia do Jogador Competitivo

* **O que ele pensa e sente?**  
  *"Quero subir de elo sem estresse; detesto perder tempo com trolls e pessoas que desistem no primeiro erro."*
* **O que ele escuta?**  
  Críticas nos chats do jogo, streams reclamando da aleatoriedade da fila solo e amigos em horários desencontrados.
* **O que ele vê?**  
  Telas de derrota por desistência alheia, composições de time desbalanceadas e servidores de Discord desorganizados.
* **O que ele diz e faz?**  
  Comunica chamadas táticas (*calls*), busca parceiros fixos em grupos aleatórios de redes sociais e desiste de jogar após partidas tóxicas.
* **Quais são as suas Dores?**  
  Perda de pontuação (PDL/Rank), frustração com parceiros inadequados, desperdício de tempo e desgaste mental.
* **Quais são os seus Ganhos?**  
  Ambiente focado na vitória, comunicação limpa por voz, entrosamento tático e progresso consistente nas ranqueadas.

---

## 💼 Jobs To Be Done (JTBD)

> **Declaração Central:**  
> *"Quando estou prestes a iniciar minha sessão diária de ranqueadas competitivas, eu quero encontrar rapidamente um duo/squad alinhado à minha rota, maturidade e estilo de comunicação, para que eu possa evoluir de elo com consistência, foco e sem desgaste com toxicidade."*

### Dimensões do Job:
1. **Funcional:** Encontrar um parceiro do mesmo elo que complete a função restante (ex.: Suporte procurando Atirador) nos próximos 5 minutos.
2. **Emocional:** Sentir-se no controle da experiência, jogando com tranquilidade e confiança mútua.
3. **Social:** Construir reputação como jogador confiável e formar um círculo de parceiros fixos.

---

## 🧩 Problem-Solution Fit Canvas

Mapeamento da relação direta entre a dor real identificada e a funcionalidade entregue na plataforma:

| Problema Identificado | Causa Raiz | Solução do TeamUp | Métrica de Sucesso |
| :--- | :--- | :--- | :--- |
| **Fila Solo Caótica** | Algoritmos oficiais focam apenas em tempo de espera e elo numérico, ignorando comportamento. | Pareamento por perfil comportamental e pontuação de reputação verificada por pares. | Redução de 80% nos relatos de toxicidade entre duos pareados. |
| **Incompatibilidade de Rota** | Dois jogadores que jogam na mesma posição caem juntos e disputam espaço. | Filtros estritos por função primária e secundária antes da formação do grupo. | 100% de sinergia de papéis táticos nas duplas formadas. |
| **Comunicação Falha** | Falta de integração com canais de voz dedicados e preferências de comunicação. | Conexão com Discord API para criação direta de sala privativa de voz. | Menos de 2 minutos entre o aceite do match e o início da chamada. |

---

## 📊 Business Model Canvas

Visão enquadrada do modelo de sustentabilidade e operação do TeamUp:

* **Proposta de Valor:** Matchmaking assertivo focado em sinergia tática e redução comprovada de toxicidade em jogos ranqueados.
* **Segmento de Clientes:** Gamers competitivos de títulos em equipe (League of Legends, Valorant, CS2, Overwatch 2).
* **Canais:** Web App responsivo, integração nativa via bot de Discord e divulgação em comunidades competitivas.
* **Relacionamento:** Sistema de reputação por pontuação mútua pós-jogo (*Karma/Fair Play*).
* **Fontes de Receita:** Modelo Freemium (acesso gratuito aos filtros essenciais; plano Pro para filtros ultra-específicos, estatísticas avançadas e badges de clã).
* **Recursos-Chave:** Algoritmo proprietário de pontuação de compatibilidade, banco de dados e APIs oficiais de jogos.
* **Atividades-Chave:** Aprimoramento contínuo do algoritmo, moderação ativa e manutenção de infraestrutura.
* **Parcerias-Chave:** Discord Developer Platform, APIs da Riot Games / Steam e ligas amadoras de eSports.
* **Estrutura de Custos:** Custos de hospedagem e servidores em nuvem, bancos de dados em tempo real e manutenção da aplicação.

---

## 💎 Value Proposition Canvas
