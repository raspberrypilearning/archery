## Celowanie strzałami

Zacznijmy od stworzenia celownika, który porusza się po ekranie.

--- task ---

Otwórz projekt startowy Scratch.

**Online**: otwórz projekt startowy na stronie [rpf.io/archeryon](https://rpf.io/archeryon){:target="_blank"}.

Jeśli masz konto Scratch, możesz wykonać kopię klikając **Remiks**.

**Offline**: otwórz [projekt startowy](https://rpf.io/p/pl-PL/archery-go){:target="_blank"} w edytorze offline.

Jeśli musisz pobrać i zainstalować edytor offline Scratcha, znajdziesz go na stronie [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

W projekcie startowym powinieneś zobaczyć tło docelowe i duszka celownika.

![projekty startowe](images/archery-starter.png)

--- /task ---

--- task ---

Po uruchomieniu gry użyj bloku "nadaj komunikat", aby przygotować nową strzałę.

![celownik](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (nowa strzała v)
```

--- /task ---

--- task ---

Po otrzymaniu komunikatu ustaw pozycję i rozmiar celownika.

![celownik](images/target-sprite.png)

```blocks3
when I receive [nowa strzała v]
go to x: (-150) y: (-150)
set size to (400) %
```

--- /task ---

--- task ---

Kliknij zieloną flagę, aby przetestować grę. Powinieneś zobaczyć swój celownik powiększający się i przechodzący do dolnej lewej części sceny.

![większy celownik w lewym dolnym rogu sceny](images/archery-start-test.png)

--- /task ---

--- task ---

Dodaj pętlę `zawsze`{:class="block3control"} do kodu celownika. W pętli powinna znaleźć się intrukcja `leć przez`{:class="block3motion"}, która pozwoli duszkowi przemieszczać się losowo po scenie.

![celownik](images/target-sprite.png)

```blocks3
when I receive [nowa strzała v]
go to x: (-150) y: (-150)
set size to (400) %
+forever
glide (0.5) secs to x: (pick random (-150) to (150)) y: (pick random (-150) to (150))
end
```

--- /task ---

--- task ---

Przy ponownym uruchomieniu gry, duszek powinien poruszać się losowo po scenie.

![cel w innej pozycji](images/archery-glide-test.png)

--- /task ---
