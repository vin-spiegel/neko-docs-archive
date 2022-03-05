---
layout: default
title: <font color="#2c84fa">❒ </font>onTick
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->



#### onTick
매 프레임마다 호출되는 이벤트입니다. 호출될 함수의 인자 형식: function( dt)
[1] dt: Delta time

#### 선언
```cs
public ScriptEventPublisher onTick { get; }
```

#### 프로퍼티 값

|타입|설명|
|ScriptEventPublisher|

#### 예제: 매 프레임마다 채팅창에 "Tick! ([횟수])" 표시하기
```lua
-- Tip: onTick 이벤트는 호출 횟수가 많은 이벤트입니다
-- 이벤트 사용 횟수가 많아지거나, 내부 로직이 실행되는데 시간이 오래 걸린다면
-- 서버에 부하가 갈 수 있으므로 최적화를 한 후 사용해야 합니다.

count = 0
function onTick(deltaTime)
    Server.SendSay("Tick! (" .. count .. ")")
    count = count + 1
end

Server.onTick.Add(onTick)
```