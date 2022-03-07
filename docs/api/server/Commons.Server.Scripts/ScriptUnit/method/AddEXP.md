---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>AddEXP</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## AddEXP(Int64)
유닛에게 경험치를 지급합니다.

#### 선언
```cs
public virtual void AddEXP(long amount)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|지급할 경험치의 양|

#### 예제: 유닛에게 10000 경험치 지급
```lua
unit.AddEXP(10000)
```