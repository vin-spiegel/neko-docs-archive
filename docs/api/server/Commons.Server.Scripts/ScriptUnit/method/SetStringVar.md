---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>SetStringVar</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## SetStringVar(Int32, String)
μ λμ λ¬Έμμ΄ λ³μ κ°μ μ€μ ν©λλ€. μ΅λ 65535 λ°μ΄νΈκΉμ§ μ μ₯ κ°λ₯ν©λλ€.

#### μ μΈ
```cs
public bool SetStringVar(int id, string value)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|id|λ³μ ID|
|System.String|value|ν΄λΉ λ³μμ κ°|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Boolean|	

#### μμ 
```lua
-- μ λμ 16λ² λ¬Έμμ΄ λ³μλ₯Ό "Hello Unit!" λ‘ μ€μ 

unit.SetStringVar(16, "Hello Unit!")
```
