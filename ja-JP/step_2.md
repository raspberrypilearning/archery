## ねらいをつける

まず、画面内を動く矢を作ります。

--- task ---

基本の Scratch プロジェクトを開きます。

**オンライン**: [scratch.mit.edu/projects/382678788](https://scratch.mit.edu/projects/382678788){:target="_blank"}から基本のプロジェクトを開きます。

Scratch アカウントを持っている場合、 **リミックス**ボタンをクリックしてプロジェクトをコピーできます。

**オフライン**: オフラインエディターで[基本のプロジェクト](https://rpf.io/p/ja-JP/archery-go){:target="_blank"}を開きます。

[rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}からScratch オフラインエディターのダウンロードしてインストールできます。

基本のプロジェクトには、まとの背景 (はいけい) と十字のスプライトがあります。

![基本のプロジェクト](images/archery-starter.png)

--- /task ---

--- task ---

ゲームが始まったら、新しい矢をはなつためにメッセージを送ります。

![矢のスプライト](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (新しい矢 v)
```

--- /task ---

--- task ---

このメッセージを受け取ったら、矢の位置 (いち) と大きさを決めます。

![矢のスプライト](images/target-sprite.png)

```blocks3
when I receive [新しい矢 v]
go to x: (-150) y: (-150)
set size to (400) %
```

--- /task ---

--- task ---

緑の旗をクリックしてゲームをテストします。 矢が大きくなり、ステージの左下に動くはずです。

![ステージの左下にある大きな矢のスプライト](images/archery-start-test.png)

--- /task ---

--- task ---

矢にコードを入れて、 矢が`ずっと`{:class="block3control"}ランダムに、ステージ上の位置を`変える`{:class="block3motion"}ようにします。

![矢のスプライト](images/target-sprite.png)

```blocks3
when I receive [新しい矢 v]
go to x: (-150) y: (-150)
set size to (400) %
+forever
glide (0.5) secs to x: (pick random (-150) to (150)) y: (pick random (-150) to (150))
end
```

--- /task ---

--- task ---

もう一度ゲームをテストすると、矢がステージ上でランダムに動くのがわかります。

![別の位置にある矢](images/archery-glide-test.png)

--- /task ---
