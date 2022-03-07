---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>CountItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## CountItem(Int32)
아이템의 ID를 통해 유닛이 해당 아이템을 몇개나 소유하고 있는지 알아옵니다.

#### 선언
```cs
public int CountItem(int dataID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터 베이스의 아이템 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Int32|유닛이 가지고 있던 아이템의 개수 (가지고 있지 않았다면 0을 반환합니다)|

#### 예제: 유닛이 5번 아이템을 몇개나 가지고 있는지 출력합니다
```lua
local cnt = unit.CountItem(5)
unit.SendCenterLabel("5번 아이템의 갯수: " .. cnt)
```