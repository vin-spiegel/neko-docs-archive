---
layout: default
title: <font color="#2c84fa">π</font> CreateItem
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## CreateItem(Int32, Int32)
μμ΄ν μμ±

#### μ μΈ
```cs
public TItem CreateItem(int dataID, int count)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|dataID|λ°μ΄ν°λ² μ΄μ€ ID|
|System.Int32|count|κ°μ|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|TItem|

#### μμ : 5λ² μμ΄νμ 3κ° μμ± ν μ λμκ² μΆκ°νκΈ°
```lua
local myItem = Server.CreateItem(5, 3)
unit.AddItemByTItem(myItem)
```