---
layout: default
title: <font color="#2c84fa">π</font> GetAnimation
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## GetAnimation(Int32)
λ°μ΄ν°λ² μ΄μ€μ μ λλ©μ΄μ μ λ³΄

#### μ μΈ
```cs
public TGameAnimation GetAnimation(int id)`
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|id|μ λλ©μ΄μ ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|TGameAnimation|λ°μ΄ν°λ² μ΄μ€μ μ λλ©μ΄μ μ λ³΄|

#### μμ : λ°μ΄ν°λ² μ΄μ€μ μμ±ν 5λ² μ λλ©μ΄μ μ λ³΄ κ°μ Έμ€κΈ°
```lua
local myAni = Server.GetAnimation(5)
```