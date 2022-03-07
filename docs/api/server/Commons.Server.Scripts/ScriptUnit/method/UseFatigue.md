---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>UseFatigue</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->

## UseFatigue(Int64)
플레이어 유닛의 피로도를 사용합니다.

#### 선언
```cs
public bool UseFatigue(long amount)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|사용할 피로도의 양|

#### 반환

|타입|설명|
|:-|:-|
|System.Boolean|

#### 예제
```lua
-- 유닛의 피로도를 100 사용합니다

unit.UseFatigue(100)
```
