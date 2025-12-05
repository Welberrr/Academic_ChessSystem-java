# ♟️ Console Chess System

> Um sistema de xadrez robusto e interativo desenvolvido em **Java Puro**, focado na aplicação de conceitos avançados de Programação Orientada a Objetos.

![Java Badge](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Status Badge](https://img.shields.io/badge/Status-Concluído-green?style=for-the-badge)

---

## 💻 Sobre o Projeto

Este projeto consiste em um jogo de Xadrez completo executado via terminal, desenvolvido para colocar em prática fundamentos sólidos de Engenharia de Software.

Diferente de projetos básicos, aqui foi implementada uma arquitetura desacoplada dividida em camadas (**Board Layer** e **Chess Layer**), permitindo que a lógica do tabuleiro seja independente das regras específicas do jogo.

### 🧠 Conceitos e Tecnologias Aplicadas

* **POO Avançada:** Herança, Polimorfismo, Encapsulamento e Abstração.
* **Tratamento de Exceções:** Criação de exceções personalizadas (`BoardException`, `ChessException`) para garantir a integridade do estado do jogo.
* **Padrões de Projeto:** Uso de padrões para organização das peças e tabuleiro.
* **Lógica Complexa:** Validação de movimentos, detecção de **Check/Checkmate** e jogadas especiais.
* **Interface:** Uso de **Códigos ANSI** para colorir o terminal e melhorar a experiência do usuário.

---

## ⚙️ Funcionalidades Implementadas

O sistema suporta as regras oficiais do Xadrez, incluindo:

* ✅ **Movimentação Básica:** Todas as peças com suas regras padrão.
* ✅ **Turnos:** Controle de turnos (Brancas vs Pretas).
* ✅ **Check & Checkmate:** Lógica de verificação de rei em perigo e fim de jogo.
* ✅ **Jogadas Especiais:**
    * **Castling (Roque):** Pequeno e Grande.
    * **En Passant:** Captura especial de peão.
    * **Promotion (Promoção):** Quando o peão chega ao final do tabuleiro.
* ✅ **Contador de Jogadas:** Histórico de turnos.

---

## 🚀 Como Executar

⚠️ **Atenção:** Como o projeto utiliza cores ANSI para desenhar o tabuleiro, recomenda-se executar em terminais que suportem cores (como **Git Bash**, **VS Code Terminal** ou terminais Linux). O console padrão do Eclipse/NetBeans pode não exibir as cores corretamente.

### Pré-requisitos
* Java Development Kit (JDK) instalado.

### Passo a Passo

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/Welberrr/chess-system-java.git](https://github.com/Welberrr/chess-system-java.git)
    ```
2.  **Entre na pasta do projeto:**
    ```bash
    cd chess-system-java/src
    ```
3.  **Compile o código:**
    ```bash
    javac application/Program.java
    ```
4.  **Execute:**
    ```bash
    java application.Program
    ```

---

## 🎮 Guia Visual das Peças

Para facilitar a visualização no terminal, as peças seguem a notação internacional (Inglês):

| Sigla | Peça (PT-BR) | Piece (EN) |
| :---: | :--- | :--- |
| **K** | ♔ Rei | King |
| **Q** | ♕ Rainha | Queen |
| **R** | ♖ Torre | Rook |
| **B** | ♗ Bispo | Bishop |
| **N** | ♘ Cavalo | Knight |
| **P** | ♙ Peão | Pawn |

> **Nota:** As peças pretas são representadas pela cor **Amarela** no terminal para melhor contraste com fundos escuros.

---

## 📂 Estrutura do Código

```text
src/
├── application/    # Classe principal e interface do usuário (UI)
├── boardgame/      # Camada de tabuleiro (lógica genérica de posições)
└── chess/          # Camada do jogo (regras específicas do Xadrez)
    └── pieces/     # Implementação de cada peça (King, Rook, etc.)
