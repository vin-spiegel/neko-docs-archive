---
layout: default
title: <font color="#2c84fa">π </font>CreateDropItem
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## CreateDropItem(Int32, Int32, Int32)
λλ μμ΄ν μμ±

#### μ μΈ
```cs
public ScriptDropItem CreateDropItem(int dataID, int count, int level = 0)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|dataID|μμ΄ν λ°μ΄ν° ID|
|System.Int32|count|κ°μ|
|System.Int32|level|μμ΄ν λ λ²¨ (κΈ°λ³Έ: 0)|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|ScriptDropItem|

#### μμ 
```lua
-- Tip: μμ±ν λλ μμ΄νμ νλμ μΆκ°μμΌμΌ μ£ΌμΈ μ μμ΅λλ€

-- νλνλ©΄ 5λ² μμ΄νμ 3κ° κ°μ§ μ μλ λλ μμ΄νμ μμ±ν©λλ€
local myDropItem = Server.CreateDropItem(5, 3)

-- νμ¬ λ΄ μ λμ΄ μλ νλμ 2μΉΈ μμ λλ μμ΄ν μΆκ°
unit.field.JoinDropItem(myDropItem, Point(unit.x, unit.y + 64))

-- λ°λ‘ μ λνν μ€κ² νκΈ°
myDropItem.Acquire(unit)
```
