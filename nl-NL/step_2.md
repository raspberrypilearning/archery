## Richten van pijlen

Laten we beginnen met het maken van een pijl die over het scherm beweegt.

\--- task \---

Open het Scratch startproject.

**Online**: open the starter project at [rpf.io/archeryon](https://rpf.io/archeryon){:target="_blank"}.

Als je een Scratch account hebt, kun je een kopie maken door op **Remix** te klikken.

**Offline**: open the [starter project](https://rpf.io/p/en/archery-go){:target="_blank"} in the offline editor.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

In het startproject zou je een doelwit-achtergrond en een dradenkruis moeten zien.

![startprojecten](images/archery-starter.png)

\--- /task \---

\--- task \---

Wanneer je spel begint, zend dan een signaal uit om een nieuwe pijl te schieten.

![doelwit sprite](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

Zodra dit signaal is ontvangen, stel je de positie en grootte van de pijl in.

![doelwit sprite](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

Klik op de groene vlag om je spel te testen. Je zou je pijl groter moeten zien worden en naar de linkerbenedenhoek van het podium zien gaan.

![grotere doelwit sprite linksonder op het podium](images/archery-start-test.png)

\--- /task \---

\--- task \---

Voeg code toe aan je pijl zodat deze `continu`{:class="block3control"} willekeurig rond `beweegt`{:class="block3motion"}.

![doelwit sprite](images/target-sprite.png)

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

Test je spel opnieuw en je zou je pijl willekeurig over het speelveld moeten zien bewegen.

![doelwit in een andere positie](images/archery-glide-test.png)

\--- /task \---