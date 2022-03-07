---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>SetQuickSlot</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## SetQuickSlot(Int32, Int32, Int32)
퀵슬롯에 등록될 아이템 및 스킬을 설정합니다.

#### 선언
```cs
public void SetQuickSlot(int type, int slotID, int dataID = -1)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|type|0 : Clear, 1 : Item, 2 : Skill|
|System.Int32|slotID|0~7|
|System.Int32|dataID|데이타베이스 ID|

#### 예제: 유닛의 퀵슬롯 설정
```lua
-- 유닛의 0번 퀵슬롯을 비운다
unit.SetQuickSlot(0, 0)

-- 유닛의 1번 퀵슬롯에 3번 스킬을 올려둔다
unit.SetQuickSlot(2, 1, 3)

-- 유닛의 2번 퀵슬롯에 ID:5 인 아이템을 올려둔다
unit.SetQuickSlot(1, 2, 5)
```
