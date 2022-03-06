---
layout: default
title: <font color="#2c84fa">𝑓</font> SetWorldVar
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## SetWorldVar(Int32, Int64)
월드 변수 값을 설정한다.

#### 선언
```cs
public void SetWorldVar(int id, long value)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|
|System.Int64|value|값|

#### 예제: 4번 월드 변수를 7로 설정
```lua
Server.SetWorldVar(4, 7)
```