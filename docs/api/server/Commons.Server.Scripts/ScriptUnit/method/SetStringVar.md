---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>SetStringVar</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## SetStringVar(Int32, String)
유닛의 문자열 변수 값을 설정합니다. 최대 65535 바이트까지 저장 가능합니다.

#### 선언
```cs
public bool SetStringVar(int id, string value)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|
|System.String|value|해당 변수의 값|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|	

#### 예제
```lua
-- 유닛의 16번 문자열 변수를 "Hello Unit!" 로 설정

unit.SetStringVar(16, "Hello Unit!")
```
