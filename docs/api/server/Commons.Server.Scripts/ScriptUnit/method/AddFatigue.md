---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>AddFatigue</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->



## AddFatigue(Int64)
플레이어 유닛에게 피로도를 채워줍니다.

#### 선언
```cs
public void AddFatigue(long amount)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int64|amount|채워줄 피로도의 양|

#### 예제: 유닛의 피로도를 10000 채웁니다
```lua
unit.AddFatigue(10000)
```