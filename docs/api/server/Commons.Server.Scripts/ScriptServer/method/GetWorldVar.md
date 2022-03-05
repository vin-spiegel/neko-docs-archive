---
layout: default
title: <font color="#2c84fa">𝑓</font> GetWorldVar
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## GetWorldVar(Int32)
월드 변수 값을 가져온다.

#### 선언
```cs
public long GetWorldVar(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Int64|

#### 예제: 4번 월드 변수의 값 출력하기
```lua
local v = Server.GetWorldVar(4)

Server.SendCenterLabel('4번 월드 변수의 값: ' .. v)
```