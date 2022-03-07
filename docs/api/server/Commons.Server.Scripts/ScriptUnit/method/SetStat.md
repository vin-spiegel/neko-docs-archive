---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>SetStat</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->


## SetStat(Int32, Single)
유닛의 스탯 값을 변경합니다.

#### 선언
```cs
public void SetStat(int type, float value)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|	type	|해당 스탯()의 타입|
|System.Single|	value	|변경할 값|

#### 예제
```lua
-- ATTACK = 0
-- DEFENSE = 1
-- MAGIC_ATTACK = 2
-- MAGIC_DEFENSE = 3
-- AGILITY = 4
-- LUCKY = 5
-- HP = 6
-- MP = 7

-- [사용자 설정 능력치 (커스텀 스탯)]

-- CUSTOM_1 = 101
-- ...
-- CUSTOM_32 = 132


-- HP를 999로 설정
unit.SetStat(6, 999)

-- ATTACK을 100으로 설정
unit.SetStat(0, 100)
```