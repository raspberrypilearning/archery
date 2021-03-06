## Disparando flechas

Vamos a programar tu flecha para disparar cuando se presiona la barra espaciadora.

--- task ---

Detén el otro script (el que mueve la flecha) cuando se presiona la barra espaciadora.

![objeto blanco](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

--- /task ---

--- task ---

Prueba tu proyecto de nuevo. Esta vez, tu flecha debe dejar de moverse **cuando se presiona la barra espaciadora**.

--- /task ---

--- task ---

Anima tu flecha, para que parezca que se mueve hacia el blanco.

![objeto blanco](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

--- /task ---

--- task ---

Vuelve a probar tu juego. Esta vez, cuando presionas la barra espaciadora, deberías ver que tu flecha se vuelve más pequeña, como si se moviera hacia el blanco.

![diana con el punto de mira sobre ella](images/archery-animate-test.png)

--- /task ---

--- task ---

Una vez que su flecha está en el blanco, puedes decirle al jugador cuántos puntos obtuvo. Por ejemplo, podrían anotar 200 puntos por golpear el amarillo.

![objeto blanco](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
+if <touching color (#ffff00) ?> then
say [200 puntos] for (2) seconds
end
```

--- /task ---

--- task ---

También puedes reproducir un sonido si tocan el amarillo.

![objeto blanco](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <touching color (#ffff00) ?> then
+start sound (cheer v)
say [200 puntos] for (2) seconds
end
```

--- /task ---

--- task ---

Por último, tienes que transmitir de nuevo el mensaje `nueva flecha`{:class="block3events"} para obtener una nueva flecha.

![objeto blanco](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <touching color (#ffff00) ?> then
start sound (cheer v)
say [200 puntos] for (2) seconds
end
+broadcast (nueva flecha v)
```

--- /task ---