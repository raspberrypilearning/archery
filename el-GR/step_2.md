## Βέλη Στόχευσης

Ας ξεκινήσουμε δημιουργώντας ένα βέλος που κινείται στην οθόνη.

\--- task \---

Άνοιξε το αρχικό έργο Scratch.

**Online**: open the starter project at [rpf.io/archeryon](https://rpf.io/archeryon){:target="_blank"}.

Αν έχεις λογαριασμό Scratch μπορείς να δημιουργήσεις ένα αντίγραφο, κάνοντας κλικ στο κουμπί **Ανάμειξη**.

**Offline**: open the [starter project](https://rpf.io/p/en/archery-go){:target="_blank"} in the offline editor.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

Στο αρχικό έργο, θα πρέπει να δεις ένα σκηνικό στόχο και έναν σταυρό.

![αρχικά έργα](images/archery-starter.png)

\--- /task \---

\--- task \---

Όταν ξεκινήσει το παιχνίδι σου, μετάδωσε ένα μήνυμα για να τραβήξεις ένα νέο βέλος.

![αντικείμενο στόχος](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

Μόλις ληφθεί αυτό το μήνυμα, ρύθμισε τη θέση και το μέγεθος του βέλους.

![αντικείμενο στόχος](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

Κάνε κλικ στην πράσινη σημαία για να δοκιμάσεις το παιχνίδι σου. Θα πρέπει να δεις το βέλος σου να μεγαλώνει και να μετακινείται στην κάτω αριστερή πλευρά της σκηνής.

![αντικείμενο μεγαλύτερου στόχου στο κάτω αριστερό μέρος της σκηνής](images/archery-start-test.png)

\--- /task \---

\--- task \---

Πρόσθεσε κώδικα στο βέλος σου έτσι ώστε να `εναλλάσσεται`{: class = "block3motion"} τυχαία γύρω από τη σκηνή `για πάντα`{: class = "block3control"}.

![αντικείμενο στόχος](images/target-sprite.png)

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

Δοκίμασε ξανά το παιχνίδι σου και θα πρέπει να δεις το βέλος σου να κινείται τυχαία γύρω από τη σκηνή.

![στόχος σε διαφορετική θέση](images/archery-glide-test.png)

\--- /task \---