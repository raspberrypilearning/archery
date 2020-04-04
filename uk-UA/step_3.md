## Стрільба

Давай напишемо код для стріли, щоб стріляти, коли натиснуто клавішу пропуск.

--- task ---

Зупини інший скрипт (той, що рухає стрілою), коли натиснуто клавішу пропуск.

![спрайт приціла](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

--- /task ---

--- task ---

Перевір свій проєкт знову. Цього разу стріла повинна перестати рухатись **коли клавішу пропуск натиснуто**.

--- /task ---

--- task ---

Анімуй стрілу, щоб вона виглядала так, ніби рухається до цілі.

![спрайт приціла](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

--- /task ---

--- task ---

Перевір свою гру ще раз. Цього разу, натискаючи клавішу пропуск, ти побачиш, як стріла зменшується, ніби рухається до цілі.

![мішень з прицілом на ній](images/archery-animate-test.png)

--- /task ---

--- task ---

Як тільки стріла досягне цілі, ти можеш повідомити гравцеві, скільки балів той набрав. Наприклад, він може набрати 200 балів за попадання в жовтий колір.

![спрайт приціла](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
+if <touching color (#ffff00) ?> then
say [200 балів] for (2) seconds
end
```

--- /task ---

--- task ---

Також ти можеш програвати звук, якщо він потрапляє в жовтий колір.

![спрайт приціла](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <touching color (#ffff00) ?> then
+start sound (cheer v)
say [200 балів] for (2) seconds
end
```

--- /task ---

--- task ---

Нарешті, тобі потрібно оповістити повідомленням `нова стріла`{:class="block3events"}, щоб отримати нову стрілу.

![спрайт приціла](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <touching color (#ffff00) ?> then
start sound (cheer v)
say [200 балів] for (2) seconds
end
+broadcast (нова стріла v)
```

--- /task ---