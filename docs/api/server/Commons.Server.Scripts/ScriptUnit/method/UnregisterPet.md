---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>UnregisterPet</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## UnregisterPet(Int32)
ν«μ IDλ₯Ό ν΅ν΄ ν«μ λ±λ‘μ ν΄μ ν©λλ€.

#### μ μΈ
```cs
public void UnregisterPet(int petID)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|petID|λ±λ‘ ν΄μ ν  ν«μ ID|

#### μμ : 0λ² IDλ‘ λ±λ‘λ ν« λ±λ‘ ν΄μ νκΈ°
```lua
-- Note: SpawnPet ν¨μλ‘ ν«μ μνν  λ μλ ₯νλ ν« ID

unit.UnregisterPet(0)
```