## تصويب السهام

لنبدأ بإنشاء سهم يتحرك حول الشاشة.

\--- task \---

افتح مشروع جديد من برنامج سكراتش.

**Online**: open the starter project at [rpf.io/archeryon](https://rpf.io/archeryon){:target="_blank"}.

اذا كنت تملك حساب على منصة السكراتش (Scratch) فيمكنك عمل نسخة بالضغط على **Remix**.

**Offline**: open the [starter project](https://rpf.io/p/en/archery-go){:target="_blank"} in the offline editor.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

في بداية المشروع ، من المفترض أن ترى خلفية الهدف مع علامة التصويب (+).

![مشاريع البداية](images/archery-starter.png)

\--- /task \---

\--- task \---

عندما تبدأ اللعبة ، قم بارسال رسالة لتصويب سهم جديد.

![كائن الهدف](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

بمجرد استلام هذه الرسالة ، قم بتحديد موقع السهم وحجمه.

![كائن الهدف](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

انقر على العلم الأخضر لاختبار لعبتك. يجب أن ترى سهمك يكبر ويتحرك إلى أسفل يسار المنصة.

![أكبر كائن الهدف في أسفل يسار المنصة](images/archery-start-test.png)

\--- /task \---

\--- task \---

أضف تعليمات برمجية إلى سهمك بحيث يكون `ينساب`{: class = "block3motion"} عشوائيًا حول المنصة `إلى الأبد`{: class = "block3control"}.

![كائن الهدف](images/target-sprite.png)

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

اختبر لعبتك مرة أخرى ، ويجب أن ترى سهمك يتحرك بشكل عشوائي حول المنصة .

![الهدف في موقع مختلف](images/archery-glide-test.png)

\--- /task \---