---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>GetSkill</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## GetSkill(Int32)
μ€ν¬μ IDλ₯Ό ν΅ν΄ μ λμ μ€ν¬μ μ»μ΄μ΅λλ€.

#### μ μΈ
```cs
public TSkill GetSkill(int dataID)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|dataID|λ°μ΄ν°λ² μ΄μ€μ μ€ν¬ ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|network.TSkill|μ€ν¬μ νμμΌλ‘ λ°νν©λλ€.|

#### μμ : μ λμ΄ κ°μ§ μ€ν¬ μ€ λ°μ΄ν°λ² μ΄μ€ μ 5λ² μ€ν¬μ μ€ν¬ λ λ²¨μ μΆλ ₯
```lua
local skillInfo = unit.GetSkill(5)

if skillInfo == nil then
    unit.SendCenterLabel("5λ² μ€ν¬μ΄ μμ΅λλ€")
else
    unit.SendCenterLabel('5λ² μ€ν¬μ λ λ²¨: ' .. skillInfo.level)
end
```