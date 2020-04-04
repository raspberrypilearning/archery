## Mirando as flechas

Vamos começar criando uma mira que se move pela tela.

\--- task \---

Open the Scratch starter project.

**Online**: open the starter project at [rpf.io/archeryon](http://rpf.io/archeryon){:target="_blank"}.

If you have a Scratch account you can make a copy by clicking **Remix**.

**Offline**: open the [starter project](http://rpf.io/p/en/archery-go){:target="_blank"} in the offline editor.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

In the starter project, you should see a target backdrop and a cross hair sprite.

![projetos iniciais](images/archery-starter.png)

\--- /task \---

\--- task \---

When your game starts, broadcast a message to shoot a new arrow.

![ator alvo](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
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