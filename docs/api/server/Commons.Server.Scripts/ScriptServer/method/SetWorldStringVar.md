---
layout: default
title: <font color="#2c84fa">𝑓</font> SetWorldStringVar
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## SetWorldStringVar(Int32, String)
월드 변수 값을 설정한다.

#### 선언
```cs
public void SetWorldStringVar(int id, string value)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|
|System.String|value|값|

#### 예제: 4번 월드 문자열 변수에 "Hello Nekoland!" 문자열 저장
```lua
Server.SetWorldStringVar(4, "Hello Nekoland!")
```
