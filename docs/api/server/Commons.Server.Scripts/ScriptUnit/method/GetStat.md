---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>GetStat</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->




## GetStat(Int32)
μ λμ λ₯λ ₯μΉ(μ€ν―)μ μ»μ΄μ΅λλ€. 
```
ATTACK = 0
DEFENSE = 1
MAGIC_ATTACK = 2
MAGIC_DEFENSE = 3
AGILITY = 4
LUCKY = 5
HP = 6
MP = 7

[μ¬μ©μ μ€μ  λ₯λ ₯μΉ (μ»€μ€ν μ€ν―)] CUSTOM_1 = 101
...
CUSTOM_32 = 132
```
#### μ μΈ
```cs
public float GetStat(int type)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|type|ν΄λΉ μ€ν―()μ νμ|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Single|	

#### μμ 
```lua
-- ATTACK = 0
-- DEFENSE = 1
-- MAGIC_ATTACK = 2
-- MAGIC_DEFENSE = 3
-- AGILITY = 4
-- LUCKY = 5
-- HP = 6
-- MP = 7

-- [μ¬μ©μ μ€μ  λ₯λ ₯μΉ (μ»€μ€ν μ€ν―)]

-- CUSTOM_1 = 101
-- ...
-- CUSTOM_32 = 132


-- HP κ°μ Έμ€κΈ°
local unitHP = unit.GetStat(6)
-- Lucky κ°μ Έμ€κΈ°
local unitLucky = unit.GetStat(5)
```