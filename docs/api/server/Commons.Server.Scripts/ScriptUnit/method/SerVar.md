---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>SerVar</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## SerVar(Int32, Int64)
유닛의 변수 값을 설정합니다. 최대 65535 바이트까지 저장 가능합니다.

#### 선언
```cs
public void SerVar(int id, long value)
```

#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|id|변수 ID|
|System.Int64|value|해당 변수의 값|

#### 예제
```lua
-- 사용을 권장하지 않습니다. ScriptUnit.SetVar() 함수를 사용하세요
```