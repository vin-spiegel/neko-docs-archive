---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>GetVar</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetVar(Int32)
유닛의 변수 값을 얻어옵니다.

#### 선언
```cs
public long GetVar(int id)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.Int64|해당 변수의 값|

#### 예제: 유닛의 32번 변수를 출력
```lua
unit.SendCenterLabel(unit.GetVar(32))
```
