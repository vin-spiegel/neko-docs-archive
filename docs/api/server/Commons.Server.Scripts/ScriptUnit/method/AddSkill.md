---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>AddSkill</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->



## AddSkill(Int32, Int32, Boolean)
νλ μ΄μ΄ μ λμκ² μ€ν¬μ μΆκ°ν©λλ€.

#### μ μΈ
```cs
public void AddSkill(int dataID, int level = 1, bool notify = true)
```
#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|dataID|λ°μ΄ν°λ² μ΄μ€μ μ€ν¬ ID|
|System.Int32|level|μ€ν¬μ λ λ²¨ (κΈ°λ³Έκ°: 1)|
|System.Boolean|notify|μ€ν¬ νλμμ μλ¦Όμ μ¬μ©ν  κ²μΈμ§λ₯Ό λνλλλ€ (κΈ°λ³Έκ°: True) `Center Label` νμμΌλ‘ μλ¦Όμ΄ νκΈ°λ©λλ€.|

#### μμ 
```lua
-- μ λμκ² 10λ λ²¨μ 3λ² μ€ν¬μ μΆκ°νλ©° μλ¦Όμ νμν©λλ€
unit.AddSkill(3, 10, true)

-- μ λμκ² 5λ λ²¨μ 7λ² μ€ν¬μ μΆκ°νλ©° μλ¦Όμ νμνμ§ μμ΅λλ€
unit.AddSkill(7, 5, false)
``` 