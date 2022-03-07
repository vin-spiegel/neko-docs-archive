---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>UseGameMoney</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## UseGameMoney(Int64)
플레이어 유닛의 게임 골드를 사용합니다.

#### 선언
```cs
public bool UseGameMoney(long amount)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|사용할 골드의 양|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|

#### 예제: 유닛의 골드를 10000만큼 제거합니다
```lua
unit.UseGameMoney(10000)
```