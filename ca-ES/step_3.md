## Disparar fletxes

Codifiquem la teva fletxa per disparar quan es prem la barra d’espai.

\--- task \---

Atura l'altre codi (el que fa moure la fletxa) quan prems la barra d'espai.

![target sprite](images/target-sprite.png)

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

![target sprite](images/target-sprite.png)

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

![target with the cross hair on it](images/archery-animate-test.png)

\--- /task \---

\--- task \---

Once your arrow is at the target, you can tell the player how many points they have scored. For example, they could score 200 points for hitting the yellow.

![target sprite](images/target-sprite.png)

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

You can also play a sound if they hit the yellow.

![target sprite](images/target-sprite.png)

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

Finally, you need to broadcast the `new arrow`{:class="block3events"} message again to get a new arrow.

![target sprite](images/target-sprite.png)

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