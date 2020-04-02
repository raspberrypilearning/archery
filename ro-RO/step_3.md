## Trasul cu săgeți

Să adăugăm cod săgeții tale pentru a o trage la apăsarea barei de spațiu.

\--- task \---

Oprește celălalt script (cel care deplasează săgeata) atunci când este apăsată bara de spațiu.

![personajul țintă](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Testează-ți proiectul din nou. De data aceasta, săgeata ta ar trebui să se oprească **atunci când este apăsată bara de spațiu**.

\--- /task \---

\--- task \---

Animează-ți săgeata, astfel încât să pară că se îndreaptă spre țintă.

![personajul țintă](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

Testează-ți jocul din nou. De data aceasta, când apeși bara de spațiu, ar trebui să vezi cum săgeata ta se micșorează, ca și cum s-ar îndrepta spre țintă.

![țintă cu crucea de pe ea](images/archery-animate-test.png)

\--- /task \---

\--- task \---

Odată ce săgeata ta a ajuns la țintă, poți spune jucătorului câte puncte a marcat. De exemplu, acesta poate înscrie 200 de puncte pentru țintirea părții galbene.

![personajul țintă](images/target-sprite.png)

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

De asemenea, poți reda un sunet dacă țintește partea galbenă.

![personajul țintă](images/target-sprite.png)

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

În cele din urmă, trebuie să difuzezi din nou mesajul `săgeată nouă`{:class="block3events"} pentru a obține o nouă săgeată.

![personajul țintă](images/target-sprite.png)

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