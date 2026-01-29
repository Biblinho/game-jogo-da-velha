# GameJogoDaVelha — Java Swing (Gamer Edition)

Aplicação desktop de **Jogo da Velha** desenvolvida em **Java com Swing**, contendo múltiplos modos de jogo, inteligência artificial com **Minimax + poda alfa-beta**, persistência de dados, sistema de undo, exportação de replay e interface gráfica estilizada.

O projeto foi criado com foco em **boas práticas de programação**, **organização de código**, **experiência do usuário (UX)** e **Programação Orientada a Objetos**.

---

## 🎮 Funcionalidades

- Modo **1 jogador (vs IA)** ou **2 jogadores (local)**
- Três níveis de dificuldade:
  - Fácil (movimentos aleatórios)
  - Médio (IA híbrida)
  - Impossível (Minimax com poda alfa-beta)
- Sistema de **Undo** (desfazer jogadas)
- Destaque visual da linha vencedora
- Persistência de placar em arquivo local
- Exportação de replay (formato JSON-like)
- Tema Gamer com alternância visual
- Efeitos sonoros gerados via Java Sound API

---

## 🧠 Arquitetura e Organização

O projeto concentra-se em uma classe principal (`GameJogoDaVelha`) responsável por:

- Construção da interface gráfica
- Gerenciamento do estado do jogo
- Controle de turnos
- Execução da inteligência artificial
- Persistência de dados
- Tratamento de eventos e UX

A lógica foi organizada em blocos bem definidos:
- **Estado do jogo** (`board`, turno, modo de jogo)
- **Eventos da UI** (cliques, botões, seletores)
- **IA** (Minimax + heurística por profundidade)
- **Persistência** (salvar/carregar placar)
- **Multimídia** (sons sintetizados)

---

## 🔄 Fluxo do Jogo

1. O jogador seleciona o modo e a dificuldade
2. Cada jogada atualiza o estado lógico (`board[][]`)
3. A interface reflete imediatamente a jogada
4. O sistema verifica vitória ou empate
5. Em modo IA, a jogada é calculada automaticamente
6. O placar é atualizado e persistido

---

## 🤖 Inteligência Artificial

A IA utiliza o algoritmo **Minimax com poda alfa-beta**, garantindo decisões ótimas no modo *Impossível*.

Características:
- Penalização por profundidade (ganhar mais rápido é melhor)
- Poda alfa-beta para reduzir custo computacional
- Simulação direta no tabuleiro lógico
- Níveis Fácil e Médio utilizam aleatoriedade controlada

---

## 🖥️ Interface Gráfica (UI/UX)

- Desenvolvida com **Swing**
- Layout responsivo com `BorderLayout` e `GridLayout`
- Estilo visual gamer com gradientes, hover effects e feedback visual
- Atualizações seguras utilizando a **Event Dispatch Thread (EDT)**

---

## 🔊 Áudio

Os efeitos sonoros são gerados dinamicamente utilizando a **Java Sound API**, sem dependência de arquivos externos, garantindo portabilidade do projeto.

---

## 💾 Persistência de Dados

O placar é salvo automaticamente em arquivo local no diretório do usuário, permitindo que os dados sejam mantidos entre execuções da aplicação.

---

## 🛠️ Tecnologias Utilizadas

- Java
- Java Swing
- Programação Orientada a Objetos
- Algoritmo Minimax
- Java Sound API
- Git / GitHub

---

## 🚀 Possíveis Melhorias Futuras

- Ranking online
- Multiplayer em rede
- Animações de transição
- Refatoração para arquitetura MVC
- Salvamento de partidas completas

---

## 👤 Autor

Roberson de Oliveira  
GitHub: https://github.com/Biblinho
