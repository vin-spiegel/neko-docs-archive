---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>GetEquipItem</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## GetEquipItem(Int32)
ν΄λΉ μ¬λ‘―μ μ₯μ°©λμ΄μλ μμ΄νμ μ λ³΄λ₯Ό κ°μ Έμ΅λλ€.

#### μ μΈ
```cs
public TItem GetEquipItem(int equipSlot)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|equipSlot|μ₯μ°© μ¬λ‘― (0 ~ 9)|

#### λ°ν
|νμ|μ€λͺ|
|:-|:-|
|TItem|νμμ μμ΄ν μ λ³΄|

#### μμ : μ λμ΄ μ₯μ°©μ€μΈ λͺ¨μμ μ΄λ¦ μΆλ ₯νκΈ°
```lua
local item = unit.GetEquipItem(0)

if item ~= nil then
    local itemData = Server.GetItem(item.dataID)
    unit.SendCenterLabel(itemData.name)
else
    unit.SendCenterLabel("λͺ¨μκ° μ₯μ°©λμ§ μμμ΅λλ€")
end
```