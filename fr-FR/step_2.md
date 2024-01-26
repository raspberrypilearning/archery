## Viser avec les flèches

Commençons par créer une flèche qui se déplace sur l'écran.

\--- task \---

Ouvre le projet de démarrage Scratch.

**Online**: open the starter project at [rpf.io/archeryon](https://rpf.io/archeryon){:target="_blank"}.

Si tu as un compte Scratch, tu peux en créer une copie en cliquant sur **Remix**.

**Offline**: open the [starter project](https://rpf.io/p/en/archery-go){:target="_blank"} in the offline editor.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

Dans le projet de démarrage, tu devrais voir un arrière-plan cible et un sprite réticule.

![projets de démarrage](images/archery-starter.png)

\--- /task \---

\--- task \---

Lorsque ton jeu démarre, diffuse un message pour tirer une nouvelle flèche.

![sprite cible](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

Une fois ce message reçu, définis la position et la taille de la flèche.

![sprite cible](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

Clique sur le drapeau vert pour tester ton jeu. Tu devrais voir ta flèche grossir et se déplacer en bas à gauche de la scène.

![sprite cible plus grand en bas à gauche de la scène](images/archery-start-test.png)

\--- /task \---

\--- task \---

Ajoute du code à ta flèche pour qu'elle `glisse`{:class="block3motion"} de façon aléatoire autour de la scène `indéfiniment`{:class="block3control"}.

![sprite cible](images/target-sprite.png)

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

Teste à nouveau ton jeu et tu devrais voir ta flèche se déplacer de façon aléatoire sur la scène.

![cible dans une position différente](images/archery-glide-test.png)

\--- /task \---