---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>SpawnAtFieldID</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## SpawnAtFieldID(Int32, Single, Single, Int32)
νλμ IDλ₯Ό μ΄μ©ν΄μ μ§μ λ μ’νμ μ λμ μνν©λλ€.

#### μ μΈ
```cs
public void SpawnAtFieldID(int mapID, float x, float y, int channelID = 0)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|mapID|μνν  νλμ ID|
|System.Single|x|μνν  μμΉμ X μ’ν|
|System.Single|y|μνν  μμΉμ Y μ’ν|
|System.Int32|channelID|μνν  μμΉμ Y μ’ν|

#### μμ : 15λ² λ§΅μ 1λ² μ±λμ μ λ μ΄λ μν€κΈ°
```lua
unit.SpawnAtFieldID(15,4*15,4*16,1)
```