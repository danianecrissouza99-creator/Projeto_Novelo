# Novelo 🐱

Bichinho virtual com um gatinho de peluche. Dá-lhe comida, banho e mimos, põe-no a dormir, joga mini-jogos para ganhar moedas e compra-lhe roupas.

**▶ Jogar:** https://danianecrissouza99-creator.github.io/Projeto_Novelo/

---

## Sobre o projeto

Projeto da UC **Testes e Qualidade de Software**, ISTEC.

O Novelo foi feito para ser **testado por um colega**. O trabalho do testador é comparar o que o jogo **faz** com o que ele **devia fazer**, segundo as regras abaixo (requisitos). Cada diferença é um defeito a registar no relatório.

- Funciona no browser, no computador ou no telemóvel, com rato, teclado ou toque.
- Não é preciso instalar nada. O progresso fica gravado no próprio browser.

---

## Como se joga

| Divisão | O que se faz |
|---|---|
| **Cozinha** | Dar comida do frigorífico |
| **Banho** | Esfregar com sabão e passar o chuveiro |
| **Quarto** | Apagar a luz para dormir e recuperar energia |
| **Jogos** | Jogar mini-jogos para ganhar moedas e XP |
| **Loja** | Comprar comida e roupas |
| **Roupas** | Vestir peças, mudar a cor do pelo e o nome |

Tocar no gatinho faz-lhe festas (+ diversão).

---

## Requisitos funcionais

Isto é o que o jogo **deve** fazer.

### Início e topo
| ID | Regra |
|---|---|
| RF-01 | Na primeira vez, o jogo pede um nome com **2 a 12 letras**. A mesma regra vale ao **mudar o nome** (Roupas → Mudar nome). |
| RF-02 | O topo mostra o nome, o nível, o humor, o XP e as moedas. Um gatinho novo começa no **nível 1**, com **50 moedas** e as barras a 80%. |

### Barras e humor
| ID | Regra |
|---|---|
| RF-03 | Há 4 barras: **Fome, Higiene, Energia e Diversão**. Os valores ficam sempre **entre 0% e 100%**. |
| RF-04 | A cor de **todas** as barras segue o valor: verde (55% ou mais), amarelo (25% a 54%) e vermelho (abaixo de 25%). |
| RF-05 | As barras descem com o tempo. A dormir, a energia sobe. |
| RF-06 | Se **qualquer** barra ficar abaixo de 25%, o gatinho fica **triste** (cara triste e lágrimas, humor "Triste") e aparece um balão com o que precisa. Com todas acima de 70%, fica "Feliz". |

### Navegação
| ID | Regra |
|---|---|
| RF-07 | Cada botão da barra de baixo abre a sua divisão e fica **marcado**. Nenhum botão deixa a página parada. |

### Cozinha
| ID | Regra |
|---|---|
| RF-08 | Cada comida gasta 1 unidade do frigorífico, dá **+5 XP** e enche a **fome** no valor indicado. |
| RF-09 | Com a fome a 100%, o gatinho recusa a comida ("Estou cheio!"). |

| Comida | Enche a fome | Preço |
|---|---|---|
| Peixe | +30 | 15 moedas |
| Leite | +15 | 8 moedas |
| Bolacha | +10 | 5 moedas |
| Sardinha | +50 | 30 moedas |

### Banho
| ID | Regra |
|---|---|
| RF-10 | Com o sabão escolhido, cada toque no gatinho faz espuma e dá **+5 de higiene**. |
| RF-11 | O chuveiro só funciona com espuma e **tira a espuma**, sem baixar a higiene. |

### Quarto
| ID | Regra |
|---|---|
| RF-12 | Acordado, o botão diz **"Apagar a luz"** e põe o gatinho a dormir. A dormir, o botão diz **"Acender a luz"** e acorda-o. |
| RF-13 | A dormir, o gatinho **não pode comer, tomar banho nem jogar** (aparece um aviso). |

### Mini-jogos
| ID | Regra |
|---|---|
| RF-14 | Cada jogo gasta 10 de energia e dá **+20 de diversão**, **+10 XP** e **2 moedas por cada ponto**. |
| RF-15 | **Apanha o Peixe:** dura **40 segundos** e tem **3 vidas**. Cada osso tira 1 vida e o jogo só acaba **sem vidas** ou **sem tempo**. As setas ← → movem o cesto **no sentido da seta**. Peixe = 1 ponto, peixe dourado = 3. |
| RF-16 | **Caça ao Rato:** dura **30 segundos**. Cada rato tocado, em **qualquer buraco**, vale 1 ponto. |
| RF-17 | **Salto do Gato:** começa assim que se abre e funciona como os outros jogos (tempo, pontos e moedas). |

### Loja
| ID | Regra |
|---|---|
| RF-18 | Comprar comida tira **exatamente o preço indicado** e soma **1** a essa comida no frigorífico. |
| RF-19 | Só se compra com **moedas suficientes**. As moedas **nunca ficam negativas**. |
| RF-20 | Cada roupa só se compra a partir do seu nível. |

| Roupa | Onde se veste | Preço | Nível |
|---|---|---|---|
| Laço | cabeça | 20 | 1 |
| Boné | cabeça | 40 | 2 |
| Óculos | olhos | 60 | 3 |
| Coroa | cabeça | 150 | 5 |

### Roupas e definições
| ID | Regra |
|---|---|
| RF-21 | Tocar numa peça comprada **veste-a no sítio certo**. Tocar outra vez **despe-a**. |
| RF-22 | Cores do pelo: Cinzento, Laranja e Branco no nível 1, Preto no nível 4. Escolher uma cor **muda logo** o gatinho. |
| RF-23 | "Recomeçar do zero" pede confirmação e depois **apaga tudo** e volta a pedir o nome. |

### Avisos, XP e gravação
| ID | Regra |
|---|---|
| RF-24 | As mensagens de aviso aparecem no topo e **desaparecem sozinhas** em cerca de 2 segundos. |
| RF-25 | Sobe-se de nível ao **chegar** a 100 × nível de XP (100 XP no nível 1). Ganha-se 20 moedas e a mensagem indica o **novo** nível. |
| RF-26 | O jogo grava sozinho **tudo** (nome, nível, XP, moedas, barras, frigorífico e roupas). Ao recarregar a página, fica tudo igual. |

---

## Requisitos não funcionais

| ID | Tipo | Regra |
|---|---|---|
| RNF-01 | Responsividade | Funciona em ecrãs de **360 px** de largura até monitores grandes, sem esconder informação (por exemplo, as moedas). |
| RNF-02 | Desempenho | Nenhuma ação deixa a página **parada ou sem responder**. |
| RNF-03 | Texto | Todos os textos estão em **português correto** e coerentes com o que acontece. |
| RNF-04 | Compatibilidade | Funciona nas versões atuais do Chrome, Edge e Firefox. |

---

## Como registar um defeito

Para cada defeito encontrado, sugere-se registar:

| Campo | O que escrever |
|---|---|
| **ID** | D-01, D-02… |
| **Título** | Frase curta com o problema |
| **Requisito** | O RF/RNF que não é cumprido |
| **Passos para reproduzir** | 1. Abrir… 2. Carregar em… 3. … |
| **Resultado esperado** | O que a regra diz |
| **Resultado obtido** | O que aconteceu |
| **Tipo** | Funcional, Interface, Usabilidade, Texto, Validação, Dados/gravação, Navegação, Desempenho, Responsividade |
| **Severidade** | Alta, Média ou Baixa |
| **Evidência** | Captura de ecrã ou vídeo |

**Dicas:**
- Para testar o telemóvel no computador, use a vista de dispositivo do browser (F12 → ícone do telemóvel).
- Para recomeçar um teste do zero, apague os dados do site (F12 → Application → Local Storage).

---

## Tecnologias

HTML, CSS e JavaScript, sem bibliotecas. O gatinho, o cenário e os mini-jogos são desenhados com a Canvas API.

---

Daniane Christyni Souza da Silva · Desenvolvimento de Software, 2.º ano · ISTEC
