---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>IsEquippedItemByDataID</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## IsEquippedItemByDataID(Int32)
유닛이 해당 아이템을 장착 중인지 알아냅니다.

#### 선언
```cs
public bool IsEquippedItemByDataID(int itemDataID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|itemDataID|데이터 베이스의 아이템 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|장착 여부 (장착 중일시: True, 아닐 시: False)|

#### 예제: 5번 아이템을 장착했는지 출력하기
```lua
if unit.IsEquippedItemByDataID(5) then
    unit.SendCenterLabel("5번 아이템 장착 중")
else
    unit.SendCenterLabel("5번 아이템 장착하지 않음")
end
```