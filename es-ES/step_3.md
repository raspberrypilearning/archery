## Disparando flechas

Vamos a programar la flecha para dispararla cuando pulsemos la barra espaciadora.

\--- task \---

Detén el otro script (el que mueve la flecha) cuando se pulse la barra espaciadora.

![objeto objetivo](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Prueba tu proyecto de nuevo. Esta vez, tu flecha debe dejar de moverse **cuando se presiona la barra espaciadora**.

\--- /task \---

\--- task \---

Anima tu flecha para que parezca que se mueve hacia el objetivo.

![objeto objetivo](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

Prueba tu juego de nuevo. Esta vez, cuando pulses la barra espaciadora, deberías ver que tu flecha se hace más pequeña, como si se estuviera moviendo hacia la diana.

![diana con el punto de mira sobre ella](images/archery-animate-test.png)

\--- /task \---

\--- task \---

Cuando la flecha llegue a la diana le puedes decir al jugador o jugadora los puntos que ha conseguido. Por ejemplo, podrían anotar 200 puntos por golpear el amarillo.

![objeto objetivo](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
+if <touching color (#ffff00) ?> then
say [200 points] for (2) seconds
end
```

\--- /task \---

\--- task \---

También puedes reproducir un sonido si dan al amarillo.

![objeto objetivo](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <touching color (#ffff00) ?> then
+start sound (cheer v)
say [200 points] for (2) seconds
end
```

\--- /task \---

\--- task \---

Finalmente, debes difundir el mensaje `nueva flecha`{:class="block3events"} para obtener una nueva flecha.

![objeto objetivo](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <touching color (#ffff00) ?> then
start sound (cheer v)
say [200 points] for (2) seconds
end
+broadcast (new arrow v)
```

\--- /task \---