---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>GetSkillLevel</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## GetSkillLevel(Int32)
μ€ν¬μ IDλ₯Ό ν΅ν΄ μ λμ ν΄λΉ μ€ν¬ λ λ²¨μ μμμ΅λλ€.

#### μ μΈ
```cs
public int GetSkillLevel(int dataID)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|dataID|λ°μ΄ν° λ² μ΄μ€μ μ€ν¬ ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Int32|μ€ν¬μ λ λ²¨ (μ€ν¬μ΄ μ‘΄μ¬νμ§ μλλ€λ©΄ `-1`μ λ°νν©λλ€)|

#### μμ 
```lua
-- μ λμ΄ κ°μ§ μ€ν¬ μ€ λ°μ΄ν°λ² μ΄μ€ μ 5λ² μ€ν¬μ μ€ν¬ λ λ²¨μ μΆλ ₯
-- μ€ν¬μ΄ μλ€λ©΄ -1 λ°ν

local skillLvl = unit.GetSkillLevel(5)
unit.SendCenterLabel(skillLvl)
```