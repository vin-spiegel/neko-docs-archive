---
layout: default
title: <font color="#2c84fa">π</font> SendSay
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## SendSay(String, UInt32)
μ±νμ°½μ λ©μΈμ§λ₯Ό νμν©λλ€.

#### μ μΈ
```cs
public void SendSay(string text, uint color = 4294967295U)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.String|text|νμν  λ©μΈμ§|
|System.UInt32|color|μκΉ|

#### μμ : κ²μ μ±νμ°½μ "Hello Nekoland!" λ©μμ§λ₯Ό νμν©λλ€
```lua
Server.SendSay("Hello Nekoland!")
```