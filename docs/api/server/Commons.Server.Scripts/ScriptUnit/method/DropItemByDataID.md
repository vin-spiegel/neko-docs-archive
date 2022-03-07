---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>DropItemByDataID</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## DropItemByDataID(Int32, Int32)
유닛이 가지고있는 아이템을 땅에 떨어뜨립니다 (드랍합니다).

#### 선언
```cs
public void DropItemByDataID(int dataID, int count = 1)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터베이스의 아이템 ID|
|System.Int32|count|개수|

#### 예제: 유저 인벤토리에 있는 데이터베이스상 5번 아이템을 1개 드랍하기
```lua
unit.DropItemByDataID(5, 1)
```