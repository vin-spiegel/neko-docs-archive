---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>RemoveCollection</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## RemoveCollection(Int32)
λκ°μ μ­μ νκ³ , μ­μ μ μ±κ³΅νλμ§λ₯Ό λ°νν©λλ€.

#### μ μΈ
```cs
public bool RemoveCollection(int collectionDataID)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|collectionDataID|λ°μ΄ν°λ² μ΄μ€μ λκ° ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Boolean|μ­μ  μ±κ³΅ μ¬λΆ (μ±κ³΅: True, μ€ν¨: False)|

#### μμ : μ λμ 5λ² λκ° μλ£ μ΄λ ₯μ μ­μ νκΈ°
```lua
unit.RemoveCollection(5)
```