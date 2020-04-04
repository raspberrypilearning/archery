## Наведение стрел

Давай начнём с создания стрелы, которая перемещается по экрану.

\--- task \---

Открой стартовый проект Scratch.

**Онлайн**: открой стартовый проект по адресу [rpf.io/archeryon](http://rpf.io/archeryon){:target="_blank"}.

Если у тебя есть учётная запись в Scratch, то ты можешь сделать копию проекта, нажав **Ремикс**.

**Оффлайн**: открой [стартовый проект](http://rpf.io/p/en/archery-go){:target="_blank"} в оффлайн редакторе.

Если тебе нужно скачать и установить оффлайн редактор Scratch, ты можешь найти его по адресу [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

В стартовом проекте ты должен увидеть фон в виде мишени и спрайт с перекрестием.

![starter projects](images/archery-starter.png)

\--- /task \---

\--- task \---

Когда твоя игра начнётся, отправь сообщение, чтобы выстрелить новой стрелой.

![target sprite](images/target-sprite.png)

```blocks3
когда щёлкнут по зелёному флагу
передать (новая стрела v)
```

\--- /task \---

\--- task \---

Как только это сообщение будет получено, задай позицию и размер стрелы.

![target sprite](images/target-sprite.png)

```blocks3
когда я получу [новая стрела v]
перейти в x: (-150) y: (-150)
установить размер (400) %
```

\--- /task \---

\--- task \---

Нажми на зелёный флаг, чтобы проверить свою игру. Ты должен увидеть, как твоя стрела стала больше и переместилась в нижний левый угол сцены.

![larger target sprite in bottom left of stage](images/archery-start-test.png)

\--- /task \---

\--- task \---

Add code to your arrow so that it `glides`{:class="block3motion"} randomly around the stage `forever`{:class="block3control"}.

![target sprite](images/target-sprite.png)

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

Test your game again, and you should see your arrow move randomly around the stage.

![target in a different position](images/archery-glide-test.png)

\--- /task \---