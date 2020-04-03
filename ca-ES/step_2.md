## Fletxes que apunten a un objectiu

Comencem creant una fletxa que es desplaça per la pantalla.

\--- task \---

Obriu el projecte inicial de Scratch.

**en línia**: obre el projecte d’inici a [rpf.io/archeryon](http://rpf.io/archeryon){:target="_ blank"}.

Si tens un compte a Scratch pots fer una còpia fent clic a **Reinventa**.

**Fora de línia**: obre el [projecte inicial](http://rpf.io/p/en/archery-go){:target="_ blank"} a l'editor fora de línia.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

In the starter project, you should see a target backdrop and a cross hair sprite.

![starter projects](images/archery-starter.png)

\--- /task \---

\--- task \---

When your game starts, broadcast a message to shoot a new arrow.

![target sprite](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

Once this message has been received, set the arrow's position and size.

![target sprite](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

Click the green flag to test your game. You should see your arrow get bigger and move to the bottom-left of the stage.

![larger target sprite in bottom left of stage](images/archery-start-test.png)

\--- /task \---

\--- task \---

Add code to your arrow so that it `glides`{:class="block3motion"} randomly around the stage `forever`{:class="block3control"}.

![target sprite](images/target-sprite.png)

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

![target in a different position](images/archery-glide-test.png)

\--- /task \---