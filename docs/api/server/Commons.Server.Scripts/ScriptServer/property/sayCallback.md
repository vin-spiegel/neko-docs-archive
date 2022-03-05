---
layout: default
title: <font color="#2c84fa">❒</font> sayCallback
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->



## sayCallback
플레이어가 말했을 때의 콜백 함수입니다. 

#### 콜백 함수의 형식
```lua
function( player, text)
반환값: 플레이어가 말한 내용이 적용 되는지 (True: 대사 적용, False: 대사 무시)
[1] player: 말한 플레이어
[2] text: 플레이어가 말한 대사
```

#### 선언
```cs
public Closure sayCallback { get; set; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|MoonSharp.Interpreter.Closure|

#### 예제 1: 금지어 필터링 예제
```lua
function badwordFillter(player, text)
    if string.contains(text, "금지어") then
        player.unit.SendCenterLabel("금지어는 사용하실 수 없습니다.")
        return false
    else
        return true    
    end
end

Server.sayCallback = badwordFillter
```
#### 예제 2: "#hi" 라고 입력하면 서버의 모든 유저들에게 인삿말 표시
```lua
function customCommand(player, text)
    if text == "#hi" then
        Server.SendCenterLabel(player.name .. ": 안녕!")
        return false
    end

    return true
end

Server.sayCallback = customCommand
```
