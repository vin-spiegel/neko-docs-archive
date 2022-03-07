---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>EquipItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## EquipItem(Int64, Boolean)
유닛에 아이템을 장착시킵니다. (이 유닛이 가지고 있는 아이템만 장착이 가능합니다.)

#### 선언
```cs
public void EquipItem(long itemID, bool forced = false)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|itemID|아이템의 고유 ID (데이터 베이스의 ID 와는 다릅니다)|
|System.Boolean|forced|

#### 예제: 유닛에게 5번 아이템 장착시키기
```lua
unit.EquipItem(5)
```