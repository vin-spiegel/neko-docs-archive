---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>SetSkillLevel</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## SetSkillLevel(Int32, Int32)
μ λμ μ€ν¬ λ λ²¨μ μ€μ ν©λλ€.

#### μ μΈ
```cs
public bool SetSkillLevel(int dataID, int level)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|dataID|λ°μ΄ν° λ² μ΄μ€μ μ€ν¬ ID|
|System.Int32|level|λ³κ²½ν  λ λ²¨|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Boolean|μ€ν¬ λ λ²¨ μ€μ μ μ±κ³΅ μ¬λΆ (μ±κ³΅μ: True, μ€ν¨μ: False)|

#### μμ 
```lua
-- μ λμ΄ κ°μ§ μ€ν¬ μ€ λ°μ΄ν°λ² μ΄μ€ μ 5λ² μ€ν¬μ μ€ν¬ λ λ²¨μ 10μΌλ‘ μ€μ 

unit.SetSkillLevel(5, 10)
```