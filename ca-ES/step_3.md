## Disparar fletxes

Codifiquem la teva fletxa per disparar quan es prem la barra d’espai.

\--- task \---

Atura l'altre codi (el que fa moure la fletxa) quan prems la barra d'espai.

![personatge destí](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Prova el teu projecte de nou. Aquest cop, la teva fletxa s'hauria de deixar de moure **quan es prem la barra d'espai**.

\--- /task \---

\--- task \---

Anima la teva fletxa de manera que sembli que s'està movent cap a l'objectiu.

![personatge destí](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

Prova el teu joc de nou. Aquest cop, quan premis la barra d’espai, hauries de veure que la teva fletxa es fa més petita, com si anés cap a l’objectiu.

![objectiu amb el punt de mira a sobre](images/archery-animate-test.png)

\--- /task \---

\--- task \---

Un cop la teva fletxa estigui a l’objectiu, pots indicar al jugador quants punts ha anotat. Per exemple, podrien aconseguir 200 punts per colpejar el groc.

![personatge destí](images/target-sprite.png)

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

També pots reproduir un so si toquen el groc.

![personatge destí](images/target-sprite.png)

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

Finalment, heu de tornar a emetre el missatge `nova fletxa`{:class="block3events"} per obtenir una fletxa nova.

![personatge destí](images/target-sprite.png)

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