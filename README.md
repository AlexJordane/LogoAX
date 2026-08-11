# LogoAX

O **LogoAX** é um ambiente interativo de aprendizagem para exploração geométrica baseado na linguagem Logo. O aplicativo foi desenvolvido para uso na disciplina de **Tecnologias Digitais em Educação Matemática**, oferecendo um espaço simples e direto para comandos de movimentação e construção de procedimentos com a tartaruga.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5 e CSS3:** Interface e estruturação visual.
- **JavaScript (ES6):** Lógica da aplicação, gestão de memória e tradução de comandos.
- **Python:** Linguagem base interpretada no navegador.
- **[Skulpt](https://skulpt.org/):** Interpretador de Python rodando diretamente no navegador (client-side).

---

## 📌 Funcionalidades

- **Área de Desenho (Canvas):** Palco de $700 \times 500$ pixels com sistema de coordenadas cartesianas centrado na origem $(0,0)$.
- **Comando Interativo:** Envio de instruções individuais com resposta visual imediata (suporta acionamento via botão ou tecla `Enter`).
- **Histórico de Comandos:** Registro contínuo das ações no modo interativo, com opção para exportação em arquivo `.txt`.
- **Editor de Procedimentos:** Espaço para criação de rotinas completas e novas palavras/funções via comando `aprenda`. Exportação dos roteiros em arquivo `.txt`.
- **Alertas de Erro:** Mensagens informativas em tela amarela indicando falhas de sintaxe ou comandos não aprendidos.

---

## 🚀 Como Executar

Por ser uma aplicação baseada em *client-side* (HTML/JavaScript/Python via Skulpt), não é necessária a instalação de dependências ou servidores.

1. Baixe o arquivo `logo6.html` (ou clone o repositório).
2. Abra o arquivo diretamente em qualquer navegador web moderno.

---

## 📖 Comandos do LogoAX

### 1. Comandos Básicos de Movimento
| Comando | Descrição | Exemplo |
| :--- | :--- | :--- |
| `pf n` | Avança $n$ passos para a frente | `pf 100` |
| `pt n` | Recua $n$ passos para trás | `pt 50` |
| `pd a` | Gira $a$ graus para a direita | `pd 90` |
| `pe a` | Gira $a$ graus para a esquerda | `pe 45` |

### 2. Comandos de Tela
| Comando | Descrição |
| :--- | :--- |
| `tat` | Apaga os desenhos, levanta a caneta e posiciona a tartaruga no centro $(0,0)$ apontada para cima |
| `lt` | Limpa a tela recarregando o aplicativo e esvaziando a memória |

### 3. Posicionamento e Coordenadas
| Comando | Descrição | Exemplo |
| :--- | :--- | :--- |
| `mudepos x y` | Move a tartaruga diretamente para o ponto $(x, y)$ | `mudepos 100 50` |
| `mudex x` | Altera apenas a coordenada horizontal $x$ | `mudex -50` |
| `mudey y` | Altera apenas a coordenada vertical $y$ | `mudey 100` |
| `centro` | Move a tartaruga para $(0,0)$ virada para cima | `centro` |
| `cima` | Ajusta a orientação da tartaruga para a direção superior ($90^\circ$) | `cima` |

### 4. Lápis e Cores
| Comando | Descrição | Exemplo |
| :--- | :--- | :--- |
| `ul` | **Use Lápis:** Abaixa a caneta para voltar a desenhar | `ul` |
| `ub` | **Use Borracha:** Configura o lápis para a cor branca de fundo | `ub` |
| `un` | **Use Nada:** Levanta a caneta para mover sem desenhar | `un` |
| `mudecl c` | Altera a cor do traço (nome, número ou `[R G B]`) | `mudecl azul`, `mudecl 4`, `mudecl [0 0 255]` |

#### Tabela de Cores Padrão
| Número | Nome da Cor | RGB |
| :---: | :--- | :---: |
| 0 | preto | `[0 0 0]` |
| 1 | vermelho | `[255 0 0]` |
| 2 | verde | `[0 255 0]` |
| 3 | amarelo | `[255 255 0]` |
| 4 | azul | `[0 0 255]` |
| 5 | magenta | `[255 0 255]` |
| 6 | ciano | `[0 255 255]` |
| 7 | branco | `[255 255 255]` |
| 8 | cinza | `[128 128 128]` |
| 9 | cinzaclaro | `[192 192 192]` |
| 10 | vermelhoescuro | `[128 0 0]` |
| 11 | verdeescuro | `[0 128 0]` |
| 12 | azulescuro | `[0 0 128]` |
| 13 | laranja | `[255 200 0]` |
| 14 | rosa | `[255 175 175]` |
| 15 | violeta | `[128 0 255]` |
| 16 | marrom | `[153 102 0]` |

---

## 🔁 Estruturas de Repetição e Procedimentos

### Comando `repita`
Sintaxe: `repita n [comandos]`  
Exemplo para desenhar um quadrado de lado 100:
```logo
repita 4 [pf 100 pd 90]
