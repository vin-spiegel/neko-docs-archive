---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>AddBuff</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## AddBuff(Int32, ScriptUnit)
해당 유닛에 상태(Buff)를 추가합니다.

#### 선언
```cs
public void AddBuff(int buffID, ScriptUnit attacker = null)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|buffID|상태(Buff) ID|
|ScriptUnit|attacker|공격한 유닛|

#### 예제
유닛에게 5번 버프를 추가
```lua
unit.AddBuff(5)
```