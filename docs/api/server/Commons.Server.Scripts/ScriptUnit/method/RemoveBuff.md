---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>RemoveBuff</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## RemoveBuff(Int32)
해당 유닛의 상태(Buff)를 제거합니다.

#### 선언
```cs
public void RemoveBuff(int buffID)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|buffID|상태(Buff) ID|

#### 예제: 유닛에서 5번 버프를 제거
```lua
unit.RemoveBuff(5)
```