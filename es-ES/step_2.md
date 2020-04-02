## Apuntando las flechas

Comencemos creando una flecha que se mueva por la pantalla.

\--- task \---

Abre el proyecto inicial de Scratch.

**En línea**: abre el proyecto inicial en [rpf.io/archeryon](http://rpf.io/archeryon){:target="_blank"}.

Si tienes una cuenta de Scratch puedes hacer una copia haciendo clic en **Remix**.

**Sin conexión**: abre el [proyecto inicial](http://rpf.io/p/en/archery-go){:target=_blank"} en el editor sin conexión (offline).

Si necesitas descargar e instalar el editor offline de Scratch, puedes encontrarlo en [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

En el proyecto inicial, deberías ver un fondo con una diana y un objeto en forma de punto de mira.

![proyectos iniciales](images/archery-starter.png)

\--- /task \---

\--- task \---

Cuando comience el juego, difunde un mensaje para disparar una nueva flecha.

![objeto objetivo](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

Una vez recibido este mensaje, configura la posición y el tamaño de la flecha.

![objeto objetivo](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

Haz clic en la bandera verde para probar tu juego. Deberías ver que tu flecha se agranda y se mueve hacia la esquina inferior izquierda del escenario.

![objeto de objetivo más grande en la parte inferior izquierda del escenario](images/archery-start-test.png)

\--- /task \---

\--- task \---

Añade código a tu flecha para que `se deslice`{:class="block3motion"} al azar por el escenario `por siempre`{:class="block3control"}.

![objeto objetivo](images/target-sprite.png)

```blocks3
al recibir [nueva flecha v]
ir a x: (-150) y: (-150)
fijar tamaño al (400)%
+ para siempre
deslizar en (0.5) segs a x: (número aleatorio entre (-150) y (150)) y: (número aleatorio entre (-150) y (150))
fin
```

\--- /task \---

\--- task \---

Vuelve a probar tu juego y verás que tu flecha se mueve aleatoriamente por el escenario.

![objetivo en una posición diferente](images/archery-glide-test.png)

\--- /task \---