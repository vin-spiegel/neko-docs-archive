---
layout: default
title: <font color="#2c84fa">π</font> CreateField
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## CreateField(Int32)
νΉμ  λ§΅ IDμ νλλ₯Ό μμλ‘ μμ±ν©λλ€.

#### μ μΈ
```cs
public ScriptField CreateField(int mapID)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|mapID|μμ±ν  λ§΅ λ°μ΄ν° ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|ScriptField|

#### μμ : 5λ² λ§΅μ μμ νλλ₯Ό μμ±ν©λλ€
```lua
local myField = Server.CreateField(5)
```