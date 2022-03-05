---
layout: default
title: <font color="#2c84fa">❒</font> playerLeavePartyCallback
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

## playerLeavePartyCallback
유닛이 파티에서 나갈 때 호출되는 콜백 함수입니다. 

#### 콜백 함수의 형식
```lua
function( player, party)
반환값: 없음
[1] player: 파티에서 나갈 유닛
[2] party: 나갈 파티
```

#### 선언
```cs
public Closure playerLeavePartyCallback { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### 예제: 파티를 나갈 때 발생하는 이벤트

```lua
Server.playerLeavePartyCallback = function(scriptRoomPlayer,scriptParty)
    print(scriptRoomPlayer.unit.name)
    print(scriptParty.maxPlayer)
end
```