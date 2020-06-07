## Okları nişan alma

Ekranda hareket eden bir ok oluşturarak başlayalım.

\--- görev \---

Scratch başlangıç projesini açın.

**Çevrimiçi**: başlangıç projesini [rpf.io/archeryon](http://rpf.io/archeryon){:target="_ blank"} linkinden açın.

Eğer bir Scratch hesabınız varsa, **Remix**'e tıklayarak bir kopyasını oluşturabilirsiniz.

** Çevrimdışı**: [başlangıç projesini](http://rpf.io/p/en/archery-go) Çevrimdışı editörde {:target ="_blank"} açın.

Scratch çevrimdışı editörünü indirip kurmanız gerekirse, bunu [ rpf.io/scratchoff adresinde bulabilirsiniz.](http://rpf.io/scratchoff) {: Hedef = "_ blank"}.

Başlangıç projesinde, bir hedef zemini ve bir artı şeklinde kukla görmelisiniz.

![başlangıç projeleri](images/archery-starter.png)

\--- görev \---

\--- görev \---

Oyununuz başladığında, yeni bir ok atmak için bir mesaj yayınlayın.

![hedef kukla](images/target-sprite.png)

```blocks3
yeşil bayrak tıkladığında yayınla (yeni ok v)
```

\--- görev \---

\--- görev \---

Bu mesaj alındıktan sonra, okun konumunu ve boyutunu ayarlayın.

![hedef kukla](images/target-sprite.png)

```blocks3
[yeni ok v]
aldığımda x: (-150)'ye y: (-150)'ye gidin
ve boyutu (%400) olarak ayarlayın.
```

\--- görev \---

\--- görev \---

Oyununuzu test etmek için yeşil bayrağa tıklayın. Okunuzun büyüdüğünü ve sahnenin sol alt köşesine hareket ettiğini görmelisiniz.

![sahnenin sol alt tarafında daha büyük hedef kukla](images/archery-start-test.png)

\--- görev \---

\--- görev \---

Sahnede etrafında rastgele `sürekli`{: class = "block3control"} `süzülmesi`{: class = "block3motion"} için okunuza kod ekleyin.

![hedef kukla](images/target-sprite.png)

```blocks3
[yeni ok v]
aldığımda x: (-150) y: (-150) konumuna gidin 
boyutu (400)% olarak belirleyin
+ sonsuza kadar
süzülme (0,5) saniye x'e: ((-150)'den (150)'ye kadar rastgele seçin) y'ye: ((-150)'den (150)'ye kadar rastgele seçin)
son
```

\--- görev \---

\--- görev \---

Oyununuzu tekrar test edin ve okunuzun sahnede rastgele hareket ettiğini görmelisiniz.

![hedef farklı bir konumda](images/archery-glide-test.png)

\--- görev \---