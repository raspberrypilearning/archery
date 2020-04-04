## Atirando as flechas

Vamos codificar sua mira para atirar quando a barra de espaço for pressionada.

\--- task \---

Pare o outro script (aquele que move a seta) quando a barra de espaço é pressionada.

![ator mira](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Teste o seu projeto novamente. Desta vez, sua mira deve parar de se mover **quando a barra de espaço for pressionada**.

\--- /task \---

\--- task \---

Anime sua mira para que pareça estar se movendo em direção ao alvo.

![ator mira](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

Teste seu jogo novamente. Desta vez, quando você pressiona a barra de espaço, sua mira ficará menor, como se estivesse se movendo em direção ao alvo.

![alvo com a mira nele](images/archery-animate-test.png)

\--- /task \---

\--- task \---

Quando sua mira estiver no alvo, você pode dizer ao jogador quantos pontos ele marcou. Por exemplo, eles poderiam marcar 200 pontos por acertar no amarelo.

![ator mira](images/target-sprite.png)

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

Você também pode tocar um som se eles acertarem no amarelo.

![ator mira](images/target-sprite.png)

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

Por fim, você precisa transmitir novamente a mensagem `nova flecha`{:class="block3events"} para obter uma nova flecha.

![ator mira](images/target-sprite.png)

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