---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>AddGameMoney</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## AddGameMoney(Int64)
유닛에게 골드를 지급합니다.

#### 선언
```cs
public void AddGameMoney(long amount)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|지급할 골드의 양|

#### 예제: 유닛에게 10000 골드 지급
```lua
unit.AddGameMoney(10000)
```
