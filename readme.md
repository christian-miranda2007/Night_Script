# Night Script! 
entendeu o trocadilho?

Um jogo de encontro no estilo *visual novel*, feito com HTML, CSS e JavaScript puro, sem bibliotecas. O jogador precisa responder corretamente às pistas da kwaii kitty para conquistá-la, e o final depende do desempenho na noite.


## História

numa noite noite fria, uma boa hora para ler um livro... Você está no sofá, deslizando no Tinder, quando aparece a pessoa mais linda que você já viu: a kwaii kitty, engenheira sênior de infraestrutura numa big tech. Você tem só seis meses de curso de Análise e Desenvolvimento de Sistemas / Programação. Deu match, e agora vocês vão jantar.

Para impressioná-la, você vai precisar mostrar que sabe de arquitetura de computadores. Ela não gosta de mentirosos.

## Como jogar

1. Clique em **Iniciar o encontro**.
2. Clique na caixa de diálogo (ou aperte Espaço ou Enter) para avançar as falas. Um clique durante a digitação mostra o texto completo.
3. A kwaii kitty dá uma **pista** e você escolhe, entre 4 alternativas, o **termo** que ela descreve.
4. Depois do jantar, você escolhe para onde ir. São três lugares, e cada um tem 4 pistas.
5. Ao final da noite o jogo mostra o desfecho, de acordo com o seu número de acertos.

## Mecânicas

### Barra de amor
- Começa em **50%**.
- Cada acerto dá **+10** e cada erro tira **15**.
- Se chegar a **0%**, a kwaii kitty conclui que você estava mentindo e vai embora. O jogo acaba na hora.

### Combo e ajuda do professor
- Cada acerto seguido aumenta o combo. Com **3 acertos seguidos**, o botão de ligar para o professor fica disponível.
- Ao ligar, o professor manda uma dica e **apaga 2 alternativas erradas**.
- Depois da ligação o combo volta a zero, e o professor atende **no máximo 3 vezes** por jogo.

### Locais
| Local | Papel |
|---|---|
| Restaurante | Primeiro encontro. É sempre o primeiro local. |
| Fliperama | Memórias: RAM, ROM, EEPROM e Flash. |
| Parque | Cache, memória de massa, DMA e microcontrolador. |
| Terraço | Barramentos, dual core e quad core. |

Você escolhe a ordem em que visita os três últimos locais.

### Conteúdo
São 16 termos de arquitetura de computadores: CPU, ULA, UC, registradores, RAM, ROM, EEPROM, Flash, cache, memória de massa, DMA, barramento de endereço, barramento de dados, microcontrolador, dual core e quad core.

## Finais

O jogo tem **5 finais**, definidos pela porcentagem de acertos (mais um final de derrota, caso a barra de amor zere):

| Acertos | Final |
|---|---|
| 100% | A casa dela |
| 80% a 94% | Beijo na praia, à noite |
| 70% a 79% | Segundo encontro |
| 21% a 69% | Ela te ignora (*ghosting*) |
| 0% a 20% | Ela te abandona |
| Barra de amor em 0% | Ela vai embora por você ter mentido |

Dá para jogar de novo no fim de cada partida para descobrir todos.

## Como rodar no seu computador

1. Baixe ou clone este repositório.
2. Abra a pasta no VS Code e use a extensão **Live Server** (clique em *Go Live*). Abrir o `index.html` direto com duplo clique também funciona, mas imagens e áudio podem não carregar em alguns navegadores.

## Como editar o jogo

Tudo o que se costuma mudar fica no bloco de edição no começo do `<script>` do `index.html`:

- `CFG`: nomes, pontos da barra de amor, tamanho do combo e usos do professor.
- `BG`, `SPRITES`, `CGS`, `SFX`, `MUSIC`: caminhos de imagens e sons.
- `PLACES`: lugares, falas e perguntas. Em cada pergunta, a **primeira** alternativa é a correta, porque o jogo embaralha a ordem ao mostrar.
- `ENDINGS`: textos e porcentagens dos finais.

## Estrutura de pastas

```
index.html
README.md
assets/
  images/     fundos
  sprites/    expressões da kwaii kitty
  cg/         imagens de cena (perfil, ghosting)
  prof/       foto do professor
  audio/      músicas e efeitos
```

## Créditos

- Desenvolvido por **Christian Miranda** como projeto da disciplina de **Aquitetura Computacional**.
- Imagens e sprites: Gemini e Pinterest.
- Codigo com ajuda de I.A (claude code).