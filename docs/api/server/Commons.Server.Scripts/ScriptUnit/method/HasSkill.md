---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>HasSkill</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## HasSkill(Int32)
μ€ν¬μ IDλ₯Ό ν΅ν΄ μ λμ μ€ν¬ μ λ¬΄λ₯Ό μμμ΅λλ€.

#### μ μΈ
```cs
public bool HasSkill(int dataID)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|dataID|λ°μ΄ν° λ² μ΄μ€μ μ€ν¬ ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Boolean|μ€ν¬μ μ‘΄μ¬ μ λ¬΄ (μμ: True, μμ: False)|

#### μμ : μ λμ΄ 5λ² μ€ν¬μ κ°μ§κ³  μλμ§ κ²μ¬
```lua
if unit.HasSkill(5) then
    unit.SendCenterLabel("5λ² μ€ν¬μ κ°μ§κ³  μμ΅λλ€")
else
    unit.SendCenterLabel("5λ² μ€ν¬μ΄ μμ΅λλ€")
end
```