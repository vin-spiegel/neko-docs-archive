---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>CountItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## CountItem(Int32)
μμ΄νμ IDλ₯Ό ν΅ν΄ μ λμ΄ ν΄λΉ μμ΄νμ λͺκ°λ μμ νκ³  μλμ§ μμμ΅λλ€.

#### μ μΈ
```cs
public int CountItem(int dataID)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|dataID|λ°μ΄ν° λ² μ΄μ€μ μμ΄ν ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Int32|μ λμ΄ κ°μ§κ³  μλ μμ΄νμ κ°μ (κ°μ§κ³  μμ§ μμλ€λ©΄ 0μ λ°νν©λλ€)|

#### μμ : μ λμ΄ 5λ² μμ΄νμ λͺκ°λ κ°μ§κ³  μλμ§ μΆλ ₯ν©λλ€
```lua
local cnt = unit.CountItem(5)
unit.SendCenterLabel("5λ² μμ΄νμ κ°―μ: " .. cnt)
```