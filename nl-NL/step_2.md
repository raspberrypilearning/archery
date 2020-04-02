## Richten van pijlen

Laten we beginnen met het maken van een pijl die over het scherm beweegt.

\--- task \---

Open het Scratch startproject.

**Online**: open het startproject via [rpf.io/archeryon](http://rpf.io/archeryon){:target="_ blank"}.

Als je een Scratch account hebt, kun je een kopie maken door op **Remix** te klikken.

**Offline**: open het [startproject](http://rpf.io/p/en/archery-go){:target="_ blank"} in de offline editor.

Als je de Scratch offline editor wilt downloaden en installeren dan kan je die vinden op [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

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
wanneer ik signaal [nieuwe pijl v] ontvang
ga naar x: (-150) y: (-150)
maak grootte (400)%
+herhaal
schuif in (0.5) sec. naar x: (willekeurig getal tussen (-150) en (150)) y: (willekeurig getal tussen (-150) en (150))
einde
```

\--- /task \---

\--- task \---

Test je spel opnieuw en je zou je pijl willekeurig over het speelveld moeten zien bewegen.

![doelwit in een andere positie](images/archery-glide-test.png)

\--- /task \---