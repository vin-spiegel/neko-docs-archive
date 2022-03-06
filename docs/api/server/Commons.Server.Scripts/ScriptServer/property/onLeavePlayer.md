---
layout: default
title: <font color="#2c84fa">❒</font> onLeavePlayer
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

# onLeavePlayer
플레이어가 게임을 나갔을 때 호출되는 이벤트입니다. 

## 호출될 함수의 인자 형식
```lua
function( player)
[1] player: 나간 플레이어
```

## 선언
```cs
public ScriptEventPublisher onLeavePlayer { get; }
```

## 프로퍼티 값

|타입|설명|
|ScriptEventPublisher|

## 예제: 플레이어가 나갔을 때 서버 전체에게 해당 유저가 나갔음을 알리기
```lua
-- Tip: 단 해당 함수는 네트워크 불안정 등의 요소를 고려해, 유저와의 연결이 끊긴 후 180초(3분) 뒤에 호출됩니다

function onLeavePlayer(player)
    Server.SendCenterLabel(player.name .. "님이 나갔습니다")
end

Server.onLeavePlayer.Add(onLeavePlayer)
```
