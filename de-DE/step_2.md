## Pfeile zielen

Beginnen wir mit der Erstellung eines Pfeils, der sich auf dem Bildschirm bewegt.

\--- task \---

Öffne das Scratch Start-Projekt.

**Online**: open the starter project at [rpf.io/archeryon](https://rpf.io/archeryon){:target="_blank"}.

Wenn du bereits einen Scratch-Account besitzt, kannst du dir durch Klick auf **Remix** eine Kopie anlegen.

**Offline**: open the [starter project](https://rpf.io/p/en/archery-go){:target="_blank"} in the offline editor.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

Im Start-Projekt solltest du eine Zielkulisse und ein Fadenkreuz sehen.

![Start-Projekt](images/archery-starter.png)

\--- /task \---

\--- task \---

Wenn dein Spiel beginnt, sende eine Nachricht um einen neuen Pfeil zu schießen.

![Ziel Figur](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

Sobald diese Nachricht empfangen wurde, lege die Position und Größe des Pfeils fest.

![Ziel Figur](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

Klicke auf die grüne Flagge, um dein Spiel zu testen. Du solltest sehen, dass der Pfeil größer wird und sich auf der Zielscheibe nach links unten bewegt.

![größeres Ziel unten links auf der Bühne](images/archery-start-test.png)

\--- /task \---

\--- task \---

Fügen deinem Pfeil Code hinzu, damit er `fortlaufend`{:class ="block3control"} zufällig um das Ziel `gleitet`{:class ="block3motion"}.

![Ziel Figur](images/target-sprite.png)

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

Teste dein Spiel erneut und du solltest sehen, wie sich dein Pfeil zufällig über die Zielscheibe bewegt.

![Ziel in einer anderen Position](images/archery-glide-test.png)

\--- /task \---