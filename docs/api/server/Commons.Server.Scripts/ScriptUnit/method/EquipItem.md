---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>EquipItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## EquipItem(Int64, Boolean)
μ λμ μμ΄νμ μ₯μ°©μν΅λλ€. (μ΄ μ λμ΄ κ°μ§κ³  μλ μμ΄νλ§ μ₯μ°©μ΄ κ°λ₯ν©λλ€.)

#### μ μΈ
```cs
public void EquipItem(long itemID, bool forced = false)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int64|itemID|μμ΄νμ κ³ μ  ID (λ°μ΄ν° λ² μ΄μ€μ ID μλ λ€λ¦λλ€)|
|System.Boolean|forced|

#### μμ : μ λμκ² 5λ² μμ΄ν μ₯μ°©μν€κΈ°
```lua
unit.EquipItem(5)
```