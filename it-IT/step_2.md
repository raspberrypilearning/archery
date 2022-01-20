## Mirare

Cominciamo creando una freccia che si sposta sullo schermo.

--- task ---

Apri il progetto iniziale.

**Online**: apri il progetto iniziale su [scratch.mit.edu/projects/382065845](https://scratch.mit.edu/projects/382065845){:target="_blank"}.

Se hai un account su Scratch, puoi farne una copia cliccando su **Remix**.

**Offline**: apri il [progetto iniziale](https://rpf.io/p/it-IT/archery-go){:target="_blank"} nell'editor offline.

Se hai bisogno di scaricare ed installare l'editor Scratch offline, puoi trovarlo su [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

Nel progetto iniziale, dovresti vedere un bersaglio di sfondo e uno sprite rappresentante un mirino.

![progetti iniziali](images/archery-starter.png)

--- /task ---

--- task ---

All'inizio del gioco, trasmetti un messaggio per lanciare una nuova freccia.

![sprite bersaglio](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (nuova freccia v)
```

--- /task ---

--- task ---

Una volta ricevuto questo messaggio, imposta la posizione e le dimensioni della freccia.

![sprite bersaglio](images/target-sprite.png)

```blocks3
when I receive [nuova freccia v]
go to x: (-150) y: (-150)
set size to (400) %
```

--- /task ---

--- task ---

Fai clic sulla bandiera verde per testare il tuo gioco. Dovresti vedere la tua freccia ingrandirsi e spostarsi nella parte inferiore sinistra dello stage.

![sprite bersaglio più grande nella parte inferiore sinistra dello stage](images/archery-start-test.png)

--- /task ---

--- task ---

Aggiungi il codice alla tua freccia in modo che `scivoli`{:class="block3motion"} in modo casuale attorno allo stage `per sempre`{:class="block3control"}.

![sprite bersaglio](images/target-sprite.png)

```blocks3
when I receive [nuova freccia v]
go to x: (-150) y: (-150)
set size to (400) %
+forever
glide (0.5) secs to x: (pick random (-150) to (150)) y: (pick random (-150) to (150))
end
```

--- /task ---

--- task ---

Prova di nuovo il tuo gioco, dovresti vedere la tua freccia muoversi in modo casuale sullo stage.

![bersaglio in una posizione diversa](images/archery-glide-test.png)

--- /task ---
