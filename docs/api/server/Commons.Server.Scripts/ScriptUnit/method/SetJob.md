---
layout: default
title: <div style="white-space:nowrap;"><font color="#2c84fa">π </font>SetJob</div>
parent: ScriptUnit
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## SetJob(Int32, Boolean)
μ§μ IDλ₯Ό ν΅ν΄ μ λμ μ§μμ μ€μ ν©λλ€.

#### μ μΈ
```cs
public virtual void SetJob(int jobID, bool keepSkills = false)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|jobID|λ°μ΄ν° λ² μ΄μ€μ μ§μ ID|
|System.Boolean|keepSkills|μ€ν¬μ μ μ§ (κΈ°λ³Έκ°: True)|

#### μμ : μ€ν¬μ μ μ§νλ©° 5λ² μ§μμΌλ‘ λ³κ²½
```lua
unit.SetJob(5, true)

-- μ€ν¬μ μ μ§νμ§ μμΌλ©΄μ 2λ² μ§μμΌλ‘ λ³κ²½
unit.SetJob(2, false)
```