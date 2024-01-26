## Ținta săgeților

Să începem prin crearea unei săgeți care se mișcă pe ecran.

\--- task \---

Deschide proiectul Scratch de început.

**Online**: open the starter project at [rpf.io/archeryon](https://rpf.io/archeryon){:target="_blank"}.

Dacă ai un cont Scratch, poți să creezi o copie dând click pe **Remix**.

**Offline**: open the [starter project](https://rpf.io/p/en/archery-go){:target="_blank"} in the offline editor.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

În proiectul de început, ar trebui să vezi un fundal de țintă și un costum cu o cruce roșie.

![proiecte de început](images/archery-starter.png)

\--- /task \---

\--- task \---

Când jocul tău începe, difuzează un mesaj pentru a trage o nouă săgeată.

![sprite țintă](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

Odată ce acest mesaj a fost primit, setează poziția și dimensiunea săgeții.

![sprite țintă](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

Dă click pe steagul verde pentru a-ți testa jocul. Ar trebui să-ți vezi săgeata că se mărește și că se mișcă în partea de stângă jos a scenei.

![sprite țintă mai mare în partea stângă jos a etapei](images/archery-start-test.png)

\--- /task \---

\--- task \---

Adaugă o secvență de cod la săgeata ta astfel încât aceasta să `alunece`{: class = "block3motion"} la întâmplare în jurul scenei `la infinit`{: class = "block3control"}.

![sprite țintă](images/target-sprite.png)

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

Testează-ți jocul din nou și ar trebui să vezi cum săgeata ta se mișcă aleatoriu în jurul scenei.

![țintă într-o poziție diferită](images/archery-glide-test.png)

\--- /task \---