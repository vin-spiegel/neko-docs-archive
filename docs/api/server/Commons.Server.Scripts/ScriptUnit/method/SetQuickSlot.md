---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>SetQuickSlot</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->



## SetQuickSlot(Int32, Int32, Int32)
ν΅μ¬λ‘―μ λ±λ‘λ  μμ΄ν λ° μ€ν¬μ μ€μ ν©λλ€.

#### μ μΈ
```cs
public void SetQuickSlot(int type, int slotID, int dataID = -1)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|type|0 : Clear, 1 : Item, 2 : Skill|
|System.Int32|slotID|0~7|
|System.Int32|dataID|λ°μ΄νλ² μ΄μ€ ID|

#### μμ : μ λμ ν΅μ¬λ‘― μ€μ 
```lua
-- μ λμ 0λ² ν΅μ¬λ‘―μ λΉμ΄λ€
unit.SetQuickSlot(0, 0)

-- μ λμ 1λ² ν΅μ¬λ‘―μ 3λ² μ€ν¬μ μ¬λ €λλ€
unit.SetQuickSlot(2, 1, 3)

-- μ λμ 2λ² ν΅μ¬λ‘―μ ID:5 μΈ μμ΄νμ μ¬λ €λλ€
unit.SetQuickSlot(1, 2, 5)
```
