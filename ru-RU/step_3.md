## Стрельба стрелами

Давай сделаем код для твоей стрелы, чтобы можно было стрелять при нажатии пробела.

--- task ---

Останови другой скрипт (тот, который перемещает стрелу), когда нажимается пробел.

![спрайт мишень](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

--- /task ---

--- task ---

Запусти свой проект для проверки ещё раз. На этот раз твоя стрела должна перестать двигаться **при нажатии клавиши пробел**.

--- /task ---

--- task ---

Анимируй свою стрелу, чтобы она выглядела так, как будто она движется к мишени.

![спрайт мишень](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

--- /task ---

--- task ---

Проверь свою игру снова. На этот раз, когда ты нажимаешь клавишу пробел, ты должен увидеть, как стрела становится меньше, как будто она движется к мишени.

![мишень с перекрестием на нем](images/archery-animate-test.png)

--- /task ---

--- task ---

Как только твоя стрела окажется в мишени, ты сможешь сказать игроку, сколько очков он набрал. Например, он мог набрать 200 очков за попадание в жёлтый цвет.

![спрайт мишень](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
+if <0> then
say [200 очков] for (2) seconds
end
```

--- /task ---

--- task ---

Ты также можешь воспроизвести звук, если он попал в желтый цвет.

![спрайт мишень](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <0> then
+start sound (cheer v)
say [200 очков] for (2) seconds
end
```

--- /task ---

--- task ---

Наконец, тебе нужно снова передать сообщение `новая стрела`{:class="block3events"}, чтобы получить новую стрелу.

![спрайт мишень](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <0> then
start sound (cheer v)
say [200 очков] for (2) seconds
end
+broadcast (новая стрела v)
```

--- /task ---