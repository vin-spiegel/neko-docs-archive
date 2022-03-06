---
layout: default
title: <font color="#2c84fa">𝑓</font> GetItem
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetItem(Int32)
데이터베이스의 아이템 정보

#### 선언
```cs
public TGameItem GetItem(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|아이템 ID|

#### 반환

|타입|설명|
|:-|:-|
|TGameItem|데이터베이스 아이템 정보|

#### 예제: 데이터베이스에 작성한 5번 아이템 정보 가져오기
```lua
local myItem = Server.GetItem(5)
```