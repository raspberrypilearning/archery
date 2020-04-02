## Tirer des flèches

Codons ta flèche pour tirer lorsque tu appuies sur la barre d'espace.

\--- task \---

Arrête l'autre script (celui qui déplace la flèche) lorsque la barre d'espace est enfoncée.

![sprite cible](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Teste ton projet à nouveau. Cette fois, ta flèche devrait cesser de bouger **lorsque la barre d'espace est enfoncée**.

\--- /task \---

\--- task \---

Anime ta flèche, de manière à ce qu'elle semble se déplacer vers la cible.

![sprite cible](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

Teste à nouveau ton jeu. Cette fois, lorsque tu appuies sur la barre d'espace, tu devrais voir ta flèche devenir plus petite, comme si elle se dirigeait vers la cible.

![cible avec le réticule sur elle](images/archery-animate-test.png)

\--- /task \---

\--- task \---

Une fois que ta flèche est sur la cible, tu peux dire au joueur combien de points il a marqués. Par exemple, ils pourraient marquer 200 points pour avoir frappé le jaune.

![sprite cible](images/target-sprite.png)

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

Tu peux également jouer un son s'ils frappent le jaune.

![sprite cible](images/target-sprite.png)

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

Enfin, tu dois diffuser à nouveau le message `nouvelle flèche`{:class="block3events"} pour obtenir une nouvelle flèche.

![sprite cible](images/target-sprite.png)

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