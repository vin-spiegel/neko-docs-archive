---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>SendSay</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->



## SendSay(String, UInt32)
μ΄ νλ μ΄μ΄ μ λμ μ±νμ°½μλ§ μΆκ°λλ νμ€νΈλ₯Ό μλλ€.

#### μ μΈ
```cs
public void SendSay(string text, uint color = 4294967295U)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.String|text|λ§(νμ€νΈ)|
|System.UInt32|color|νμ€νΈμ μ (κΈ°λ³Έκ°: κ²μ )|

#### μμ : μ΄ μ λμ `μ±νμ°½`μ "Welcome to Nekoland!" λΌκ³  λμ€κ² νκΈ°
```lua
unit.SendSay("Welcome to Nekoland!")
-- λΉ¨κ°μ
unit.SendSay("Welcome to Nekoland! (Red)", 0xFF0000)
-- μ΄λ‘μ
unit.SendSay("Welcome to Nekoland! (Green)", 0x00FF00)
-- νλμ
unit.SendSay("Welcome to Nekoland! (Blue)", 0x0000FF)
```