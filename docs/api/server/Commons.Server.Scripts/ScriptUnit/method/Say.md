---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>Say</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->



## Say(String, UInt32)
ν΄λΉ μ λμ΄ λ§νκ² ν©λλ€.

#### μ μΈ
```cs
public void Say(string text, uint color = 4294967295U)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.String|text|λ§(νμ€νΈ)|
|System.UInt32|color|νμ€νΈμ μ (κΈ°λ³Έκ°: κ²μ )|

#### μμ : μ΄ μ λμ΄ "Hello Nekoland!" λΌκ³  λ§νκ² νκΈ°
```lua
unit.Say("Hello Nekoland!")

-- λΉ¨κ°μ
unit.Say("Hello Nekoland! (Red)", 0xFF0000)
-- μ΄λ‘μ
unit.Say("Hello Nekoland! (Green)", 0x00FF00)
-- νλμ
unit.Say("Hello Nekoland! (Blue)", 0x0000FF)
```