---
layout: default
title: <font color="#2c84fa">π</font> GetField
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## GetField(Int32, Int32)
νΉμ  λ§΅ IDμ νλλ₯Ό κ°μ Έμ΅λλ€.

#### μ μΈ
```cs
public ScriptField GetField(int mapID, int channelID = -1)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|mapID|κ°μ Έμ¬ λ§΅ λ°μ΄ν° ID|
|System.Int32|channelID|μ±λ ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|ScriptField|

#### μμ : 5λ² λ§΅μ νλλ₯Ό κ°μ Έμ΅λλ€
```lua
local myField = Server.GetField(5)
```