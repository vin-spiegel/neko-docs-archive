---
layout: default
title: <font color="#2c84fa">π</font> GetWorldStringVar
parent: ScriptServer
grand_parent: Commons.Server.Scripts
nav_order: 1
---

<!-- μλλ‘ νΈμ§ -->

## GetWorldStringVar(Int32)
μλ λ³μ κ°μ κ°μ Έμ¨λ€.

#### μ μΈ
```cs
public string GetWorldStringVar(int id)
```

#### λ§€κ° λ³μ(μΈμ)

|νμ|μ΄λ¦|μ€λͺ|
|:-|:-|:-|
|System.Int32|id|λ³μ ID|

#### λ°ν

|νμ|μ€λͺ|
|:-|:-|
|System.String|

#### μμ : 4λ² μλ λ¬Έμμ΄ λ³μμ κ° μΆλ ₯
```lua
local v = Server.GetWorldStringVar(4)
Server.SendCenterLabel("4λ² μλ λ¬Έμμ΄ λ³μμ κ°: " .. v)
```
