---
layout: default
title: <font color="#2c84fa">π</font> GetWorldVar
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->


## GetWorldVar(Int32)
μλ λ³μ κ°μ κ°μ Έμ¨λ€.

#### μ μΈ
```cs
public long GetWorldVar(int id)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|id|λ³μ ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.Int64|

#### μμ : 4λ² μλ λ³μμ κ° μΆλ ₯νκΈ°
```lua
local v = Server.GetWorldVar(4)

Server.SendCenterLabel('4λ² μλ λ³μμ κ°: ' .. v)
```