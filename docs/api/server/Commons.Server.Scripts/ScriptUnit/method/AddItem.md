---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>AddItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## AddItem(Int32, Int32, Boolean)
μ λμ μμ΄νμ μΆκ°ν©λλ€.

#### μ μΈ
```cs
public void AddItem(int dataID, int count = 1, bool notify = true)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|dataID|λ°μ΄ν°λ² μ΄μ€μ μμ΄ν ID|
|System.Int32|count|μΆκ°ν  μλ (κΈ°λ³Έκ°: 1)|
|System.Boolean|notify|μμ΄ν νλμμ μλ¦Όμ μ¬μ©ν  κ²μΈμ§λ₯Ό λνλλλ€ (κΈ°λ³Έκ°: True) `Center Label` νμμΌλ‘ μλ¦Όμ΄ νκΈ°λ©λλ€.|

#### μμ 
```lua
-- 0λ² IDμ μμ΄νμ 1κ° μΆκ°νλ©° μλ¦Όμ νμν©λλ€.
unit.AddItem(0, 1, true)

-- 1λ² IDμ μμ΄νμ 2κ° μΆκ°νλ©° μλ¦Όμ νμνμ§ μμ΅λλ€.
unit.AddItem(1, 2)
```