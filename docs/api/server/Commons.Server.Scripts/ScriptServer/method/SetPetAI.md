---
layout: default
title: <font color="#2c84fa">π </font>SetPetAI
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## SetPetAI(Int32, Closure)
ν« AIλ₯Ό λ±λ‘νλ€.

#### μ μΈ
```cs
public void SetPetAI(int id, Closure c)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|id|ν« ID|
|MoonSharp.Interpreter.Closure|c|AI ν¨μ|

#### μμ : 0λ² ν«μ AI μ€μ 
```lua
Server.SetPetAI(0,
    function(pet, ai, event, data)
        -- μ¬κΈ°μ AI μ½λλ₯Ό μ½μν©λλ€
    end)
```