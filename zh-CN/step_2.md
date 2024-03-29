## 瞄准箭头

让我们从创建一个在屏幕上移动的准心开始。

--- task ---

打开 Scratch 初始项目。

**在线版本：** 从 [scratch.mit.edu/projects/382479386](https://scratch.mit.edu/projects/382479386){:target="_blank"} 打开初始项目。

如果您有一个 Scratch 帐户，您可以通过点击 **改编** 复制该项目。

**离线版本**: 在离线编辑器中打开 [初始项目](https://rpf.io/p/zh-CN/archery-go){:target="_blank"}.

如果您需要下载并安装 Scratch 离线编辑器，可以点击链接 [ rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"} 获取 。

在初始项目中，您应该看到预设好的背景和十字准心精灵。

![初始项目](images/archery-starter.png)

--- /task ---

--- task ---

游戏开始时，广播一条消息用于发射新箭头。

![箭头精灵](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (新箭头 v)
```

--- /task ---

--- task ---

接收到此消息后，设置准心的位置和大小。

![箭头精灵](images/target-sprite.png)

```blocks3
when I receive [新箭头 v]
go to x: (-150) y: (-150)
set size to (400) %
```

--- /task ---

--- task ---

单击绿色小旗标志来测试您的游戏。 您应该看到准心变大并移到舞台的左下角。

![舞台左下方的较大的箭头精灵](images/archery-start-test.png)

--- /task ---

--- task ---

将代码添加到您的箭头精灵，使其 `重复执行`{:class ="block3motion"} `滑行`{:class="block3control"} 到随机位置。

![箭头精灵](images/target-sprite.png)

```blocks3
when I receive [新箭头 v]
go to x: (-150) y: (-150)
set size to (400) %
+forever
glide (0.5) secs to x: (pick random (-150) to (150)) y: (pick random (-150) to (150))
end
```

--- /task ---

--- task ---

再次测试您的游戏，您应该能看到准心在舞台上随机移动。

![射中不同的位置](images/archery-glide-test.png)

--- /task ---
