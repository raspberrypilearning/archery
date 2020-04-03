## 矢をはなつ

スペースバーがおされたときに、矢がはなたれるようにコードを入れましょう。

\--- task \---

スペースバーがおされたとき、他のスクリプト（矢を動かすスクリプト）を止めます。

![矢のスプライト](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

もう一度テストしてみましょう。 今度は、**スペースバーがおされたとき**、矢の動きが止まるはずです。

\--- /task \---

\--- task \---

矢をアニメーションして、まとに向かって動いているように見せます。

![矢のスプライト](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

もう一度ゲームをテストします。 今度は、スペースバーをおすと矢が小さくなっていき、まとに向かって動いているように見えるはずです。

![的の上に十字](images/archery-animate-test.png)

\--- /task \---

\--- task \---

矢がまとにあたると、取った点数をプレイヤーに教えることができます。 たとえば、黄色にあてると200点をとることができます。

![矢のスプライト](images/target-sprite.png)

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

黄色にあてると音を出すこともできます。

![矢のスプライト](images/target-sprite.png)

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

さいごに、新しい矢を取得 (しゅとく) するには、また`新しい矢`{:class="block3events"}メッセージを送る必要があります。

![矢のスプライト](images/target-sprite.png)

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