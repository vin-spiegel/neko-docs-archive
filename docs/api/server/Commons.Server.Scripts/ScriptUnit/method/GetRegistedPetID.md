---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>GetRegistedPetID</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## GetRegistedPetID()
λ±λ‘λ ν«λ€μ IDλ₯Ό `[]` νμμΌλ‘ λ°νν©λλ€.

#### μ μΈ
```cs
public int[] GetRegistedPetID()
```

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Int32|[]|λ±λ‘λ ν«λ€μ IDκ° λ΄κΈ΄ [] νμ λ°°μ΄|

#### μμ : νμ¬ λ±λ‘λ ν«λ€μ IDλ₯Ό μ°¨λ‘λλ‘ λͺ¨λ μΆλ ₯
```lua
local petIdList = unit.GetRegistedPetID()

for i = 1, #petIdList do
    if petIdList[i] ~= nil then
        unit.SendCenterLabel(petIdList[i])
    end
end
```