---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>GetVar</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## GetVar(Int32)
μ λμ λ³μ κ°μ μ»μ΄μ΅λλ€.

#### μ μΈ
```cs
public long GetVar(int id)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|id|λ³μ ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Int64|ν΄λΉ λ³μμ κ°|

#### μμ : μ λμ 32λ² λ³μλ₯Ό μΆλ ₯
```lua
unit.SendCenterLabel(unit.GetVar(32))
```
