---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>DropItemByDataID</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->



## DropItemByDataID(Int32, Int32)
μ λμ΄ κ°μ§κ³ μλ μμ΄νμ λμ λ¨μ΄λ¨λ¦½λλ€ (λλν©λλ€).

#### μ μΈ
```cs
public void DropItemByDataID(int dataID, int count = 1)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|dataID|λ°μ΄ν°λ² μ΄μ€μ μμ΄ν ID|
|System.Int32|count|κ°μ|

#### μμ : μ μ  μΈλ²€ν λ¦¬μ μλ λ°μ΄ν°λ² μ΄μ€μ 5λ² μμ΄νμ 1κ° λλνκΈ°
```lua
unit.DropItemByDataID(5, 1)
```