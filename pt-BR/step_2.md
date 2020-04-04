## Mirando as flechas

Vamos começar criando uma mira que se move pela tela.

\--- task \---

Abra o projeto inicial do Scratch.

**Online**: abra o projeto inicial em [rpf.io/archeryon](http://rpf.io/archeryon){:target="_blank"}.

Se você tiver uma conta do Scratch, pode fazer uma cópia clicando em **Remix**.

**Offline**: abra o [projeto inicial](http://rpf.io/p/en/archery-go){:target="_ blank"} no editor offline.

Se você precisar baixar e instalar o editor offline do Scratch, você pode encontrá-lo em [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

No projeto inicial, você verá um cenário de alvo e um ator de mira.

![projetos iniciais](images/archery-starter.png)

\--- /task \---

\--- task \---

Quando o jogo começar, transmita uma mensagem para disparar uma nova flecha.

![ator mira](images/target-sprite.png)

```blocks3
quando bandeira verde for clicado
transmita(new flecha v)
```

\--- /task \---

\--- task \---

Depois que essa mensagem for recebida, defina a posição e o tamanho da seta.

![ator mira](images/target-sprite.png)

```blocks3
quando eu receber [nova flecha v]
vá para x: (-150) y: (-150)
defina o tamanho como (400) %
```

\--- /task \---

\--- task \---

Clique na bandeira verde para testar seu jogo. Você deve ver se sua mira irá aumentar e se mover para o canto inferior esquerdo do palco.

![ator mira maior no canto inferior esquerdo do palco](images/archery-start-test.png)

\--- /task \---

\--- task \---

Adicione código para que sua mira `deslize`{: class = "block3motion"} aleatoriamente pelo palco `para sempre`{: class = "block3control"}.

![ator mira](images/target-sprite.png)

```blocks3
quando eu receber [nova flecha v]
vá para x: (-150) y: (-150)
defina o tamanho para (400)%
+sempre
deslize por (0,5) segs. até x: (número aleatório entre (-150) e(150)) y: (número aleatório entre (-150) e (150))
fim
```

\--- /task \---

\--- task \---

Teste seu jogo novamente e você verá sua mira se movendo aleatoriamente pelo palco.

![mira em uma posição diferente](images/archery-glide-test.png)

\--- /task \---