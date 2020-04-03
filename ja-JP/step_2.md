## ねらいをつける

まず、画面内を動く矢を作ります。

\--- task \---

基本の Scratch プロジェクトを開きます。

**オンライン**: [rpf.io/archeryon](http://rpf.io/archeryon){:target="_blank"}から基本のプロジェクトを開きます。

Scratch アカウントを持っている場合、 **リミックス**ボタンをクリックしてプロジェクトをコピーできます。

**オフライン**: オフラインエディターで[基本のプロジェクト](http://rpf.io/p/en/archery-go){:target="_blank"}を開きます。

[rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}からScratch オフラインエディターのダウンロードしてインストールできます。

基本のプロジェクトには、まとの背景 (はいけい) と十字のスプライトがあります。

![基本のプロジェクト](images/archery-starter.png)

\--- /task \---

\--- task \---

ゲームが始まったら、新しい矢をはなつためにメッセージを送ります。

![矢のスプライト](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (new arrow v)
```

\--- /task \---

\--- task \---

このメッセージを受け取ったら、矢の位置 (いち) と大きさを決めます。

![矢のスプライト](images/target-sprite.png)

```blocks3
when I receive [new arrow v]
go to x: (-150) y: (-150)
set size to (400) %
```

\--- /task \---

\--- task \---

緑の旗をクリックしてゲームをテストします。 矢が大きくなり、ステージの左下に動くはずです。

![ステージの左下にある大きな矢のスプライト](images/archery-start-test.png)

\--- /task \---

\--- task \---

矢にコードを入れて、 矢が`ずっと`{:class="block3control"}ランダムに、ステージ上の位置を`変える`{:class="block3motion"}ようにします。

![矢のスプライト](images/target-sprite.png)

```blocks3
[新しい矢印v]を受け取ったら
移動x：（-150）y：（-150）
サイズを（400）％
+永久に
グライド（0.5）秒x：（ランダムに選択（-150）から（150））y：（ランダムに選択（-150）から（150））
終了
```

\--- /task \---

\--- task \---

もう一度ゲームをテストすると、矢がステージ上でランダムに動くのがわかります。

![別の位置にある矢](images/archery-glide-test.png)

\--- /task \---