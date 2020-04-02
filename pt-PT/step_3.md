## Atirar flechas

Vamos acrescentar código à tua flecha de forma a que seja disparada quando a barra de espaço for pressionada.

\--- task \---

Pára o outro código (aquele que move a flecha) quando a barra de espaço é pressionada.

![ator alvo](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

\--- /task \---

\--- task \---

Testa o teu projeto novamente. Desta vez, a tua flecha deve parar de se mover **quando a barra de espaço for pressionada**.

\--- /task \---

\--- task \---

Anima a tua flecha para que pareça que está a mover-se em direção ao alvo.

![ator alvo](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

\--- /task \---

\--- task \---

Testa o teu jogo novamente. Desta vez, quando pressionares a barra de espaço, a tua flecha vai ficar mais pequena, como se estivesse a mover-se em direção ao alvo.

![alvo com a mira em cima](images/archery-animate-test.png)

\--- /task \---

\--- task \---

Quando a tua flecha estiver no alvo, pode dizer quantos pontos fez. Por exemplo, pode-se fazer 200 pontos por acertar no amarelo.

![ator alvo](images/target-sprite.png)

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

Também podes fazer com que toque um som se acertarem no amarelo.

![ator alvo](images/target-sprite.png)

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

Finalmente, tens que transmitir novamente a mensagem `nova flecha`{: class = "block3events"} para obter uma nova flecha.

![ator alvo](images/target-sprite.png)

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