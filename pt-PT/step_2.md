## Apontando flechas

Vamos começar por criar uma flecha que se move pelo ecrã.

\--- task \---

Abre o projeto inicial do Scratch.

**Online**: open the starter project at [rpf.io/archeryon](https://rpf.io/archeryon){:target="_blank"}.

Se tiveres uma 'conta Scratch' podes fazer uma cópia ao clicares **Remix**.

**Offline**: open the [starter project](https://rpf.io/p/en/archery-go){:target="_blank"} in the offline editor.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

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
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
+forever
glide (0.5) secs to x: (pick random (-150) to (150)) y: (pick random (-150) to (150))
end
```

\--- /task \---

\--- task \---

Testa o jogo novamente e verás a flecha a mover-se ao acaso pelo palco.

![alvo numa posição diferente](images/archery-glide-test.png)

\--- /task \---