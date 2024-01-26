## Strzelanie z łuku

Zaprogramuj celownik tak, że strzał zostanie oddany jeżeli klawisz spacji został naciśnięty.

\--- task \---

Zatrzymaj drugi skrypt (ten poruszający celownikiem) naciśnięciem spacji.

![celownik](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Przetestuj swój projekt ponownie. Tym razem twój celownik powinien przestać się poruszać **po naciśnięciu spacji**.

\--- /task \---

\--- task \---

Animuj celownik, tak żeby wyglądał, jakby zbliżał się do tarczy.

![celownik](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

Przetestuj swoją grę jeszcze raz. Tym razem, kiedy naciśniesz spację, powinieneś zobaczyć duszka zmniejszającego się, jakby poruszał się w kierunku tarczy.

![tarcza z celownikiem](images/archery-animate-test.png)

\--- /task \---

\--- task \---

Gdy strzał do tarczy zostanie oddany, możesz powiedzieć graczowi, ile punktów zdobył. Na przykład można zdobyć 200 punktów za trafienie w żółtą część.

![celownik](images/target-sprite.png)

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

Możesz także odtworzyć dźwięk, jeśli trafi się w żółtą część.

![celownik](images/target-sprite.png)

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

Na koniec musisz ponownie nadać komunikat `nowa strzała`{: class = "block3events"}, aby móc strzelić jeszcze raz.

![celownik](images/target-sprite.png)

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