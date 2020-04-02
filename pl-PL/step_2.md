## Celowanie strzałami

Zacznijmy od stworzenia celownika, który porusza się po ekranie.

\--- task \---

Otwórz projekt startowy Scratch.

**Online**: otwórz projekt startowy na stronie [rpf.io/archeryon](http://rpf.io/archeryon){:target="_blank"}.

Jeśli masz konto Scratch, możesz wykonać kopię klikając **Remiks**.

**Offline**: otwórz [ projekt startowy ](http://rpf.io/p/en/archery-go) {:target="_ blank"} w edytorze offline.

Jeśli musisz pobrać i zainstalować edytor offline Scratcha, znajdziesz go na stronie [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

W projekcie startowym powinieneś zobaczyć tło docelowe i duszka celownika.

![projekty startowe](images/archery-starter.png)

\--- /task \---

\--- task \---

Po uruchomieniu gry wyślij wiadomość, aby wystrzelić nową strzałę.

![celownik](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

Po otrzymaniu wiadomości ustaw pozycję i rozmiar celownika.

![celownik](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

Kliknij zieloną flagę, aby przetestować grę. Powinieneś zobaczyć swój celownik powiększający się i przechodzący do dolnej lewej części sceny.

![większy celownik w lewym dolnym rogu sceny](images/archery-start-test.png)

\--- /task \---

\--- task \---

Dodaj pętlę `zawsze`{: class = "block3control"} do kodu celownika. W pętli powinna znaleźć się intrukcja `leć przez`{: class = "block3motion"}, która pozwoli duszkowi przemieszczać się losowo po scenie.

![celownik](images/target-sprite.png)

```blocks3
kiedy otrzymam [nowa strzała v]
idź do x: (-150) y: (-150)
ustaw rozmiar na (400)%
+zawsze
leć przez (0,5) sekund do x: (losuj liczbę od (-150) do (150)) y: (losuj liczbę od (-150) do (150))
koniec
```

\--- /task \---

\--- task \---

Przy ponownym uruchomieniu gry, duszek powinien poruszać się losowo po scenie.

![cel w innej pozycji](images/archery-glide-test.png)

\--- /task \---