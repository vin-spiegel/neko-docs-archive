---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>HasBuff</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## HasBuff(Int32)
ν΄λΉ μ λμ΄ μν(Buff)λ₯Ό κ°μ§κ³  μλμ§ μ²΄ν¬ν©λλ€.

#### μ μΈ
```cs
public bool HasBuff(int buffID)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|buffID|μν(Buff) ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Boolean|	

#### μμ : μ λμ΄ 5λ² λ²νλ₯Ό κ°μ§κ³  μλμ§ κ²μ¬
```lua
if unit.HasBuff(5) then
    unit.SendCenterLabel("5λ² λ²νκ° μλ€")
else
    unit.SendCenterLabel("5λ² λ²νκ° μλ€");
end
```