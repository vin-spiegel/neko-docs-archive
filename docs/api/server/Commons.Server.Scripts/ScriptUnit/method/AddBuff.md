---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>AddBuff</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## AddBuff(Int32, ScriptUnit)
ν΄λΉ μ λμ μν(Buff)λ₯Ό μΆκ°ν©λλ€.

#### μ μΈ
```cs
public void AddBuff(int buffID, ScriptUnit attacker = null)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|buffID|μν(Buff) ID|
|ScriptUnit|attacker|κ³΅κ²©ν μ λ|

#### μμ 
μ λμκ² 5λ² λ²νλ₯Ό μΆκ°
```lua
unit.AddBuff(5)
```