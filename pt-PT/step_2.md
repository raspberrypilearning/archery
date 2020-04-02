## Apontando flechas

Vamos começar por criar uma flecha que se move pelo ecrã.

\--- task \---

Abre o projeto inicial do Scratch.

**Online:** abre o projeto inicial em [rpf.io/archeryon](http://rpf.io/archeryon){:target="_blank"}.

Se tiveres uma 'conta Scratch' podes fazer uma cópia ao clicares **Remix**.

**Offline**: Abre o [projecto inicial](http://rpf.io/p/en/archery-go){:target="_blank"} no editor offline.

Se precisares de descarregar e instalar o editor offline do Scratch, podes encontrá-lo em [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

No projeto inicial, vais ver um cenário com um alvo e um ator com a mira.

![projetos iniciais](images/archery-starter.png)

\--- /task \---

\--- task \---

Quando o jogo começar, transmite uma mensagem para disparar uma nova flecha.

![ator alvo](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

Depois dessa mensagem ser recebida, define a posição e o tamanho da flecha.

![ator alvo](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

Clica na bandeira verde para testar o teu jogo. Deves ver a tua flecha aumentar de tamanho e ir para o canto inferior esquerdo do palco.

![ator alvo maior no canto inferior esquerdo do palco](images/archery-start-test.png)

\--- /task \---

\--- task \---

Adiciona código à tua flecha para que ela `deslize`{: class = "block3motion"} ao acaso pelo palco `para sempre`{: class = "block3control"}.

![ator alvo](images/target-sprite.png)

```blocks3
quando eu receber [nova flecha v]
vai para x: (-150) y: (-150)
define o tamanho para (400)%
+ para sempre
desliza (0,5) segundos para x: (escolha aleatória (-150) para (150)) y: (escolha aleatória (-150) a (150))
fim
```

\--- /task \---

\--- task \---

Testa o jogo novamente e verás a flecha a mover-se ao acaso pelo palco.

![alvo numa posição diferente](images/archery-glide-test.png)

\--- /task \---