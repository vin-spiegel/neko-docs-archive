---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>UnequipItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## UnequipItem(Int64)
μ λμ μ₯μ°©μ€μΈ μμ΄νμ μ₯μ°© ν΄μ ν©λλ€.

#### μ μΈ
```cs
public void UnequipItem(long itemID)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int64|itemID|μμ΄νμ κ³ μ  ID (λ°μ΄ν° λ² μ΄μ€μ ID μλ λ€λ¦λλ€)|

#### μμ : μ λμ΄ μ₯μ°© μ€μΈ 5λ² μμ΄ν μ₯μ°© ν΄μ μν€κΈ°
```lua
unit.UnequipItem(5)
```