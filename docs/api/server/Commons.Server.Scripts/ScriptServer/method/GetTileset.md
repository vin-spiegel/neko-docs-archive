---
layout: default
title: <font color="#2c84fa">π</font> GetTileset
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## GetTileset(Int32)
λ°μ΄ν°λ² μ΄μ€μ νμΌμ μ λ³΄

#### μ μΈ
```cs
public TGameTileset GetTileset(int id)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|id|νμΌμ ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|TGameTileset|λ°μ΄ν°λ² μ΄μ€μ νμΌμ μ λ³΄|

#### μμ : λ°μ΄ν°λ² μ΄μ€μ μμ±ν 5λ² νμΌμ μ λ³΄ κ°μ Έμ€κΈ°
```lua
local myTileset = Server.GetTileset(5)
```