---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>GetStringVar</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## GetStringVar(Int32)
μ λμ λ¬Έμμ΄ λ³μ κ°μ μ»μ΄μ΅λλ€.

#### μ μΈ
```cs
public string GetStringVar(int id)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|id|λ³μ ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.String|ν΄λΉ λ³μμ κ°|

#### μμ : μ λμ 16λ² λ¬Έμμ΄ λ³μλ₯Ό μΆλ ₯
```lua
unit.SendCenterLabel(unit.GetStringVar(16))
```