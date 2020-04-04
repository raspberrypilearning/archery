## Pfeile schießen

Lass uns deinen Pfeil coden, der abgeschossen wird, wenn die Leertaste gedrückt wird.

\--- task \---

Stoppe das andere Skript (das den Pfeil bewegt), wenn du die Leertaste drückst.

![target sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Teste dein Projekt erneut. Dieses Mal sollte dein Pfeil aufhören sich zu bewegen, **wenn die Taste Leertaste gedrückt wird**.

\--- /task \---

\--- task \---

Animiere deinen Pfeil so, dass er sich auf das Ziel zubewegt.

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

Teste dein Spiel erneut. Dieses Mal, wenn du die Leertaste drückst, solltest du sehen, dass der Pfeil kleiner wird, als ob er sich in Richtung des Ziels bewegt.

![target with the cross hair on it](images/archery-animate-test.png)

\--- /task \---

\--- task \---

Sobald dein Pfeil am Ziel ist, kannst du dem Spieler mitteilen, wie viele Punkte er erzielt hat. Zum Beispiel könnte man 200 Punkte erzielen, wenn man das gelbe Feld trifft.

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

Du kannst auch einen Ton abspielen, wenn das gelbe Feld getroffen wird.

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

Am Ende musst du die `neuer Pfeil `{:class="block3events"} Nachricht erneut senden, um einen neuen Pfeil zu erhalten.

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