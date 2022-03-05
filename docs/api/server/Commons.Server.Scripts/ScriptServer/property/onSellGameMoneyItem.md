---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">❒ </font>onSellGameMoneyItem</div>
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 0
---

<!-- 아래로 편집 -->




## onSellGameMoneyItem
유닛이 골드(게임 머니) 아이템을 팔았을 때 호출되는 이벤트입니다. 

#### 호출될 함수의 인자 형식
```lua
function( unit, itemID, count)
[1] unit: 아이템을 판 유닛
[2] itemID: 판 아이템의 ID
[3] count: 판 아이템의 개수
```

#### 선언
```cs
public ScriptEventPublisher onSellGameMoneyItem { get; }
```

#### 프로퍼티 값

|타입|설명|
|:-|:-|
|ScriptEventPublisher|

#### 예제: 플레이어가 아이템을 팔았을 때 유닛의 이름, 아이템 ID, 갯수 출력하기
```lua
function onSellGameMoneyItem(unit, itemID, count)
    print(string.format("%s, %s, %s", unit.name, itemID, count))
end

Server.onSellGameMoneyItem.Add(onSellGameMoneyItem)
```