---
layout: default
title: <font color="#2c84fa">❒</font>playerJoinPartyCallback
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

## playerJoinPartyCallback
유닛이 파티에 참가할 때 호출되는 콜백 함수입니다. 

#### 콜백 함수의 형식
```lua
function( player, party)
반환값: 유닛이 파티에 참가되었는가 (True: 참가, False: 참가하지 못함)
[1] player: 참가할 유닛
[2] party: 참가할 파티
```

#### 선언
```cs
public Closure playerJoinPartyCallback { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### 예제: 파티 입장 때 발생하는 이벤트
```lua
Server.playerJoinPartyCallback = function(scriptRoomPlayer,scriptParty)
    print(scriptRoomPlayer.unit.name)
    print(scriptParty.maxPlayer)

    -- true 를 반환 시, 파티에 입장됩니다
    -- 조건에 따라서 true/false를 이용해 파티 입장을 막을 수 있습니다
    return true
end
```