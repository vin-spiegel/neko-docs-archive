---
layout: default
title: <font color="#2c84fa">❒ </font>onUseItem
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

## onUseItem
유닛이 아이템을 사용했을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function( unit, item)
[1] unit: 아이템을 사용한 유닛
[2] item: 사용한 아이템
```

#### 선언
```cs
public ScriptEventPublisher onUseItem { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 아이템 사용 시 아이템을 사용한 유저의 이름과 아이템 번호 출력하기
```lua
function onUseItem(unit, item)
    unit.SendCenterLabel(unit.name .. ": " .. item.dataID)
end

Server.onUseItem.Add(onUseItem)
```