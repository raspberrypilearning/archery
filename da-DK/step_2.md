## Sigte pile

Lad os starte med at lave en pil, der bevæger sig rundt på skærmen.

--- task ---

Åben Scratch-starterprojektet.

**Online**: åben starterprojektet hos [rpf.io/archeryon](http://rpf.io/archeryon){:target="_blank"}.

Hvis du har en Scratch-konto, kan du lave en kopi ved at klikke **Remix**.

**Offline**: åben [starterprojektet](http://rpf.io/p/en/archery-go){:target="_blank"} i offline-versionen af Scratch-redigeringsprogrammet.

Hvis du har brug for at downloade og installere offline-versionen, kan du finde det hos [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

I starterprojektet burde du se en baggrund med en målskive, og en sprite af et sigtekorn. Sigtekornet skal forestille at være pilen.

![Starter projekt](images/archery-starter.png)

--- /task ---

--- task ---

Når dit spil starter, skal der sendes en besked om at skyde en ny pil.

![Sigtekorn sprite](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (ny pil v)
```

--- /task ---

--- task ---

Når denne besked er modtaget, skal pilens position og størrelse indstilles.

![Sigtekorn sprite](images/target-sprite.png)

```blocks3
when I receive [ny pil v]
go to x: (-150) y: (-150)
set size to (400) %
```

--- /task ---

--- task ---

Klik på det grønne flag for at teste dit spil. Du burde se din pil blive større og flytte til hjørnet nederst til venstre på skærmen.

![Større sigtekorn sprite i hjørnet nederst til venstre på skærmen](images/archery-start-test.png)

--- /task ---

--- task ---

Tilføj kode til din pil så den `svæver`{:class="block3motion"} tilfældigt rundt på skærmen `for evigt`{:class="block3control"}.

![Sigtekorn sprite](images/target-sprite.png)

```blocks3
when I receive [ny pil v]
go to x: (-150) y: (-150)
set size to (400) %
+forever
glide (0.5) secs to x: (pick random (-150) to (150)) y: (pick random (-150) to (150))
end
```

--- /task ---

--- task ---

Test dit spil igen, og du burde se din pil bevæge sig tilfældigt rundt på skærmen.

![Sigtekorn i en anden position](images/archery-glide-test.png)

--- /task ---
