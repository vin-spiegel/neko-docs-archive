---
layout: default
title: <font color="#2c84fa">❒</font> onUnitLevelUp
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

## onUnitLevelUp
유닛이 레벨 업 했을 때 호출되는 이벤트입니다. 

#### 호출 될 함수의 인자 형식
```lua
function( unit)
[1] unit: 레벨 업 한 유닛
```

#### 선언
```cs
public ScriptEventPublisher onUnitLevelUp { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 플레이어가 특정 레벨에 도달했을 때 보상 지급
```lua
function onUnitLevelUp(target, level)
    -- 타겟이 50레벨을 달성했으면 서버 전체에 알림을 띄우고 1번 아이템을 지급한다.
    if target.level == 50 then
        Server.SendCenterLabel(target.name .. '님이 ' .. level .. '이 되었습니다!')
        target.AddItem(1)
    -- 55레벨을 달성했으면 5번스킬과 5000게임머니를 지급한다. 
    elseif target.level == 55 then
        target.AddSkill(5)
        target.AddGameMoney(5000)
    end
end
 
Server.onUnitLevelUp.Add(onUnitLevelUp)
```