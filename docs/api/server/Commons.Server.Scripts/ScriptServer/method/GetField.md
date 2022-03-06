---
layout: default
title: <font color="#2c84fa">𝑓</font> GetField
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetField(Int32, Int32)
특정 맵 ID의 필드를 가져옵니다.

#### 선언
```cs
public ScriptField GetField(int mapID, int channelID = -1)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|mapID|가져올 맵 데이터 ID|
|System.Int32|channelID|채널 ID|

#### 반환

|타입|설명|
|:-|:-|
|ScriptField|

#### 예제: 5번 맵의 필드를 가져옵니다
```lua
local myField = Server.GetField(5)
```