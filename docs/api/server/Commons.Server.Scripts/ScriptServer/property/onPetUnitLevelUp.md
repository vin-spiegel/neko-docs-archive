---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">❒ </font>onPetUnitLevelUp</div>
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

# onPetUnitLevelUp
펫 유닛이 레벨 업 했을 때 호출되는 이벤트입니다. 

## 호출될 함수의 인자 형식
```lua
function( unit, level)
[1] unit: 레벨 업한 펫 유닛
[2] level: 펫 레벨
```

## 선언
```cs
public ScriptEventPublisher onPetUnitLevelUp { get; }
```

## 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

## 예제 
펫 레벨업시 메세지 출력
```lua
function onPetUnitLevelUp(pet, level)
    Server.SendCenterLabel("펫 " .. pet.name .. "이(가) " .. level .. "레벨이 되었습니다")
end

Server.onPetUnitLevelUp.Add(onPetUnitLevelUp)
```
