---
layout: default
title: <font color="#2c84fa">π</font> RunLater
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## RunLater(Closure, Single)
t μ΄ νμ, callback ν¨μλ₯Ό μ€νν©λλ€.

#### μ μΈ
```cs
public void RunLater(Closure callback, float t)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|MoonSharp.Interpreter.Closure|callback|μ€νν  ν¨μ|
|System.Single|t|μ€νκΉμ§ λκΈ°μκ° (μ΄)|

#### μμ : 5μ΄ λ€μ λͺ¨λ  ν΄λΌμ΄μΈνΈλ€μκ² λ©μμ§λ₯Ό μ μ‘νκΈ°
```lua
Server.RunLater(function()
    Server.SendCenterLabel('5μ΄ μ§λ¨!')
end, 5)
```