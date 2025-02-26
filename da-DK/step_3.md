## Skyde pile

Lad os kode dine pile til at skyde, når mellemrumstasten er trykket.

--- task ---

Stop det andet skript (den som bevæger pilen), når mellemrumstasten er trykket.

![Sigtekorn sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

--- /task ---

--- task ---

Test dit projekt igen. Denne gang bør din pil stoppe med at bevæge sig __når mellemrumstasten er trykket__.

--- /task ---

--- task ---

Animer din pil, så det ser ud som om at den flyver mod målskiven.

![Sigtekorn sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

--- /task ---

--- task ---

Test dit spil igen. Denne gang, når du trykker mellemrumstasten, burde du se pilen blive mindre, som om at den flyver mod målskiven.

![Målskive med sigtekorn over den](images/archery-animate-test.png)

--- /task ---

--- task ---

Når din pil har ramt målskiven, kan du vise, hvor mange point spilleren har skoret. Som et eksempel kan spilleren skore 200 point for at ramme det gule på målskiven.

![Sigtekorn sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
+if <touching color (#ffff00) ?> then
say [200 point] for (2) seconds
end
```

--- /task ---

--- task ---

Du kan også afspille en lyd, hvis spilleren rammer det gule.

![Sigtekorn sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <touching color (#ffff00) ?> then
+start sound (cheer v)
say [200 point] for (2) seconds
end
```

--- /task ---

--- task ---

Endelig skal du sende `ny pil`{:class="block3events"}-beskeden igen for at få en ny pil.

![Sigtekorn sprite](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <touching color (#ffff00) ?> then
start sound (cheer v)
say [200 point] for (2) seconds
end
+broadcast (ny pil v)
```

--- /task ---
