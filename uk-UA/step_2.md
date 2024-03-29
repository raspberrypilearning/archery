## Прицілювання

Почнемо зі створення стріли, яка рухається по екрану.

--- task ---

Відкрий початковий проєкт на Скретч.

**Онлайн**: відкрий початковий проєкт на [scratch.mit.edu/projects/382750315](https://scratch.mit.edu/projects/382750315){:target="_blank"}.

Якщо у тебе є обліковий запис Скретч, то ти можеш зробити копію проєкту, натиснувши **Ремікс**.

**Офлайн**: відкрий [початковий проєкт](https://rpf.io/p/uk-UA/archery-go){:target="_blank"} в офлайн-редакторі.

Якщо тобі треба завантажити та встановити офлайн-редактор Скретч, то ти можеш його знайти на [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

У початковому проєкті ти маєш бачити тло із мішенню та спрайт для приціла.

![початкові проєкти](images/archery-starter.png)

--- /task ---

--- task ---

Коли твоя гра починається, оповісти повідомленням, що нова стріла випущена.

![спрайт приціла](images/target-sprite.png)

```blocks3
when green flag clicked
broadcast (нова стріла v)
```

--- /task ---

--- task ---

Після отримання цього повідомлення задай положення та розмір стріли.

![спрайт приціла](images/target-sprite.png)

```blocks3
when I receive [нова стріла v]
go to x: (-150) y: (-150)
set size to (400) %
```

--- /task ---

--- task ---

Натисни на зелений прапор, щоб перевірити свою гру. Ти маєш побачити, як стріла збільшилася, і перемістилася в нижню ліву частину сцени.

![більший спрайт приціла у лівій нижній частині сцени](images/archery-start-test.png)

--- /task ---

--- task ---

Додай код до стріли, щоб вона навмання `ковзала`{:class="block3motion"} по сцені `завжди`{:class="block3control"}.

![спрайт приціла](images/target-sprite.png)

```blocks3
when I receive [нова стріла v]
go to x: (-150) y: (-150)
set size to (400) %
+forever
glide (0.5) secs to x: (pick random (-150) to (150)) y: (pick random (-150) to (150))
end
```

--- /task ---

--- task ---

Перевір свою гру ще раз, і ти маєш побачити, як стріла рухається випадковим чином по сцені.

![приціл в іншій позиції](images/archery-glide-test.png)

--- /task ---
