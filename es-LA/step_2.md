## Apuntando flechas

Comencemos creando una flecha que se mueva por la pantalla.

\--- task \---

Abre el proyecto inicial de Scratch.

**En línea**: abre el proyecto de inicio en [rpf.io/archeryon](http://rpf.io/archeryon){:target="_blank"}.

Si tienes una cuenta de Scratch puedes hacer una copia haciendo clic en **Remix**.

**Sin conexión**: abre el [proyecto de inicio](http://rpf.io/p/en/archery-go){:target="_blank"} en el editor sin conexión.

Si necesitas descargar e instalar el editor offline de Scratch, puedes encontrarlo en [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

En el proyecto inicial, deberías ver un fondo con una diana y un objeto en forma de punto de mira.

![proyectos iniciales](images/archery-starter.png)

\--- /task \---

\--- task \---

Cuando comience el juego, transmite un mensaje para disparar una nueva flecha.

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