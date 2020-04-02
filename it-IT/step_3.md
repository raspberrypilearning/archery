## Scoccare le frecce

Programmiamo la freccia in modo da scoccarla quando viene premuta la barra spaziatrice.

\--- task \---

Ferma l'altro script (quello che sposta la freccia) quando viene premuta la barra spaziatrice.

![sprite bersaglio](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Prova di nuovo il tuo codice. Questa volta, la freccia dovrebbe smettere di muoversi **quando si preme la barra spaziatrice**.

\--- /task \---

\--- task \---

Anima la freccia, in modo che sembri muoversi verso il bersaglio.

![sprite bersaglio](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

Prova di nuovo il tuo gioco. Questa volta, quando premi la barra spaziatrice, dovresti vedere la tua freccia diventare più piccola, come se si stesse muovendo verso il bersaglio.

![bersaglio con il mirino su di esso](images/archery-animate-test.png)

\--- /task \---

\--- task \---

Una volta che la tua freccia è sul bersaglio, puoi dire al giocatore quanti punti ha realizzato. Ad esempio, potrebbero realizzare 200 punti colpendo il giallo.

![sprite bersaglio](images/target-sprite.png)

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

Puoi anche riprodurre un suono se colpiscono il giallo.

![sprite bersaglio](images/target-sprite.png)

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

Infine, è necessario trasmettere nuovamente il messaggio `nuova freccia`{:class="block3events"} per ottenere una nuova freccia.

![sprite bersaglio](images/target-sprite.png)

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