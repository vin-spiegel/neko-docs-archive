---
layout: default
title: <font color="#2c84fa">❒</font> createClan
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

# createClan
클랜이 생성되었을 때의 콜백 함수입니다. 

## 콜백 함수의 형식

```lua
function(player, name, joinType)
```

|이름|타입|설명|
|:-|:-|:-|
|player|ScriptRoomPlayer|클랜을 만든 플레이어|
|name|string|클랜의 이름|
|joinType|number|클랜의 가입 형식 0: 즉시 가입, 1: 가입 요청, 2: 비공개|

## 반환값

|타입|설명|
|:-|:-|
|boolean|클랜 생성이 성공했는지 (`true`: 클랜 생성 성공, `false`: 클랜 생성 실패)|

## 선언
```cs
public Closure createClan { get; set; }
```

## 프로퍼티 값

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

## 예제 1
`boolean` 값 반환을 이용한 클랜 생성 성공/실패 여부 결정
```lua
function createClan(player, clanName, joinType)
    local noticeText = player.name ' 님이 ' .. clanName .. '클랜을 창설했습니다!'
    Server.SendCenterLabel(noticeText)
    
    -- False 반환시 클랜 생성을 막는다
    return true
end

Server.createClan = createClan
```

## 예제 2
문자열 반환을 이용한 클랜 생성 실패 여부 보내주기
```lua
function createClan(player, clanName, joinType)
    local noticeText = player.name ' 님이 ' .. clanName .. '클랜을 창설했습니다!'
    Server.SendCenterLabel(noticeText)
    
    -- 아래와 같이 문자열을 반환하게 되면 클라이언트에 메시지 박스가 표시된다.
    return "Error: 클랜 생성에 실패했습니다"
end
Server.createClan = createClan
```