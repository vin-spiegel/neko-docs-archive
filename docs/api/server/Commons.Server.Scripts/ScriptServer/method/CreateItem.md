---
layout: default
title: <font color="#2c84fa">𝑓</font> CreateItem
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## CreateItem(Int32, Int32)
아이템 생성

#### 선언
```cs
public TItem CreateItem(int dataID, int count)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|dataID|데이터베이스 ID|
|System.Int32|count|개수|

#### 반환

|타입|설명|
|:-|:-|
|TItem|

#### 예제: 5번 아이템을 3개 생성 후 유닛에게 추가하기
```lua
local myItem = Server.CreateItem(5, 3)
unit.AddItemByTItem(myItem)
```