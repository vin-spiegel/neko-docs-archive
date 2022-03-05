---
layout: default
title: <font color="#2c84fa">𝑓</font> GetTileset
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetTileset(Int32)
데이터베이스의 타일셋 정보

#### 선언
```cs
public TGameTileset GetTileset(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|타일셋 ID|

#### 반환

|타입|설명|
|:-|:-|
|TGameTileset|데이터베이스의 타일셋 정보|

#### 예제: 데이터베이스에 작성한 5번 타일셋 정보 가져오기
```lua
local myTileset = Server.GetTileset(5)
```