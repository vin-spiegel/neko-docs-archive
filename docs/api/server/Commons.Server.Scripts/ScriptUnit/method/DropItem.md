---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>DropItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->



## DropItem(Int64, Int32)
μ λμ΄ κ°μ§κ³ μλ μμ΄νμ λμ λ¨μ΄λ¨λ¦½λλ€ (λλν©λλ€).

#### μ μΈ
```cs
public void DropItem(long id, int count = 1)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int64|id|μ κ±°ν  μμ΄νμ ID.λ°μ΄ν° λ² μ΄μ€μ μμ΄νID κ° μλ μμ΄νλ§μ μ λν¬ ID μλλ€.|
|System.Int32|count|κ°μ|

#### μμ 
```lua
-- μ μ  μΈλ²€ν λ¦¬μ μλ λλ κ°λ₯ν μμ΄ν μ λΆ λλνκΈ°

local items = unit.player.GetItems()

for i = 1, #items do
    if items[i] ~= nil then
        unit.DropItem(items[i].id)
    end
end
```