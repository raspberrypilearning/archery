## تصويب السهام

لنبدأ بإنشاء سهم يتحرك حول الشاشة.

--- task ---

افتح مشروع جديد من برنامج سكراتش.

**متصل بالانترنت**: افتح مشروع جديد من هنا [scratch.mit.edu/projects/382054880](https://scratch.mit.edu/projects/382054880){:target="_blank"}.

اذا كنت تملك حساب على منصة السكراتش (Scratch) فيمكنك عمل نسخة بالضغط على **Remix**.

**دون اتصال بالانترنت**: افتح [المشروع المبدئي](https://rpf.io/p/ar-SA/archery-go){:target="_blank"} عبر المحرر الموجود على جهازك.

اذا تحتاج تنزيل وتنصيب برنامج السكراتش Scratch على جهازك الشخصي، ستجده في [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

في بداية المشروع ، من المفترض أن ترى خلفية الهدف مع علامة التصويب (+).

![مشاريع البداية](images/archery-starter.png)

--- /task ---

--- task ---

عندما تبدأ اللعبة ، قم بارسال رسالة لتصويب سهم جديد.

![كائن الهدف](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (سهم جديد v)
```

--- /task ---

--- task ---

بمجرد استلام هذه الرسالة ، قم بتحديد موقع السهم وحجمه.

![كائن الهدف](images/target-sprite.png)

```blocks3
when I receive [سهم جديد v]
go to x: (-150) y: (-150)
set size to (400) %
```

--- /task ---

--- task ---

انقر على العلم الأخضر لاختبار لعبتك. يجب أن ترى سهمك يكبر ويتحرك إلى أسفل يسار المنصة.

![أكبر كائن الهدف في أسفل يسار المنصة](images/archery-start-test.png)

--- /task ---

--- task ---

أضف تعليمات برمجية إلى سهمك بحيث يكون `ينساب`{:class="block3motion"} عشوائيًا حول المنصة `إلى الأبد`{:class="block3control"}.

![كائن الهدف](images/target-sprite.png)

```blocks3
when I receive [سهم جديد v]
go to x: (-150) y: (-150)
set size to (400) %
+forever
glide (0.5) secs to x: (pick random (-150) to (150)) y: (pick random (-150) to (150))
end
```

--- /task ---

--- task ---

اختبر لعبتك مرة أخرى ، ويجب أن ترى سهمك يتحرك بشكل عشوائي حول المنصة .

![الهدف في موقع مختلف](images/archery-glide-test.png)

--- /task ---
