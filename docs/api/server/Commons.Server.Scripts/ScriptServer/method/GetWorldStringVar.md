---
layout: default
title: <font color="#2c84fa">𝑓</font> GetWorldStringVar
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetWorldStringVar(Int32)
월드 변수 값을 가져온다.

#### 선언
```cs
public string GetWorldStringVar(int id)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.String|

#### 예제: 4번 월드 문자열 변수의 값 출력
```lua
local v = Server.GetWorldStringVar(4)
Server.SendCenterLabel("4번 월드 문자열 변수의 값: " .. v)
```
