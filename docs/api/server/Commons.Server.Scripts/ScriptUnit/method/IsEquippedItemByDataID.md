---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>IsEquippedItemByDataID</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->



## IsEquippedItemByDataID(Int32)
μ λμ΄ ν΄λΉ μμ΄νμ μ₯μ°© μ€μΈμ§ μμλλλ€.

#### μ μΈ
```cs
public bool IsEquippedItemByDataID(int itemDataID)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|itemDataID|λ°μ΄ν° λ² μ΄μ€μ μμ΄ν ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Boolean|μ₯μ°© μ¬λΆ (μ₯μ°© μ€μΌμ: True, μλ μ: False)|

#### μμ : 5λ² μμ΄νμ μ₯μ°©νλμ§ μΆλ ₯νκΈ°
```lua
if unit.IsEquippedItemByDataID(5) then
    unit.SendCenterLabel("5λ² μμ΄ν μ₯μ°© μ€")
else
    unit.SendCenterLabel("5λ² μμ΄ν μ₯μ°©νμ§ μμ")
end
```