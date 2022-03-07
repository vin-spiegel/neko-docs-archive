---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">𝑓 </font>GetStat</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- 아래로 편집 -->




## GetStat(Int32)
유닛의 능력치(스탯)을 얻어옵니다. 
```
ATTACK = 0
DEFENSE = 1
MAGIC_ATTACK = 2
MAGIC_DEFENSE = 3
AGILITY = 4
LUCKY = 5
HP = 6
MP = 7

[사용자 설정 능력치 (커스텀 스탯)] CUSTOM_1 = 101
...
CUSTOM_32 = 132
```
#### 선언
```cs
public float GetStat(int type)
```
#### 매개 변수(인자)

|타입|이름|설명|
|:-|:-|:-|
|System.Int32|type|해당 스탯()의 타입|

#### 반환

|타입|설명|
|:-|:-|
|System.Single|	

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


-- HP 가져오기
local unitHP = unit.GetStat(6)
-- Lucky 가져오기
local unitLucky = unit.GetStat(5)
```