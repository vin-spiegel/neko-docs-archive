---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>GetSingleSummonedPet</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->



## GetSingleSummonedPet()
νμ¬ μν μ€μΈ ν«μ κ°μ Έμ΅λλ€.

#### μ μΈ
```cs
public ScriptPetUnit GetSingleSummonedPet()
```
#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|ScriptPetUnit|ν« μ λμ νμμΌλ‘ λ°νν©λλ€.|

#### μμ : νμ¬ μνλμ΄μλ ν« μ λμ κ°μ Έμ μ΄λ¦ μΆλ ₯
```lua
local myPet = unit.GetSingleSummonedPet()

if myPet == nil then
    unit.SendCenterLabel("μνλ ν«μ΄ μμ΅λλ€")
    return
end

unit.SendCenterLabel("νμ¬ μνλ ν« μ΄λ¦: " .. myPet.name)
```