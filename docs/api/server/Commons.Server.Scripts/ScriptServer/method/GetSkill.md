---
layout: default
title: <font color="#2c84fa">π</font> GetSkill
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## GetSkill(Int32)
λ°μ΄ν°λ² μ΄μ€μ μ€ν¬ μ λ³΄

#### μ μΈ
```cs
public TGameSkill GetSkill(int id)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|id|μ€ν¬ ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|TGameSkill|λ°μ΄ν°λ² μ΄μ€μ μ€ν¬ μ λ³΄|

#### μμ : λ°μ΄ν°λ² μ΄μ€μ μμ±ν 5λ² μ€ν¬ μ λ³΄ κ°μ Έμ€κΈ°
```lua
local mySkill = Server.GetSkill(5)
```