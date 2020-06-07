## Okları nişan alma

Ekranda hareket eden bir ok oluşturarak başlayalım.

\--- task \---

Scratch başlangıç projesini açın.

**Çevrimiçi**: başlangıç projesini [rpf.io/archeryon](http://rpf.io/archeryon){:target="_ blank"} linkinden açın.

Eğer bir Scratch hesabınız varsa, **Remix**'e tıklayarak bir kopyasını oluşturabilirsiniz.

** Çevrimdışı**: [başlangıç projesini](http://rpf.io/p/en/archery-go) Çevrimdışı editörde {:target ="_blank"} açın.

Scratch çevrimdışı editörünü indirip kurmanız gerekirse, bunu [ rpf.io/scratchoff adresinde bulabilirsiniz.](http://rpf.io/scratchoff) {: Hedef = "_ blank"}.

Başlangıç projesinde, bir hedef zemini ve bir artı şeklinde kukla görmelisiniz.

![starter projects](images/archery-starter.png)

\--- /task \---

\--- task \---

Oyununuz başladığında, yeni bir ok atmak için bir mesaj yayınlayın.

![target sprite](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

Bu mesaj alındıktan sonra, okun konumunu ve boyutunu ayarlayın.

![target sprite](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

Oyununuzu test etmek için yeşil bayrağa tıklayın. Okunuzun büyüdüğünü ve sahnenin sol alt köşesine hareket ettiğini görmelisiniz.

![larger target sprite in bottom left of stage](images/archery-start-test.png)

\--- /task \---

\--- task \---

Sahnede etrafında rastgele `sürekli`{: class = "block3control"} `süzülmesi`{: class = "block3motion"} için okunuza kod ekleyin.

![target sprite](images/target-sprite.png)

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

Oyununuzu tekrar test edin ve okunuzun sahnede rastgele hareket ettiğini görmelisiniz.

![target in a different position](images/archery-glide-test.png)

\--- /task \---