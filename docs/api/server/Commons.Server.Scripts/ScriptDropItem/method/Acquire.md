---
layout: default
title: <div style="white-space:nowrap; "><font color="#2c84fa">π </font>Acquire</div>
nav_order: 1
parent: ScriptDropItem
grand_parent: Commons.Server.Scripts
---

## Acquire(ScriptUnit)

ν΄λΉ μμ΄νμ νΉμ  Unitμ΄ κ°μ Έκ° μ μκ²νλ€.

#### μ μΈ
```cs
public int Acquire(ScriptUnit unit)
```

### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|[ScriptUnit](../17.ScriptUnit)|unit|κ°μ²΄|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Int32|

#### μμ 
μ 5λ² λλ μμ΄νμ μμ±νκ³  νλ μ΄μ΄νν νλμν¨λ€
```lua
local dropItem = Server.CreateDropItem(5, 1)
unit.field.JoinDropItem(dropItem)
dropItem.Acquire(unit)
```