---
layout: default
title: <font color="#2c84fa">𝑓</font> CreateField
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## CreateField(Int32)
특정 맵 ID의 필드를 임시로 생성합니다.

#### 선언
```cs
public ScriptField CreateField(int mapID)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|mapID|생성할 맵 데이터 ID|

#### 반환

|타입|설명|
|:-|:-|
|ScriptField|

#### 예제: 5번 맵의 임시 필드를 생성합니다
```lua
local myField = Server.CreateField(5)
```