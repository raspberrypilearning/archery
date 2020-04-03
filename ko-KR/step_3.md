## 화살 발사

스페이스 바를 눌렀을 때 화살을 쏘도록 코드를 짜 봅시다.

--- task ---

스페이스 바를 누르면 다른 스크립트(화살표 이동) 를 중지합니다.

![타겟 스프라이트](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
```

--- /task ---

--- task ---

프로젝트를 다시 테스트해 보세요. 이번에는 **스페이스 키가 눌렸을 때** 화살의 움직임이 멈춰야 합니다.

--- /task ---

--- task ---

화살이 타겟을 향해 움직이는 것처럼 보이도록 애니메이션을 적용하십시오.

![타겟 스프라이트](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
+repeat (50)
change size by (-10)
end
```

--- /task ---

--- task ---

게임을 다시 테스트 해 보세요. 이번에는 스페이스 바가 누렸을 때 화살이 목표를 향해 움직이며 작아지는 것이 보여야 합니다.

![조준점이 겨냥된 타겟](images/archery-animate-test.png)

--- /task ---

--- task ---

화살이 타겟에 성공적으로 명중하면, 당신은 플레이어가 얻은 점수를 말해줄 수 있습니다. 예를 들어 노란색을 명중했다면 200 점을 득점 할 수 있습니다.

![타겟 스프라이트](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
+if <touching color (#ffff00) ?> then
say [200 포인트] for (2) seconds
end
```

--- /task ---

--- task ---

노란색에 명중했을 경우 소리를 재생할 수도 있습니다.

![타겟 스프라이트](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <touching color (#ffff00) ?> then
+start sound (cheer v)
say [200 포인트] for (2) seconds
end
```

--- /task ---

--- task ---

마지막으로 새 화살을 얻기 위해서는, `새 화살`{:class="block3events"} 신호를 보내야 합니다.

![타겟 스프라이트](images/target-sprite.png)

```blocks3
when [space v] key pressed
stop [other scripts in sprite v]
repeat (50)
change size by (-10)
end
if <touching color (#ffff00) ?> then
start sound (cheer v)
say [200 포인트] for (2) seconds
end
+broadcast (새로운 화살 v)
```

--- /task ---