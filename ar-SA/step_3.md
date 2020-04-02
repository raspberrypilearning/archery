## سهام الرماية

دعنا نبرمج سهمك للتصويب عند الضغط على مفتاح المسافة.

\--- task \---

أوقف الجزء البرمجي الآخر (الذي يحرك السهم) عند الضغط على مفتاح المسافة.

![كائن الهدف](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

اختبر مشروعك مرة أخرى. هذه المرة ، يجب أن يتوقف سهمك عن التحرك **عند الضغط على مفتاح المسافة**.

\--- /task \---

\--- task \---

قم بتحريك سهمك ، بحيث يبدو أنه يتحرك نحو الهدف.

![كائن الهدف](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

اختبر لعبتك مرة أخرى. هذه المرة ، عندما تضغط على مفتاح (زر) المسافة ، يجب أن ترى سهمك أصغر ، كما لو كان يتحرك نحو الهدف.

![الهدف مع علامة التصويب عليه](images/archery-animate-test.png)

\--- /task \---

\--- task \---

بمجرد أن يكون سهمك في الهدف ، يمكنك إخبار اللاعب بعدد النقاط التي سجلها. على سبيل المثال ، يمكنهم تسجيل 200 نقطة لتصويب اللون الأصفر.

![كائن الهدف](images/target-sprite.png)

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

يمكنك أيضًا تشغيل صوت إذا صدم اللون الأصفر.

![كائن الهدف](images/target-sprite.png)

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

أخيرًا ، يلزمك ارسال رسالة `سهم جديد`{: class = "block3events"} مرة أخرى للحصول على سهم جديد.

![كائن الهدف](images/target-sprite.png)

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