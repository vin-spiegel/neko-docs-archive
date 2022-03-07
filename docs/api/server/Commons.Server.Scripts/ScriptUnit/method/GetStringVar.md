---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>GetStringVar</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## GetStringVar(Int32)
유닛의 문자열 변수 값을 얻어옵니다.

#### 선언
```cs
public string GetStringVar(int id)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|

#### 반환

|타입|설명|
|:-|:-|
|System.String|해당 변수의 값|

#### 예제: 유닛의 16번 문자열 변수를 출력
```lua
unit.SendCenterLabel(unit.GetStringVar(16))
```