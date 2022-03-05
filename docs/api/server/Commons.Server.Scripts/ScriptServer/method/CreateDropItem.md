---
layout: default
title: <font color="#2c84fa">𝑓 </font>CreateDropItem
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## CreateDropItem(Int32, Int32, Int32)
드랍 아이템 생성

#### 선언
```cs
public ScriptDropItem CreateDropItem(int dataID, int count, int level = 0)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|아이템 데이터 ID|
|System.Int32|count|개수|
|System.Int32|level|아이템 레벨 (기본: 0)|

#### 반환

|타입|설명|
|:-|:-|
|ScriptDropItem|

#### 예제
```lua
-- Tip: 생성한 드랍 아이템은 필드에 추가시켜야 주울 수 있습니다

-- 획득하면 5번 아이템을 3개 가질 수 있는 드랍 아이템을 생성합니다
local myDropItem = Server.CreateDropItem(5, 3)

-- 현재 내 유닛이 있는 필드의 2칸 위에 드랍 아이템 추가
unit.field.JoinDropItem(myDropItem, Point(unit.x, unit.y + 64))

-- 바로 유닛한테 줍게 하기
myDropItem.Acquire(unit)
```
