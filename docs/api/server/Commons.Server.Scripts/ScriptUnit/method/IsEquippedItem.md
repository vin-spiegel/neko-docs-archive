---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>IsEquippedItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->



## IsEquippedItem(Int64)
μ λμ΄ ν΄λΉ μμ΄νμ μ₯μ°© μ€μΈμ§ μμλλλ€.

#### μ μΈ
```cs
public bool IsEquippedItem(long itemID)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int64|itemID|μμ΄νμ κ³ μ  ID (λ°μ΄ν° λ² μ΄μ€μ ID μλ λ€λ¦λλ€)|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Boolean|μ₯μ°© μ¬λΆ (μ₯μ°© μ€μΌμ: True, μλ μ: False)|

#### μμ : μ λμ μΈλ²€ν λ¦¬λ₯Ό λλ©° μ₯μ°© μ€μΈ μμ΄ν μλ €μ£ΌκΈ°
```lua
local inven = unit.player.GetItems()

for i = 1, #inven do
    if inven[i] ~= nil then
        local itemData = Server.GetItem(inven[i].dataID)
        if unit.IsEquippedItem(inven[i].id) then
            unit.SendSay(i .. "." .. itemData.name .. ": μ₯μ°© μ€")
        else
            unit.SendSay(i .. "." .. itemData.name .. ": λ―Έμ₯μ°©")
        end    
    end
end
```