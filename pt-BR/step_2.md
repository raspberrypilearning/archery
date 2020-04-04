## Mirando as flechas

Vamos começar criando uma mira que se move pela tela.

\--- task \---

Abra o projeto inicial do Scratch.

**Online**: abra o projeto inicial em [rpf.io/archeryon](http://rpf.io/archeryon){:target="_blank"}.

Se você tiver uma conta do Scratch, pode fazer uma cópia clicando em **Remisturar**.

**Offline**: abra o [projeto inicial](http://rpf.io/p/en/archery-go){:target="_ blank"} no editor offline.

Se você precisar baixar e instalar o editor offline do Scratch, você pode encontrá-lo em [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

No projeto inicial, você verá um cenário de alvo e um ator de mira.

![projetos iniciais](images/archery-starter.png)

\--- /task \---

\--- task \---

Quando o jogo começar, transmita uma mensagem para disparar uma nova flecha.

![ator alvo](images/target-sprite.png)

```blocks3
quando bandeira verde for clicado
transmita(new arrow v)
```

\--- /task \---

\--- task \---

Once this message has been received, set the arrow's position and size.

![ator alvo](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

Click the green flag to test your game. You should see your arrow get bigger and move to the bottom-left of the stage.

![ator alvo maior no canto inferior esquerdo do palco](images/archery-start-test.png)

\--- /task \---

\--- task \---

Add code to your arrow so that it `glides`{:class="block3motion"} randomly around the stage `forever`{:class="block3control"}.

![sprite alvo](images/target-sprite.png)

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

Test your game again, and you should see your arrow move randomly around the stage.

![alvo em uma posição diferente](images/archery-glide-test.png)

\--- /task \---