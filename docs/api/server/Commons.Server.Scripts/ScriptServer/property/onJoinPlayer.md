---
layout: default
title: <font color="#2c84fa">❒</font> onJoinPlayer
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

# onJoinPlayer
게임에 플레이어가 들어왔을 때 호출되는 이벤트입니다. 

## 호출될 함수의 인자 형식
```lua
function( player)
```

[1] player: 접속한 플레이어

## 선언
```cs
public ScriptEventPublisher onJoinPlayer { get; }
```

## 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

## 예제
플레이어가 접속했을 때 그 유저에게 "Hello [유저이름]!" 출력하기
```lua
function onJoinPlayer(player)
    player.unit.SendCenterLabel("Hello " .. player.name .. "!")
end

Server.onJoinPlayer.Add(onJoinPlayer)
```