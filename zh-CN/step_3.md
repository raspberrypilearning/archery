## 发射箭头

我们来给箭头精灵加上一些代码，以便在按下空格键时发射。

\--- task \---

按下空格键时，停止另一个脚本(移动准心的脚本)。

![箭头精灵](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

再次测试你的程序。 这回当按下 **空格键** 时准心应该停止移动。

\--- /task \---

\--- task \---

给准心加一些动画，让它看起来像是在不断朝靶子移动。

![箭头精灵](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

再次测试您的游戏。 这下当您按下空格键时，您应该看到准心不断变小，好像它正在朝靶子移动。

![用十字准心瞄准](images/archery-animate-test.png)

\--- /task \---

\--- task \---

一旦箭头射中了目标，您就可以告诉玩家他们得分了多少分。 举个例子，如果射中了黄色靶心可以得到200分。

![箭头精灵](images/target-sprite.png)

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

当射中黄色靶心，也可以来点音效。

![箭头精灵](images/target-sprite.png)

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

最后，您需要再次广播 `新箭头`{:class ="block3events"} 消息来得到一个新箭头。

![箭头精灵](images/target-sprite.png)

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