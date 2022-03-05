---
layout: default
title: <font color="#2c84fa">❒</font> onBuyGameMoneyItem
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->

## onBuyGameMoneyItem
유닛이 골드(게임 머니)로 아이템을 샀을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function(unit, itemID, count)
```

|이름|타입|설명|
|:-|:-|:-|
|unit|ScriptUnit|아이템을 산 유닛|
|itemID|number|산 아이템의 ID|
|count|number|산 아이템의 개수|

#### 선언
```cs
public ScriptEventPublisher onBuyGameMoneyItem { get; }
```

#### 프로퍼티 값
|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 플레이어가 아이템을 샀을 때 유닛의 이름, 아이템 ID, 갯수 출력하기
```lua
function onBuyGameMoneyItem(unit, itemID, count)
    print(string.format("%s, %s, %s", unit.name, itemID, count))
end

Server.onBuyGameMoneyItem.Add(onBuyGameMoneyItem)
```