---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>AddHP</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## AddHP(Int64)
해당 유닛의 HP를 회복시킵니다.

#### 선언
```cs
public void AddHP(long amount)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|회복시킬 HP의 양|

#### 예제: 유닛의 HP를 500 회복
```lua
unit.AddHP(500)
```