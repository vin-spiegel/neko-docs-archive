---
layout: default
title: <font color="#2c84fa">π</font> CreateParty
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## CreateParty(String, Int32)
νν° μμ±

#### μ μΈ
```cs
public ScriptParty CreateParty(string name = "", int maxPlayer = 4)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.String|name|νν°μ μ΄λ¦|
|System.Int32|maxPlayer|νν°μ μ΅λ νλ μ΄μ΄ μ (κΈ°λ³Έ: 4λͺ, μ΅λ: 4λͺ)|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|ScriptParty|νν° μ λ³΄|

#### μμ : μ΅λ μΈμμ΄ 4λͺμΈ μ νν°λ₯Ό μμ±ν©λλ€
```lua
local myParty = Server.CreateParty("Nekoland Party!", 4)
```