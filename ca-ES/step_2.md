## Fletxes que apunten a un objectiu

Comencem creant una fletxa que es desplaça per la pantalla.

\--- task \---

Obriu el projecte inicial de Scratch.

**en línia**: obre el projecte d’inici a [rpf.io/archeryon](http://rpf.io/archeryon){:target="_ blank"}.

Si tens un compte a Scratch pots fer una còpia fent clic a **Reinventa**.

**Fora de línia**: obre el [projecte inicial](http://rpf.io/p/en/archery-go){:target="_ blank"} a l'editor fora de línia.

Si necessites descarregar i instal·lar l'editor fora de línia de Scratch, el pots trobar a [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

Al projecte d’inici, hauries de veure un escenari amb una diana com a objectiu i una icona de punt de mira.

![projectes d’inici](images/archery-starter.png)

\--- /task \---

\--- task \---

Quan comenci el joc, emet un missatge per disparar una fletxa nova.

![personatge destí](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

Un cop rebut aquest missatge, configura la posició i la mida de la fletxa.

![personatge destí](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

Fes clic a la bandera verda per provar el teu joc. Hauries de veure que la teva fletxa s’amplia i es desplaça a la part inferior esquerra de l’escenari.

![el personatge destí més gran a la part inferior esquerra de l’escenari](images/archery-start-test.png)

\--- /task \---

\--- task \---

Afegeix codi a la teva fletxa de manera que `llisqui`{:class="block3motion"} aleatòriament al voltant de l'escenari `per sempre`{:class="block3control"}.

![personatge destí](images/target-sprite.png)

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

Prova el teu joc de nou i hauries de veure que la teva fletxa es mou aleatòriament per l'escenari.

![objectiu en una posició diferent](images/archery-glide-test.png)

\--- /task \---