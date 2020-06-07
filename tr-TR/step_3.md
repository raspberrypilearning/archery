## Okları atma

Boşluk tuşuna basıldığında oku fırlatmak için okunuzun kodlarını yazalım.

\--- task \---

Boşluk çubuğuna basıldığında (oku hareket ettiren) diğer komut dosyasını durdurun.

![hedef kukla](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Kodunuzu tekrar test edin. Bu kez, **boşluk çubuğuna basıldığında** okunuz durmalı.

\--- /task \---

\--- task \---

Okunuzu canlandırın, böylece hedefe doğru hareket ediyormuş gibi görünür.

![hedef kukla](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

Oyununuzu tekrardan test edin. Bu kez, boşluk tuşuna bastığınızda, okunuzun hedefe doğru hareket ediyormuş gibi küçüldüğünü görmelisiniz.

![üzerinde artı işareti ile hedef](images/archery-animate-test.png)

\--- /task \---

\--- task \---

Okunuz hedefe ulaştığında, oyuncuya kaç puan kazandığını söyleyebilirsiniz. Örneğin, sarıya vurduklarında 200 puan alabilirler.

![target sprite](images/target-sprite.png)

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

Eğer sarıya vururlarsa bir de ses çıkmasını sağlayabilirsiniz.

![target sprite](images/target-sprite.png)

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

Son olarak, yeni bir ok almak için `yeni ok`{: class = "block3events"} mesajını tekrar yayınlamanız gerekir.

![target sprite](images/target-sprite.png)

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

\--- /görev \---