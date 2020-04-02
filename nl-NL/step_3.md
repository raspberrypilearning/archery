## Pijlen afschieten

Laten we de pijl programmeren om af te schieten wanneer de spatiebalk wordt ingedrukt.

\--- task \---

Stop het andere script (degene die de pijl beweegt) wanneer de spatiebalk wordt ingedrukt.

![doelwit sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Test je project opnieuw. Deze keer moet je pijl stoppen met bewegen **wanneer de spatiebalk wordt ingedrukt**.

\--- /task \---

\--- task \---

Animeer je pijl, zodat het lijkt alsof hij naar het doel beweegt.

![doelwit sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

Test je spel opnieuw. Deze keer zou je, als je op de spatiebalk drukt, je pijl kleiner moeten zien worden, alsof hij naar het doel toe beweegt.

![doelwit met het dradenkruis erop](images/archery-animate-test.png)

\--- /task \---

\--- task \---

Zodra je pijl het doel geraakt heeft, kun je de speler vertellen hoeveel punten hij heeft gescoord. Ze kunnen bijvoorbeeld 200 punten kunnen scoren als ze geel raken.

![doelwit sprite](images/target-sprite.png)

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

Je kunt ook een geluid afspelen als ze geel raken.

![doelwit sprite](images/target-sprite.png)

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

Ten slotte moet je het signaal `nieuwe pijl`{:class="block3events"} opnieuw uitzenden om een nieuwe pijl te krijgen.

![doelwit sprite](images/target-sprite.png)

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